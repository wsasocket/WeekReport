<template>
  <v-app>
    <v-main>
      <v-container class="fill-height" fluid>
        <v-row align="center" justify="center">
          <v-col cols="12" sm="8" md="8">
            <v-card class="elevation-12">
              <v-window v-model="step">
                <v-window-item :value="1">
                  <v-row>
                    <v-col cols="12" md="4" class="teal accent-3">
                      <h1 class="display-2 text-center mt-12 white--text">
                        你好，我的伙伴
                      </h1>
                      <div class="px-4">
                        <h3 class="subtitle-1 white--text mt-4 text-left">
                          Python是一种计算机程序设计语言。你可能已经听说过很多种流行的编程语言，比如非常难学的C语言，非常流行的Java语言，适合初学者的Basic语言，适合网页编程的JavaScript语言等等。
                        </h3>
                      </div>

                      <div class="text-center mt-6">
                        <v-btn rounded outlined dark @click="++step"
                          >登录</v-btn
                        >
                      </div>
                    </v-col>
                    <v-col cols="12" md="8">
                      <v-card-text class="mt-12">
                        <h1
                          class="text-center display-2 teal--text text--accent-3"
                        >
                          欢迎注册日报及周报系统
                        </h1>
                        <div class="text-center mt-4">
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon> fab fa-facebook-f </v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon> fab fa-linkedin-in </v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon> fab fa-google-plus-g </v-icon>
                          </v-btn>
                        </div>
                        <h4 class="text-center mt-4">
                          注册需要填写完整的email和电话信息，请牢记你设置用户名和口令
                        </h4>
                        <v-form class="my-n3">
                          <v-text-field
                            type="text"
                            color="teal accent-3"
                            prepend-icon="account_box"
                            label="Username"
                            name="Username"
                          />
                          <v-text-field
                            color="teal accent-3"
                            prepend-icon="vpn_key"
                            label="Password"
                            name="Password"
                            :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                            :type="show1 ? 'text' : 'password'"
                            counter
                            @click:append="show1 = !show1"
                            :rules="[rules.required, rules.min]"
                          />
                          <v-text-field
                            type="text"
                            color="teal accent-3"
                            prepend-icon="email"
                            label="Email"
                            name="Email"
                            :rules="[rules.required, rules.phone]"
                          />
                        </v-form>
                        <h4 class="font-weight-light text-center text--black">
                          注册出现问题？
                        </h4>
                      </v-card-text>
                      <div class="text-center mt-3">
                        <v-btn color="teal accent-3" rounded dark>注册</v-btn>
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>
                <v-window-item :value="2">
                  <v-row>
                    <v-col cols="12" md="8">
                      <v-card-text class="mt-12">
                        <h1
                          class="text-center display-2 teal--text text--accent-3"
                        >
                          欢迎登录日报及周报系统
                        </h1>
                        <div class="text-center mt-4">
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon> fab fa-facebook-f </v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon> fab fa-linkedin-in </v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon> fab fa-google-plus-g </v-icon>
                          </v-btn>
                        </div>
                        <h4 class="text-center mt-4">
                          登录的凭据可以持续使用30天
                        </h4>
                        <v-form class="mt-12">
                          <v-text-field
                            type="text"
                            color="teal accent-3"
                            prepend-icon="account_box"
                            label="Username"
                            name="Username"
                          />
                          <v-text-field
                            color="teal accent-3"
                            prepend-icon="vpn_key"
                            label="Password"
                            name="Password"
                            :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                            :type="show1 ? 'text' : 'password'"
                            counter
                            @click:append="show1 = !show1"
                            :rules="[rules.required, rules.min]"
                          />
                          <!-- <v-text-field
                            type="text"
                            color="teal accent-3"
                            prepend-icon="email"
                            label="Email"
                            name="Email"
                            :rules="[rules.required, rules.phone]"
                          /> -->
                        </v-form>
                        <h4 class="font-weight-light text-center text--black">
                          登录出现问题？
                        </h4>
                      </v-card-text>
                      <div class="text-center mt-3">
                        <v-btn color="teal accent-3" rounded dark>登录</v-btn>
                      </div>
                    </v-col>
                    <v-col cols="12" md="4" class="teal accent-3">
                      <h1 class="display-2 text-center mt-12 white--text">
                        欢迎你，我的伙伴
                      </h1>
                      <div class="px-4">
                        <h3 class="subtitle-1 white--text mt-4 text-left">
                          研发过程中，很多工作步骤枯燥耗时，具有较强的重复性或规律性，研发人员往往考虑会将这部分内容用自动化代替，如此一来，团队就可以把更多时间投入在核心工作和更有创造性的任务上。例如，在发布工具库中有大量的脚本，这些脚本可以自动完成，这样研发人员也不会遗漏琐碎的部分，节省大量时间和精力。
                        </h3>
                      </div>
                      <div class="text-center mt-6">
                        <v-btn rounded outlined dark @click="++step"
                          >注册</v-btn
                        >
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>
              </v-window>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    step: 1,
    show1: false,
    rules: {
      required: (value) => !!value || "Required.",
      min: (v) => v.length >= 8 || "Min 8 characters",
      phone: (v) => v.length == 13 || "Pls input you Phone Number",
    },
  }),
  props: {
    source: String,
  },
};
</script>
