<!doctype html>
<html lang="en">

<head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    .cuboid
  width 100%
  height 100%
  position relative
  // 1 is the top and go t, r, b, l, f, b

  &__side:nth-of-type(1)
    height calc(var(--thickness) * 1vmin)
    width 100%
    position absolute
    top 0
    transform translate(0, -50%) rotateX(90deg)

  &__side:nth-of-type(2)
    height 100%
    width calc(var(--thickness) * 1vmin)
    position absolute
    top 50%
    right 0
    transform translate(50%, -50%) rotateY(90deg)

  &__side:nth-of-type(3)
    width 100%
    height calc(var(--thickness) * 1vmin)
    position absolute
    bottom 0
    transform translate(0%, 50%) rotateX(90deg)

  &__side:nth-of-type(4)
    height 100%
    width calc(var(--thickness) * 1vmin)
    position absolute
    left 0
    top 50%
    transform translate(-50%, -50%) rotateY(90deg)

  &__side:nth-of-type(5)
    height 100%
    width 100%
    transform translate3d(0, 0, calc(var(--thickness) * 0.5vmin))
    position absolute
    top 0
    left 0

  &__side:nth-of-type(6)
    height 100%
    width 100%
    transform translate3d(0, 0, calc(var(--thickness) * -0.5vmin)) rotateY(180deg)
    position absolute
    top 0
    left 0

*
*:after
*:before
  box-sizing border-box
  transform-style preserve-3d
  transition background 0.1s ease

body
  min-height 100vh
  display grid
  background var(--bg)
  place-items center
  touch-action none

:root
  --base-size 1vmin
  --base-height calc(45 * 0.65)
  --base-width calc(75 * 0.65)
  --speed 0.4s
  --bg 'hsl(210, 80%, %s)' % calc((15 + (var(--on, 0) * 75)) * 1%)
  --width calc(var(--base-width) * var(--base-size))
  --height calc(var(--base-height) * var(--base-size))
  --road-one 'hsl(0, 0%, %s)' % calc((40 + (var(--on, 0) * 35)) * 1%)
  --road-two 'hsl(0, 0%, %s)' % calc((30 + (var(--on, 0) * 35)) * 1%)
  --road-three 'hsl(0, 0%, %s)' % calc((20 + (var(--on, 0) * 35)) * 1%)
  --road-four 'hsl(0, 0%, %s)' % calc((10 + (var(--on, 0) * 35)) * 1%)
  --road-marking-one 'hsl(0, 0%, %s)' % calc((85 + (var(--on, 0) * 15)) * 1%)
  --road-marking-two 'hsl(0, 0%, %s)' % calc((80 + (var(--on, 0) * 15)) * 1%)
  --road-marking-three 'hsl(0, 0%, %s)' % calc((75 + (var(--on, 0) * 15)) * 1%)
  --white-one 'hsl(0, 0%, %s)' % calc((85 + (var(--on, 0) * 10)) * 1%)
  --white-two 'hsl(0, 0%, %s)' % calc((80 + (var(--on, 0) * 10)) * 1%)
  --white-three 'hsl(0, 0%, %s)' % calc((75 + (var(--on, 0) * 10)) * 1%)
  --white-four 'hsl(0, 0%, %s)' % calc((70 + (var(--on, 0) * 10)) * 1%)
  --glass-one 'hsl(210, 80%, %s)' % calc((85 + (var(--on, 0) * 10)) * 1%)
  --glass-two 'hsl(210, 80%, %s)' % calc((80 + (var(--on, 0) * 10)) * 1%)
  --glass-three 'hsl(210, 80%, %s)' % calc((75 + (var(--on, 0) * 10)) * 1%)
  --glass-four 'hsl(210, 80%, %s)' % calc((70 + (var(--on, 0) * 10)) * 1%)
  --bumper-one 'hsl(0, 0%, %s)' % calc((80 + (var(--on, 0) * 10)) * 1%)
  --bumper-two 'hsl(0, 0%, %s)' % calc((75 + (var(--on, 0) * 10)) * 1%)
  --bumper-three 'hsl(0, 0%, %s)' % calc((70 + (var(--on, 0) * 10)) * 1%)
  --bumper-four 'hsl(0, 0%, %s)' % calc((65 + (var(--on, 0) * 10)) * 1%)
  --wheel-one 'hsl(0, 0%, %s)' % calc((15 + (var(--on, 0) * 10)) * 1%)
  --wheel-two 'hsl(0, 0%, %s)' % calc((10 + (var(--on, 0) * 10)) * 1%)
  --wheel-three 'hsl(0, 0%, %s)' % calc((5 + (var(--on, 0) * 10)) * 1%)
  --wheel-four 'hsl(0, 0%, %s)' % calc((0 + (var(--on, 0) * 10)) * 1%)
  --white-four 'hsl(0, 0%, %s)' % calc((70 + (var(--on, 0) * 10)) * 1%)
  --black-one 'hsl(0, 0%, %s)' % calc((20 + (var(--on, 0) * 10)) * 1%)
  --black-two 'hsl(0, 0%, %s)' % calc((15 + (var(--on, 0) * 10)) * 1%)
  --black-three 'hsl(0, 0%, %s)' % calc((10 + (var(--on, 0) * 10)) * 1%)
  --black-four 'hsl(0, 0%, %s)' % calc((5 + (var(--on, 0) * 10)) * 1%)
  --hub 'hsl(0, 0%, %s)' % calc((65 + (var(--on, 0) * 25)) * 1%)
  --glare hsla(0, 0%, 100%, 0.25)
  --siren-red hsla(5, 90%, 50%, 0.25)
  --siren-blue hsla(205, 90%, 50%, 0.25)
  --lamp 'hsl(45, 90%, 90%, %s)' % calc(0.75 - calc(var(--on, 0) * 0.75))
  --headlight 'hsl(45, 90%, 100%, %s)' % calc(1 - calc(var(--on, 0) * 0.5))
  --indicator 'hsl(35, 90%, 50%, %s)' % calc(1 - calc(var(--on, 0) * 0.5))
  --taillight 'hsl(0, 90%, 50%, %s)' % calc(1 - calc(var(--on, 0) * 0.5))
  --shift calc(var(--height) * 0.1)
  --bob calc(var(--width) * 0.08)
  --bob-speed 2s
  --shift-speed 5s

