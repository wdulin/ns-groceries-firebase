# To Do List


## Next

4. Working in iOS Emulator

5. Forgot Password Working

6. Clean-up/Refactor Code

7. Gif of all three Working

8. Instructions

9. Post to Github


## Done
~~1. Order grocery list from newest to lowest~~ 

~~2. Error: Logout creates firebase.database error~~

~~3. Label truncation is too short in listview.~~



# Feature Tests

### Original Features 

1. Login with pre-created account
2. Account specific grocery items are listed in main listview
3. Adding an item results in a permanent addition to user's grocery items
4. Clicking delete moves item to <Recent> list
5. Clicking item in <Recent> list moves item to <Main Grocery List>
6. Logout returns to <Login Screen> without error.
7. Sign up New User Working
8. Each user has own private grocery list
9. Reset Password



### New Features in Advanced Grocery Example

1. Telerik RadListView allows ordering list
2. Sign In using social networks
3. Online/Offline Indicator and Button
4. Permanent Delete button on <Recent> list
5. Add picture to grocery items using Firebase storage
6. Edit saved item
7. Lookup Item with barcode



## Additional Ideas

1. Framework for abstracting Realtime Offline First Backends 



## Troubleshooting:


1. Logging Off raises the following error in Android Emulator:

com.tns.NativeScriptException: 
Calling js method onCancelled failed

Error: java.lang.AbstractMethodError: abstract method "void com.google.firebase.database.ChildEventListener.onCancelled(com.google.firebase.database.DatabaseError)"
    com.tns.Runtime.callJSMethodNative(Native Method)
    com.tns.Runtime.dispatchCallJSMethodNative(Runtime.java:862)
    com.tns.Runtime.callJSMethodImpl(Runtime.java:727)
    com.tns.Runtime.callJSMethod(Runtime.java:713)
    com.tns.Runtime.callJSMethod(Runtime.java:694)
    com.tns.Runtime.callJSMethod(Runtime.java:684)
    com.tns.gen.com.google.firebase.database.ChildEventListener.onCancelled(ChildEventListener.java:38)
    com.google.android.gms.internal.zzahe.zza(Unknown Source)
    com.google.android.gms.internal.zzajc.zzcta(Unknown Source)
    com.google.android.gms.internal.zzajh$1.run(Unknown Source)
    android.os.Handler.handleCallback(Handler.java:739)
    android.os.Handler.dispatchMessage(Handler.java:95)
    android.os.Looper.loop(Looper.java:135)
    android

    Resolved: Updated version of nativescript-plugin-firebase fixed.

2. Incompatibility with Xcode 8. 

        OS_ACTIVITY_MODE = disable environment variable stops emulator from 
        producing a deluge of log output



3. iOS build throws "Could not locate configuration file: 'GoogleService-Info.plist'." on execution in emulator.

4. iOS build throws "Class PLBuildVersion is implemented in both..." on execution in emulator.

## Child Changed Event

{"type":"ChildAdded","key":"-KS1l7Inwa1RVCXpWTq6","value":{"name":"Milk","done":false,"deleted":false,"dateCreated":1474293957917,"key":""}}
{"type":"ChildAdded","key":"-KS1lHvxF6DYqmkS3WEj","value":{"name":"Potatoes","done":false,"deleted":false,"dateCreated":1474294001448,"key":""}}
{"type":"ChildAdded","key":"-KS1nJTJguLu4M55qBrw","value":{"name":"Butter","done":false,"deleted":false,"dateCreated":1474294532036,"key":""}}
{"type":"ChildAdded","key":"-KS1tMHiJwlrLjuP5cq0","value":{"name":"Ketchup","done":false,"deleted":false,"dateCreated":1474296116485,"key":""}}
{"type":"ChildChanged","key":"-KS1l7Inwa1RVCXpWTq6","value":{"done":true,"deleted":false}}
{"type":"ChildChanged","key":"-KS1l7Inwa1RVCXpWTq6","value":{"done":false,"deleted":true}}
{"type":"ChildRemoved","key":"-KS1l7Inwa1RVCXpWTq6","value":{"done":false,"deleted":true}}



CONSOLE LOG file:///app/shared/login.firebase.service.js:49:20: Login Service : login - {"email":"groceryapp@kingsburytx.com","password":"password"}
CONSOLE LOG file:///app/shared/login.firebase.service.js:78:20: "An error occurred when accessing the keychain. The @c NSLocalizedFailureReasonErrorKey field in the @c NSError.userInfo dictionary will contain more information about the error encountered"