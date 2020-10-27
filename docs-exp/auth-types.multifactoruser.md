<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@firebase/auth-types](./auth-types.md) &gt; [MultiFactorUser](./auth-types.multifactoruser.md)

## MultiFactorUser interface

This is the interface that defines the multi-factor related properties and operations pertaining to a [User](./auth-types.user.md)<!-- -->.

<b>Signature:</b>

```typescript
export interface MultiFactorUser 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [enrolledFactors](./auth-types.multifactoruser.enrolledfactors.md) | [MultiFactorInfo](./auth-types.multifactorinfo.md)<!-- -->\[\] | Returns a list of the user's enrolled second factors. |

## Methods

|  Method | Description |
|  --- | --- |
|  [enroll(assertion, displayName)](./auth-types.multifactoruser.enroll.md) | Enrolls a second factor as identified by the [MultiFactorAssertion](./auth-types.multifactorassertion.md) for the user. On resolution, the user tokens are updated to reflect the change in the JWT payload. Accepts an additional display name parameter used to identify the second factor to the end user. Recent re-authentication is required for this operation to succeed. On successful enrollment, existing Firebase sessions (refresh tokens) are revoked. When a new factor is enrolled, an email notification is sent to the user’s email. |
|  [getSession()](./auth-types.multifactoruser.getsession.md) | Returns the session identifier for a second factor enrollment operation. This is used to identify the user trying to enroll a second factor. |
|  [unenroll(option)](./auth-types.multifactoruser.unenroll.md) | Unenrolls the specified second factor. To specify the factor to remove, pass a [MultiFactorInfo](./auth-types.multifactorinfo.md) object (retrieved from [MultiFactorUser.enrolledFactors](./auth-types.multifactoruser.enrolledfactors.md)<!-- -->) or the factor's UID string. Sessions are not revoked when the account is unenrolled. An email notification is likely to be sent to the user notifying them of the change. Recent re-authentication is required for this operation to succeed. When an existing factor is unenrolled, an email notification is sent to the user’s email. |
