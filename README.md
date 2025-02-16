## Hi 👋 This is Ammytz-MJ

<<!--
**Ammytz/Ammytz** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...Tech
- 🌱 I’m currently learning ...about the world 
- 👯 I’m looking to collaborate on ...my actions
- 🤔 I’m looking for help with ...any device
- 💬 Ask me about .. anything 
- 📫 How to reach me: ...
- 😄 Pronouns: ...sounds cool
- ⚡ Fun fact: ... entertainment 
-->
@dataclass
class Event:
    """
    Represents a GitHub webhook event.
    """

    name: str
    """ The name of the event. Could be `pull_request`, for example."""

    delivery_id: str
    """The delivery ID of the event."""

    signature: t.Optional[str]
    """The signature of the event. Will only be set if a Webhook-secret is configured on the
    client side (e.g. in [`Webhook.secret`][github_bot_api.webhook.Webhook] / if the *webhook_secret* parameter is
    passed to [`accept_event()`][github_bot_api.event.accept_event])."""

    user_agent: str
    """The user agent invoking the webhook."""

    payload: t.Dict[str, t.Any]
    """The event payload."""
