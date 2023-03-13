<script setup lang="ts">
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>1. 上传语音</template>
    根据提示文案，朗读并上传您的语音数据以作为语音质量评估。
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>2. 智能纠错</template>
    基于深度神经网络，算法自动比对学员和标准发音，在短时间内提出建议。
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>3. 学员画像</template>
    我们为每位学员构建成长画像，这包括线上与线下的交互及独立作业等。
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>4. 作品分享</template>

    拥抱微信内容生态，一键分享语音作品到朋友，家人等。
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>5. 专家指导</template>

    可选线下付费资优英语，由英语教育专家进行小班教育，精选每堂课的内容。
  </WelcomeItem>
</template>