.scene
  position fixed
  height var(--height)
  width var(--width)
  top 50%
  left 50%
  transform translate3d(-50%, -50%, 100vmin)
  transform translate3d(-50%, -65%, 100vmin) rotateX(-24deg) rotateY(44deg) rotateX(calc(var(--rotate-x, 0) * 1deg)) rotateY(calc(var(--rotate-y, 0) * 1deg))

.road
  position absolute
  bottom 0
  width 100%
  height 20%
  transform translate3d(0, 1px, 0)

.car
  position absolute
  height 100%
  width 100%
  animation bob var(--bob-speed) infinite linear alternate

  @keyframes bob
    0%
      transform translate(calc(var(--bob) * -0.5))
    100%
      transform translate(calc(var(--bob) * 1.5))

  &__bob
    position absolute
    left 50%
    bottom 20%
    height 50%
    width 50%
    transform translate3d(-50%, 0%, 0vmin)
    animation shift var(--shift-speed) infinite linear alternate

    @keyframes shift
      0%
        transform translate3d(-50%, 0%, calc(var(--shift) * -1))
      100%
        transform translate3d(-50%, 0%, calc(var(--shift) * 1))

  & > *
    position absolute

  &__shadow
    width 100%
    height calc(var(--height) * 0.4)
    background hsla(0, 0%, 0%, 0.5)
    bottom 0
    transform translate(0, 50%) rotateX(90deg) translate3d(0, 0, 1px) scale(1.05, 1.1)

  &__headlights
    width 25%
    height calc(var(--height) * 0.5)
    bottom 0%
    left 0
    transform translate(-125%, 50%) rotateX(90deg) translate3d(0, 0, 1px)
    position relative

    &:after
    &:before
      content ''
      position absolute
      height 50%
      width 100%
      background var(--lamp)
      border-radius 50%
      filter blur(10px)

    &:after
      top 0

    &:before
      bottom 0


  &__wheel
    height calc(var(--height) * 0.13)
    width calc(var(--height) * 0.13)
    bottom 0

    &--f
      left 10%

    &--r
      right 10%

    &--osf
    &--osr
      transform translate3d(0, 0, calc(var(--height) * 0.2))
    &--nsf
    &--nsr
      transform translate3d(0, 0, calc(var(--height) * -0.2))

  &__body
    &--bottom
      bottom 5%
      width 100%
      height 40%

    &--top
      bottom 44.5%
      width 60%
      height 40%
      left 22%

  &__siren
    bottom 85%
    height calc(var(--height) * 0.0725)
    width calc(var(--height) * 0.0725)
    left 50%

    & > *
      position absolute
      top 0
      left 0

  &__mirrors
    width 5%
    height 13%
    left 24%
    bottom 40%

  &__mirror
    height 100%
    position absolute
    width 100%

    &--left
      transform translate3d(0, 0, calc((var(--height) * 0.2325) + 2px))
    &--right
      transform translate3d(0, 0, calc((var(--height) * -0.2325) - 2px))

  &__bumper
    height calc(var(--height) * 0.05)
    width calc(var(--height) * 0.05)
    bottom 4%

    &--front
      left 0
      transform translate(-40%, 0)
    &--rear
      right 0
      transform translate(40%, 0)



