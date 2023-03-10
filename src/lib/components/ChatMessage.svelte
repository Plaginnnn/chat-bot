<script lang="ts">
	import type { ChatCompletionRequestMessageRoleEnum } from 'openai'
	export let type: ChatCompletionRequestMessageRoleEnum
	export let message: string
</script>

<div class="chat {type === 'user' ? 'chat-end' : 'chat-start'} justify-end">
	<div class="chat-image avatar">
		<div class="w-9 rounded-full">
			<img
				src={type === 'user'
					? 'https://assets.stickpng.com/images/585e4bf3cb11b227491c339a.png'
					: 'https://media.tproger.ru/uploads/2023/02/4094595_algorithm_gym_learning_openai_reinforcement_icon1-cover-icon-original.png'}
				alt="{type} avatar"
			/>
		</div>
	</div>
	<div class="chat-header" />
	<div class="chat-bubble {type === 'user' ? 'chat-bubble-info' : 'chat-start'}">
		{message}
	</div>
</div>
