<template>
  <LayoutContainer>
    <LayoutContainerContent>
      <UiHeading>
        {{ $t('headings.look_back_on_2024') }}
      </UiHeading>
      <p class="text-balance">
        {{ $t('pages.home.look_back_on_2024') }}
      </p>

      <UiImage
        class="rounded-lg shadow-xl"
        src="/pragvue2024.webp"
        :title="$t('pages.home.link_2024')"
        :alt="$t('accessibility.photo_of_the_speakers_from_2024')"
      />
    </LayoutContainerContent>
  </LayoutContainer>
</template>
