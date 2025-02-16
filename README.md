## Hi 👋 This is Ammytz 
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