.body
  --thickness calc(var(--base-height) * 0.4)

  &--top
    div
      background var(--white-two)

      &:nth-of-type(1)
        // background-color var(--white-one)
        background linear-gradient(90deg, transparent 0 20%, var(--white-one) 20% 80%, transparent 80% 100%)

      &:nth-of-type(2)
        background transparent

        &:after
          content ''
          position absolute
          width 100%
          height 112%
          background var(--white-two)
          bottom 0
          left 50%
          transform translate(-50%, 0) rotateX(27deg)
          transform-origin 50% 100%

        &:before
          content ''
          position absolute
          width 100%
          height 112%
          background linear-gradient(55deg, transparent 0 30%, var(--glare) 30% 40%, transparent 40% 45%, var(--glare) 45% 50%, transparent 50% 100%), var(--glass-two)
          bottom 0
          left 50%
          transform translate(-50%, 0) rotateX(27deg) translate3d(0, 0, 1px)
          transform-origin 50% 100%
          --clip inset(10% 10% 10% 10%)
          -webkit-clip-path var(--clip)
          clip-path var(--clip)

      &:nth-of-type(3)
        background var(--white-four)

      &:nth-of-type(4)
        background-color transparent

        &:after
          content ''
          position absolute
          width 100%
          height 112%
          background var(--white-two)
          bottom 0
          left 50%
          transform translate(-50%, 0) rotateX(-27deg)
          transform-origin 50% 100%

        &:before
          content ''
          position absolute
          width 100%
          height 112%
          background linear-gradient(55deg, transparent 0 30%, var(--glare) 30% 40%, transparent 40% 45%, var(--glare) 45% 50%, transparent 50% 100%), var(--glass-two)
          bottom 0
          left 50%
          transform translate(-50%, 0) rotateX(-27deg) translate3d(0, 0, -1px)
          transform-origin 50% 100%
          --clip inset(10% 10% 10% 10%)
          -webkit-clip-path var(--clip)
          clip-path var(--clip)

      &:nth-of-type(5)
        background var(--white-three)
        --clip polygon(0 100%, 20% 0, 80% 0, 100% 100%)
        -webkit-clip-path var(--clip)
        clip-path var(--clip)

        &:after
          content ''
          background linear-gradient(var(--white-three), var(--white-three)) 65% 50% / 8% 100% no-repeat
          background-color var(--glass-three)
          position absolute
          height 90%
          width 90%
          bottom 0
          left 50%
          transform translate(-50%, 0)
          --clip polygon(0 100%, 20% 0, 80% 0, 100% 100%)
          -webkit-clip-path var(--clip)
          clip-path var(--clip)

      &:nth-of-type(6)
        background var(--white-four)
        --clip polygon(0 100%, 20% 0, 80% 0, 100% 100%)
        -webkit-clip-path var(--clip)
        clip-path var(--clip)

        &:after
          content ''
          background linear-gradient(var(--white-four), var(--white-four)) 35% 50% / 8% 100% no-repeat
          background-color var(--glass-four)
          position absolute
          height 90%
          width 90%
          bottom 0
          left 50%
          transform translate(-50%, 0)
          --clip polygon(0 100%, 20% 0, 80% 0, 100% 100%)
          -webkit-clip-path var(--clip)
          clip-path var(--clip)


  &--bottom
    div
      background var(--black-two)

      &:nth-of-type(1)
        background linear-gradient(90deg, var(--black-one) 0 22%, var(--white-one) 22% 82%, var(--black-one) 82% 100%)
        background-color var(--black-one)

        &:after
          content ''
          background var(--black-one)
          position absolute
          top 50%
          left 50%
          height 99%
          width 101%
          transform translate3d(-50%, -50%, -1px)

        &:before
          content '382'
          font-family sans-serif
          font-weight bold
          height 30%
          width 40%
          text-align center
          overflow hidden
          position absolute
          font-size calc(var(--height) * 0.1)
          color var(--white-one)
          right 0
          bottom 50%
          transform translate3d(50%, 50%, 2px) rotate(-90deg) translate(0, -50%)

      &:nth-of-type(2)
        background linear-gradient(var(--indicator), var(--indicator)) 95% 50% / 5% 25% no-repeat,
          linear-gradient(var(--indicator), var(--indicator)) 5% 50% / 5% 25% no-repeat,
          linear-gradient(var(--taillight), var(--taillight)) 10% 50% / 15% 25% no-repeat,
          linear-gradient(var(--taillight), var(--taillight)) 90% 50% / 15% 25% no-repeat
        background-color var(--black-two)

      &:nth-of-type(3)
        background-color var(--black-four)

      &:nth-of-type(4)
        background repeating-linear-gradient(transparent 0 20%, var(--black-four) 20% 40%) 50% 50% / 25% 25% no-repeat,
          linear-gradient(var(--bumper-one), var(--bumper-one)) 50% 50% / 35% 25% no-repeat,
          linear-gradient(var(--indicator), var(--indicator)) 95% 50% / 5% 25% no-repeat,
          linear-gradient(var(--indicator), var(--indicator)) 5% 50% / 5% 25% no-repeat,
          linear-gradient(var(--headlight), var(--headlight)) 10% 50% / 15% 25% no-repeat,
          linear-gradient(var(--headlight), var(--headlight)) 90% 50% / 15% 25% no-repeat
        background-color var(--black-two)

      &:nth-of-type(5)
        background linear-gradient(90deg, var(--black-three) 0 22%, var(--white-three) 22% 82%, var(--black-three) 82% 100%)
        background-color var(--black-three)

        &:after
          content ''
          height 75%
          width 35%
          background url(https://assets.codepen.io/605876/bear--gold-badge--large.png)
          background-repeat no-repeat
          background-size contain
          position absolute
          left 35%
          top 50%
          transform translate(0, -50%)

      &:nth-of-type(6)
        background linear-gradient(90deg, var(--black-four) 0 18%, var(--white-four) 18% 78%, var(--black-four) 78% 100%)
        background-color var(--black-four)

        &:after
          content ''
          height 75%
          width 35%
          background url(https://assets.codepen.io/605876/bear--gold-badge--large.png)
          background-repeat no-repeat
          background-size contain
          position absolute
          left 45%
          top 50%
          transform translate(0, -50%)

.scene__road
  --thickness calc(var(--base-height))

  & > div

    &:nth-of-type(1)
      background-color var(--road-one)

    &:nth-of-type(2)
      background var(--road-two)

    &:nth-of-type(3)
      background var(--road-four)

    &:nth-of-type(4)
      background-color var(--road-two)

    &:nth-of-type(5)
      background var(--road-three)
    &:nth-of-type(6)
      background var(--road-four)

.siren--red
  --thickness calc(var(--base-height) * 0.1)
  --alpha 0.25
  transform translate3d(0, 0, calc(var(--height) * -0.075))
  --siren-red 'hsla(5, 90%, 50%, %s)' % var(--alpha)
  animation flash var(--siren) infinite
  div
    background var(--siren-red)
.siren--blue
  --alpha 0.25
  --thickness calc(var(--base-height) * 0.1)
  --siren-blue 'hsla(210, 90%, 50%, %s)' % var(--alpha)
  transform translate3d(0, 0, calc(var(--height) * 0.075))
  animation flash var(--siren) infinite reverse
  div
    background var(--siren-blue)

.siren--middle
  --thickness calc(var(--base-height) * 0.05)
  transform translate3d(0, 0, 0)

  div
    background var(--white-one)

    &:nth-of-type(1)
      background var(--white-one)
    &:nth-of-type(2)
      background var(--white-two)
    &:nth-of-type(3)
      background var(--white-three)
    &:nth-of-type(4)
    &:nth-of-type(5)
      background var(--white-four)
    &:nth-of-type(6)
      background var(--white-three)

.wheel
  --thickness calc(var(--base-height) * 0.05)

  div
    background var(--wheel-four)

    &:nth-of-type(1)
      background var(--wheel-one)
    &:nth-of-type(2)
      background var(--wheel-two)
    &:nth-of-type(3)
      background var(--wheel-three)
    &:nth-of-type(4)
      background var(--wheel-four)
    &:nth-of-type(5)
      background linear-gradient(var(--hub), var(--hub)) 50% 50% / 35% 35% no-repeat
      background-color var(--wheel-four)
    &:nth-of-type(6)
      background linear-gradient(var(--hub), var(--hub)) 50% 50% / 35% 35% no-repeat
      background-color var(--wheel-three)

.bumper
  --thickness calc(var(--base-height) * 0.45)

  div
    background var(--bumper-one)

    &:nth-of-type(1)
      background var(--bumper-one)
    &:nth-of-type(2)
      background var(--bumper-two)
    &:nth-of-type(3)
      background var(--bumper-three)
    &:nth-of-type(4)
    &:nth-of-type(5)
      background var(--bumper-four)
    &:nth-of-type(6)
      background var(--bumper-three)

.mirror
  --thickness calc(var(--base-height) * 0.075)

  div
    background var(--black-two)

    &:nth-of-type(1)
      background-color var(--black-one)

    &:nth-of-type(2)
      background linear-gradient(var(--white-one), var(--white-one)) 50% 50% / 75% 75% no-repeat
      background-color var(--black-two)

    &:nth-of-type(3)
      background var(--black-four)

    &:nth-of-type(4)
      background-color var(--black-two)

    &:nth-of-type(5)
      background var(--black-three)
    &:nth-of-type(6)
      background var(--black-four)

.road__markings
  height 100%
  width 100%
  overflow hidden

  &--bottom
    transform translate3d(0, 0, -1px)
    &:after
      content ''
      position absolute
      height 100%
      width calc(var(--width) * 2)
      background repeating-linear-gradient(270deg, var(--road-marking-three) 0 10%, transparent 10% 15%) 0 50% / 100% 5% no-repeat
      bottom 0
      left 50%
      transform translate3d(-50%, 0, 0)
      animation roll-bottom var(--speed) infinite linear

  &--front
    transform translate3d(0, 0, -1px)
    &:after
      content ''
      position absolute
      height calc(var(--base-height) * 1vmin)
      width calc(var(--width) * 2)
      background repeating-linear-gradient(270deg, var(--road-marking-two) 0 10%, transparent 10% 15%) 0 50% / 100% 5% no-repeat
      top 0%
      left 50%
      transform translate(-50%, -50%) rotate(-90deg) translate3d(-35%, 0, -1px)
      animation roll-front var(--speed) infinite linear

      @keyframes roll-front
        to
          transform translate(-50%, -50%) rotate(-90deg) translate3d(-20%, 0, -1px)
  &--back
    transform translate3d(0, 0, 1px)
    &:after
      content ''
      position absolute
      height calc(var(--base-height) * 1vmin)
      width calc(var(--width) * 2)
      background repeating-linear-gradient(270deg, var(--road-marking-two) 0 10%, transparent 10% 15%) 0 50% / 100% 5% no-repeat
      top 0%
      left 50%
      transform translate(-50%, -50%) rotate(-90deg) translate3d(-35%, 0, 1px)
      animation roll-back var(--speed) infinite linear

      @keyframes roll-back
        to
          transform translate(-50%, -50%) rotate(-90deg) translate3d(-50%, 0, 1px)
  &--top
    transform translate3d(0, 0, 1px)
    &:after
      content ''
      position absolute
      height 100%
      width calc(var(--width) * 2)
      background repeating-linear-gradient(270deg, var(--road-marking-one) 0 10%, transparent 10% 15%) 0 50% / 100% 5% no-repeat
      bottom 0
      left 50%
      transform translate3d(-50%, 0, 1px)
      animation roll-top var(--speed) infinite linear

    @keyframes roll-top
      to
        transform translate3d(-35%, 0, 1px)

@keyframes roll-bottom
  to
    transform translate3d(-65%, 0, 0)

@keyframes flash
  50%
    --alpha 1

.controls
  position fixed
  bottom 1rem
  right 1rem
  display flex
  flex-direction column

  & > * + *
    margin-top 1rem
button
  height 48px
  width 48px
  cursor pointer
  transform translate3d(0, 0, 150vmin)
  appearance none
  border 0
  background transparent
  outline transparent

  & > svg
    position absolute
    height 100%
    width 100%
    top 0
    left 0

  path
    fill 'hsl(210, 80%, %s)' % calc((90 - (var(--on, 0) * 75)) * 1%)

  svg:nth-of-type(1)
  span:nth-of-type(1)
    display none

  span
    position absolute
    width 1px
    height 1px
    padding 0
    margin -1px
    overflow hidden
    clip rect(0, 0, 0, 0)
    white-space nowrap
    border-width 0

[aria-pressed="true"]
  svg:nth-of-type(1)
  span:nth-of-type(1)
    display block
  svg:nth-of-type(2)
  span:nth-of-type(2)
    display none
    <link rel="stylesheet" href="style.css">

    <title>Coding Torque</title>
</head>

<body>
    mixin cuboid()
  .cuboid(class!=attributes.class)
    - let s = 0
    while s < 6
      .cuboid__side
      - s++

.scene
  .road
    .cuboid.scene__road
      .cuboid__side
        .road__markings.road__markings--top
      .cuboid__side
        .road__markings.road__markings--back
      .cuboid__side
        .road__markings.road__markings--bottom
      .cuboid__side
        .road__markings.road__markings--front
      .cuboid__side
      .cuboid__side
  .car__bob
    .car
      .car__body.car__body--bottom
        +cuboid()(class="body body--bottom")
      .car__body.car__body--top
        +cuboid()(class="body body--top")
      .car__siren
        +cuboid()(class="siren--blue")
        +cuboid()(class="siren--middle")
        +cuboid()(class="siren--red")
      .car__wheel.car__wheel--nsf.car__wheel--f
        +cuboid()(class="wheel")
      .car__wheel.car__wheel--nsr.car__wheel--r
        +cuboid()(class="wheel")
      .car__wheel.car__wheel--osf.car__wheel--f
        +cuboid()(class="wheel")
      .car__wheel.car__wheel--osr.car__wheel--r
        +cuboid()(class="wheel")
      .car__mirrors
        .car__mirror.car__mirror--left
          +cuboid()(class="mirror")
        .car__mirror.car__mirror--right
          +cuboid()(class="mirror")
      .car__bumper.car__bumper--front
        +cuboid()(class="bumper")
      .car__bumper.car__bumper--rear
        +cuboid()(class="bumper")
      .car__shadow
      .car__headlights
.controls
  button.audio-toggle(title='Toggle audio')
    span Turn Audio Off
    span Turn Audio On
    svg(viewBox="0 0 512 512" width="100" title="volume-mute")
      path(d="M215.03 71.05L126.06 160H24c-13.26 0-24 10.74-24 24v144c0 13.25 10.74 24 24 24h102.06l88.97 88.95c15.03 15.03 40.97 4.47 40.97-16.97V88.02c0-21.46-25.96-31.98-40.97-16.97zM461.64 256l45.64-45.64c6.3-6.3 6.3-16.52 0-22.82l-22.82-22.82c-6.3-6.3-16.52-6.3-22.82 0L416 210.36l-45.64-45.64c-6.3-6.3-16.52-6.3-22.82 0l-22.82 22.82c-6.3 6.3-6.3 16.52 0 22.82L370.36 256l-45.63 45.63c-6.3 6.3-6.3 16.52 0 22.82l22.82 22.82c6.3 6.3 16.52 6.3 22.82 0L416 301.64l45.64 45.64c6.3 6.3 16.52 6.3 22.82 0l22.82-22.82c6.3-6.3 6.3-16.52 0-22.82L461.64 256z")
    svg(viewBox="0 0 576 512" width="100" title="volume-up")
      path(d="M215.03 71.05L126.06 160H24c-13.26 0-24 10.74-24 24v144c0 13.25 10.74 24 24 24h102.06l88.97 88.95c15.03 15.03 40.97 4.47 40.97-16.97V88.02c0-21.46-25.96-31.98-40.97-16.97zm233.32-51.08c-11.17-7.33-26.18-4.24-33.51 6.95-7.34 11.17-4.22 26.18 6.95 33.51 66.27 43.49 105.82 116.6 105.82 195.58 0 78.98-39.55 152.09-105.82 195.58-11.17 7.32-14.29 22.34-6.95 33.5 7.04 10.71 21.93 14.56 33.51 6.95C528.27 439.58 576 351.33 576 256S528.27 72.43 448.35 19.97zM480 256c0-63.53-32.06-121.94-85.77-156.24-11.19-7.14-26.03-3.82-33.12 7.46s-3.78 26.21 7.41 33.36C408.27 165.97 432 209.11 432 256s-23.73 90.03-63.48 115.42c-11.19 7.14-14.5 22.07-7.41 33.36 6.51 10.36 21.12 15.14 33.12 7.46C447.94 377.94 480 319.54 480 256zm-141.77-76.87c-11.58-6.33-26.19-2.16-32.61 9.45-6.39 11.61-2.16 26.2 9.45 32.61C327.98 228.28 336 241.63 336 256c0 14.38-8.02 27.72-20.92 34.81-11.61 6.41-15.84 21-9.45 32.61 6.43 11.66 21.05 15.8 32.61 9.45 28.23-15.55 45.77-45 45.77-76.88s-17.54-61.32-45.78-76.86z")
  button.theme-toggle(title='Toggle theme')
    span Turn Lights Off
    span Turn Lights On
    svg(viewBox="0 0 512 512" width="100" title="moon")
      path(d="M283.211 512c78.962 0 151.079-35.925 198.857-94.792 7.068-8.708-.639-21.43-11.562-19.35-124.203 23.654-238.262-71.576-238.262-196.954 0-72.222 38.662-138.635 101.498-174.394 9.686-5.512 7.25-20.197-3.756-22.23A258.156 258.156 0 0 0 283.211 0c-141.309 0-256 114.511-256 256 0 141.309 114.511 256 256 256z")
    svg(viewBox="0 0 512 512" width="100" title="sun")
      path(d="M256 160c-52.9 0-96 43.1-96 96s43.1 96 96 96 96-43.1 96-96-43.1-96-96-96zm246.4 80.5l-94.7-47.3 33.5-100.4c4.5-13.6-8.4-26.5-21.9-21.9l-100.4 33.5-47.4-94.8c-6.4-12.8-24.6-12.8-31 0l-47.3 94.7L92.7 70.8c-13.6-4.5-26.5 8.4-21.9 21.9l33.5 100.4-94.7 47.4c-12.8 6.4-12.8 24.6 0 31l94.7 47.3-33.5 100.5c-4.5 13.6 8.4 26.5 21.9 21.9l100.4-33.5 47.3 94.7c6.4 12.8 24.6 12.8 31 0l47.3-94.7 100.4 33.5c13.6 4.5 26.5-8.4 21.9-21.9l-33.5-100.4 94.7-47.3c13-6.5 13-24.7.2-31.1zm-155.9 106c-49.9 49.9-131.1 49.9-181 0-49.9-49.9-49.9-131.1 0-181 49.9-49.9 131.1-49.9 181 0 49.9 49.9 49.9 131.1 0 181z")

</body>

</html>
