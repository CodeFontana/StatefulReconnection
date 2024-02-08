# StatefulReconnection
Based on https://github.com/SteveSandersonMS/StatefulReconnection
For .NET 7.0, only.

This is an alternative UX to the default Blazor Server experience, when the SignalR/WebSocket connection to the server is disconnected.

## Test out examples in App.razor

```
@* Example #1: Default experience, with built-in UI and default reconnection parameters. *@
<StatefulReconnection />
```
![image](https://github.com/CodeFontana/StatefulReconnection/assets/41308769/42ec7852-2955-4325-aeaf-b6b7c355be14)

```
@* Example #2: Default UI, with custom reconnection parameters. *@
@* <StatefulReconnection MaxRetries="20" RetryIntervalMilliseconds="1000" /> *@
```
![image](https://github.com/CodeFontana/StatefulReconnection/assets/41308769/0eac5da3-d26c-4e55-a271-d408bca0df66)

```
@* Example #3: Custom UI and reconnection parameters, using Bootstrap classes, as an example. *@
@* <StatefulReconnection MaxRetries="600" RetryIntervalMilliseconds="1000">
    <ReconnectContent>
        <div class="d-flex justify-content-center" style="margin-top: 10vh;">
            <div class="card">
                <div class="card-body">
                    <h5 class="mb-0">Rejoining the server...</h5>
                </div>
                <div class="card-footer d-flex justify-content-center">
                    <button class="btn btn-primary flex-grow-1" onclick="location.reload()">Reload</button>
                </div>
            </div>
        </div>
    </ReconnectContent>
</StatefulReconnection> *@
```
![image](https://github.com/CodeFontana/StatefulReconnection/assets/41308769/9184e31e-7520-4eb0-97ad-65d7169d350d)

```
@* Example #4: Custom component, using bootstrap classes, demonstrating display of reconnection progress,
               per provided reconnection parameters. This example takes advantage of the optional feedback
               elements that can be populated by the StatefulReconnection.razor.js script. *@
@* <CustomStatefulReconnection /> *@
```
![image](https://github.com/CodeFontana/StatefulReconnection/assets/41308769/2fec23dd-4013-4454-9124-b9eed2c3d25e)

```
@* Example #5: Another custom component, using a bootstrap modal, demonstrating additional styling and
               animation, with using Blazor CSS isolation.*@
@* <AnotherCustomStatefulReconnection /> *@
```
![image](https://github.com/CodeFontana/StatefulReconnection/assets/41308769/59a56cf4-484e-41e6-bcd7-58a59ba29136)
