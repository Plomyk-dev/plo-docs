# 👮 Dispatch API

{% hint style="warning" %}
Implementing this features requires basic knowladge of fivem platform. Always make backups before implementing or use [Version Control System](#user-content-fn-1)[^1]&#x20;
{% endhint %}

{% hint style="info" %}
We use <mark style="color:green;">**`SV`**</mark> to mark Server Only Exports and <mark style="color:orange;">**`CL`**</mark> for client only exports
{% endhint %}

## Create a new call  <mark style="color:green;">`SV`</mark>

Create new call in dispatch system. Will be shown and accesible to all players with authorization to this call.

```lua
exports.plo_notify:AddCall(CallData)
```

* CallData: `object`
  * title: `string`
  * message: `string`
  * priority: `"low"|"medium"|"high"|"critical"|"request"`
  * duration?: `number`  <i class="fa-message-exclamation">:message-exclamation:</i> Duration in miliseconds when dispatch will be visible on player screen
  * code?: `string`  <i class="fa-message-exclamation">:message-exclamation:</i> Not defining this parameter will skip code element in UI.
  * jobs?: `string[]`  <i class="fa-message-exclamation">:message-exclamation:</i> Not defining this parameter will use `Config.Dispatch.DefaultJobs`
  * coords?: `vec3`  <i class="fa-message-exclamation">:message-exclamation:</i> Not defining this parameter will skip street code element in UI and won't allow to use **navigate feature** for this call
  * maxAssignableOfficers?: `number`  <i class="fa-message-exclamation">:message-exclamation:</i> Not defining this parameter will disable max assignable officers limiter
  * incidentData?:&#x20;



[^1]: Tool that tracks and manages changes to code over time. Recommended <i class="fa-github">:github:</i> Github / <i class="fa-gitlab">:gitlab:</i> Gitlab
