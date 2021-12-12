<template>
  <div>
    <!-- <Button size="large" :onClick="refresh"> My Button </Button>
    <Lable size="small" type="positive">لیبل</Lable>
    <NotificationBadge numeric>۱۲</NotificationBadge> -->
    <!-- <div>
      <Icon name="terminal" />
    </div> -->
    <!-- <Icon name="terminal" /> -->
    <!-- <Input
      :startInput="startInput"
      @startInput="startInput = $event"
      :endInput="endInput"
      @endInput="endInput = $event"
    />
    {{ text }}
    <TextField v-model="text" />
    <Link text="gved" to="/home" />
		<Logo name="zarinpal" type="logo" language="fa" size="medium" /> -->
    <NavigationBar>
      <SwitchTerminalPopover>
        <template v-slot:terminal>
          <SwitchTerminal
            title="عنوان درگاه"
            link="zarinp.al/getway"
            icon="terminal"
          >
          </SwitchTerminal>
        </template>
        <template v-slot:menu>
          <Overview link="overview" active> نمای کلی </Overview>
          <SwitchTerminalItem
            title="عنوان درگاه"
            link="zarinp.al/getway"
            icon="terminal"
            active
            state="active"
            state-text="وضعیت"
          />
          <SwitchTerminalItem
            title="عنوان درگاه"
            link="zarinp.al/getway"
            icon="terminal"
            state="inactive"
            state-text="وضعیت"
          />
          <Create link="/home"> ایجاد درگاه جدید </Create>
        </template>
      </SwitchTerminalPopover>
      <template v-slot:logo>
        <Logo name="zarinpal" type="logo" language="fa" size="medium" />
      </template>
      <template v-slot:firstList>
        <NavItem
          active
          link="/"
          title="لیبل"
          icon="questionCircle"
          badge="12"
        />
        <NavItem link="/" title="لیبل" icon="questionCircle" badge="12" />
      </template>
      <template v-slot:secondList>
        <NavItem link="/" title="لیبل" icon="questionCircle" />
        <NavItem link="/" title="لیبل" icon="questionCircle" />
      </template>
    </NavigationBar>
  </div>
</template>
