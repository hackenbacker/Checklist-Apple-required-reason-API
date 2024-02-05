# required reason API

## File timestamp APIs
| Name | Used? | Reason |
|------|--------|-------|
| creationDate |   | □ DDA9.1<br>□ C617.1<br>□ 3B52.1<br>□ 0A2A.1 |
| modificationDate | |   □ DDA9.1<br>□ C617.1<br>□ 3B52.1<br>□ 0A2A.1 |
| fileModificationDate | |   □ DDA9.1<br>□ C617.1<br>□ 3B52.1<br>□ 0A2A.1 |
| contentModificationDateKey | |   □ DDA9.1<br>□ C617.1<br>□ 3B52.1<br>□ 0A2A.1 |
| creationDateKey | |  □ DDA9.1<br>□ C617.1<br>□ 3B52.1<br>□ 0A2A.1 |
| getattrlist(\_:\_:\_:\_:\_:) | |  □ DDA9.1<br>□ C617.1<br>□ 3B52.1<br>□ 0A2A.1 |
| getattrlistbulk(\_:\_:\_:\_:\_:) | |  □ DDA9.1<br>□ C617.1<br>□ 3B52.1<br>□ 0A2A.1 |
| fgetattrlist(\_:\_:\_:\_:\_:) | |  □ DDA9.1<br>□ C617.1<br>□ 3B52.1<br>□ 0A2A.1 |
| stat | |  □ DDA9.1<br>□ C617.1<br>□ 3B52.1<br>□ 0A2A.1 |
| fstat(\_:\_:) | |  □ DDA9.1<br>□ C617.1<br>□ 3B52.1<br>□ 0A2A.1 |
| fstatat(\_:\_:\_:\_:) | |  □ DDA9.1<br>□ C617.1<br>□ 3B52.1<br>□ 0A2A.1 |
| lstat(\_:\_:) | |  □ DDA9.1<br>□ C617.1<br>□ 3B52.1<br>□ 0A2A.1 |
| getattrlistat(\_:\_:\_:\_:\_:\_:) | |  □ DDA9.1<br>□ C617.1<br>□ 3B52.1<br>□ 0A2A.1 |

- DDA9.1
    
  Declare this reason to display file timestamps to the person using the device.

  Information accessed for this reason, or any derived information, may not be sent off-device.

  デバイスを使用する人にファイルのタイムスタンプを表示する。

  この理由でアクセスされた情報、または派生する情報は、デバイス外に送信してはならない。

- C617.1
    
  Declare this reason to access the timestamps, size, or other metadata of files inside the app container, app group container, or the app’s CloudKit container.

  アプリコンテナ、アプリグループコンテナ、アプリのCloudKitコンテナ内のファイルのタイムスタンプ、サイズ、その他のメタデータにアクセスする。

- 3B52.1
    
  Declare this reason to access the timestamps, size, or other metadata of files or directories that the user specifically granted access to, such as using a document picker view controller.

  ドキュメントピッカービューコントローラを使用するなどして、ユーザが特にアクセスを許可したファイルやディレクトリのタイムスタンプ、サイズ、その他のメタデータにアクセスする。

- 0A2A.1
    
  Declare this reason if your third-party SDK is providing a wrapper function around file timestamp API(s) for the app to use, and you only access the file timestamp APIs when the app calls your wrapper function. This reason may only be declared by third-party SDKs. This reason may not be declared if your third-party SDK was created primarily to wrap required reason API(s).

  Information accessed for this reason, or any derived information, may not be used for your third-party SDK’s own purposes or sent off-device by your third-party SDK.

  サードパーティSDKが、アプリが使用するファイルタイムスタンプAPIのラッパー関数を提供しており、アプリがラッパー関数を呼び出すときだけファイルタイムスタンプAPIにアクセスする場合、この理由を宣言します。この理由は、サードパーティSDKによってのみ宣言することができます。サードパーティSDKが、主に`required reason API`をラップするために作成された場合、この理由を宣言することはできません。

  この理由でアクセスされた情報、または派生する情報は、サードパーティSDK自身の目的のために利用したり、 サードパーティSDKによってデバイス外に送信したりすることはできません。

## System boot time APIs

| Name | Used? | Reason |
|------|--------|-------|
| systemUptime |  | □ 35F9.1 |
| mach_absolute_time() |  | □ 35F9.1 |

- 35F9.1

  Declare this reason to access the system boot time in order to measure the amount of time that has elapsed between events that occurred within the app or to perform calculations to enable timers.

  Information accessed for this reason, or any derived information, may not be sent off-device. There is an exception for information about the amount of time that has elapsed between events that occurred within the app, which may be sent off-device.

  アプリ内で発生したイベント間の経過時間を測定するため、またはタイマーを有効にするための計算を実行するために、システム起動時間にアクセスする。

  この理由でアクセスされた情報、または派生する情報は、デバイス外に送信することはできません。ただし、アプリ内で発生したイベント間の経過時間に関する情報は例外であり、デバイス外に送信することができます。

## Disk space APIs

| Name | Used? | Reason |
|------|--------|-------|
| volumeAvailableCapacityKey | | □ 85F4.1<br>□ E174.1<br>□ 7D9E.1 |
| volumeAvailableCapacityForImportantUsageKey |  | □ 85F4.1<br>□ E174.1<br>□ 7D9E.1 |
| volumeAvailableCapacityForOpportunisticUsageKey |  | □ 85F4.1<br>□ E174.1<br>□ 7D9E.1 |
| volumeTotalCapacityKey |  | □ 85F4.1<br>□ E174.1<br>□ 7D9E.1 |
| systemFreeSize |  | □ 85F4.1<br>□ E174.1<br>□ 7D9E.1 |
| systemSize |  | □ 85F4.1<br>□ E174.1<br>□ 7D9E.1 |
| statfs(\_:\_:) |  | □ 85F4.1<br>□ E174.1<br>□ 7D9E.1 |
| statvfs(\_:\_:) |  | □ 85F4.1<br>□ E174.1<br>□ 7D9E.1 |
| fstatfs(\_:\_:) |  | □ 85F4.1<br>□ E174.1<br>□ 7D9E.1 |
| fstatvfs(\_:\_:) |  | □ 85F4.1<br>□ E174.1<br>□ 7D9E.1 |
| getattrlist(\_:\_:\_:\_:\_:) |  | □ 85F4.1<br>□ E174.1<br>□ 7D9E.1 |
| fgetattrlist(\_:\_:\_:\_:\_:) |  | □ 85F4.1<br>□ E174.1<br>□ 7D9E.1 |
| getattrlistat(\_:\_:\_:\_:\_:\_:) |  | □ 85F4.1<br>□ E174.1<br>□ 7D9E.1 |

- 85F4.1
  
  Declare this reason to display disk space information to the person using the device. Disk space may be displayed in units of information (such as bytes) or units of time combined with a media type (such as minutes of HD video).

  Information accessed for this reason, or any derived information, may not be sent off-device. There is an exception that allows the app to send disk space information over the local network to another device operated by the same person only for the purpose of displaying disk space information on that device; this exception only applies if the user has provided explicit permission to send disk space information, and the information may not be sent over the Internet.

  デバイスを使用する人にディスク容量情報を表示する。ディスク容量は、情報単位（バイトなど）またはメディアタイプと組み合わされた時間単位（HDビデオの分単位など）で表示することができる。

  このような理由でアクセスされた情報、または派生する情報は、デバイス外に送信することはできません。この例外は、ディスク容量情報を送信するための明示的な許可をユーザーが提供した場合にのみ適用され、情報はインターネット経由で送信することはできません。

- E174.1

  Declare this reason to check whether there is sufficient disk space to write files, or to check whether the disk space is low so that the app can delete files when the disk space is low. The app must behave differently based on disk space in a way that is observable to users.

  Information accessed for this reason, or any derived information, may not be sent off-device. There is an exception that allows the app to avoid downloading files from a server when disk space is insufficient.

  ファイルを書き込むのに十分なディスク容量があるかどうかをチェックするため、またはディスク容量が少ないときにアプリがファイルを削除できるように、ディスク容量が少ないかどうかをチェックする。アプリは、ユーザーが観察可能な方法で、ディスク容量に基づいて異なる動作をしなければならない。

  このような理由でアクセスされた情報、または派生する情報は、デバイス外に送信することはできません。ディスクの空き容量が不足している場合、アプリがサーバーからファイルをダウンロードしないようにする例外があります。

- 7D9E.1

  Declare this reason to include disk space information in an optional bug report that the person using the device chooses to submit. The disk space information must be prominently displayed to the person as part of the report.

  Information accessed for this reason, or any derived information, may be sent off-device only after the user affirmatively chooses to submit the specific bug report including disk space information, and only for the purpose of investigating or responding to the bug report.

  デバイスを使用する人が任意で提出するバグレポートにディスク容量情報を含める。ディスク容量情報は、報告書の一部としてその人に目立つように表示されなければなりません。

  この理由でアクセスされた情報、または派生する情報は、ユーザーがディスクスペース情報を含む特定のバグ報告を提出することを明確に選択した後、バグ報告の調査または対応の目的でのみ、デバイス外に送信することができます。

## Active keyboard APIs

| Name | Used? | Reason |
|------|--------|-------|
| activeInputModes |  | □ 3EC4.1<br>□ 54BD.1 |

- 3EC4.1
  Declare this reason if your app is a custom keyboard app, and you access this API category to determine the keyboards that are active on the device.

  Providing a systemwide custom keyboard to the user must be the primary functionality of the app.

  Information accessed for this reason, or any derived information, may not be sent off-device.

  アプリがカスタムキーボードアプリで、デバイス上でアクティブなキーボードを決定するためにこのAPIカテゴリにアクセスする。

  ユーザーにシステム全体のカスタムキーボードを提供することが、アプリの主要な機能でなければなりません。

  この理由でアクセスされた情報、または派生する情報は、デバイス外に送信することはできません。

- 54BD.1

  Declare this reason to access active keyboard information to present the correct customized user interface to the person using the device. The app must have text fields for entering or editing text and must behave differently based on active keyboards in a way that is observable to users.

  Information accessed for this reason, or any derived information, may not be sent off-device.

  デバイスを使用する人に正しくカスタマイズされたユーザー・インターフェースを提示するために、アクティブ・キーボード情報にアクセスする。アプリは、テキストを入力または編集するためのテキストフィールドを持たなければならず、ユーザーが観察可能な方法でアクティブキーボードに基づいて異なる動作をしなければならない。

  このような理由でアクセスされた情報、または派生する情報は、デバイス外に送信することはできません。

## User defaults APIs

| Name | Used? | Reason |
|------|--------|-------|
| UserDefaults |  | □ CA92.1<br>□ 1C8F.1<br>□ C56D.1<br>□ AC6B.1 |

- CA92.1

  Declare this reason to access user defaults to read and write information that is only accessible to the app itself.

  This reason does not permit reading information that was written by other apps or the system, or writing information that can be accessed by other apps.

  ユーザーデフォルトにアクセスするためにこの理由を宣言し、アプリ自身のみがアクセス可能な情報を読み書きする。

  この理由は、他のアプリやシステムによって書き込まれた情報の読み取りや、他のアプリがアクセスできる情報の書き込みを許可しません。

- 1C8F.1

  Declare this reason to access user defaults to read and write information that is only accessible to the apps, app extensions, and App Clips that are members of the same App Group as the app itself.

  This reason does not permit reading information that was written by apps, app extensions, or App Clips outside the same App Group or by the system. This reason also does not permit writing information that can be accessed by apps, app extensions, or App Clips outside the same App Group.

  アプリ自身と同じApp Groupのメンバーであるアプリ、アプリ拡張、App Clipのみがアクセス可能な情報を読み書きするために、ユーザーデフォルトにアクセスする。

  この理由では、同じ App Group 外のアプリ、アプリ拡張機能、App Clip、またはシステムによって書き込まれた情報の読み取りは許可されません。この理由はまた、同じApp Group外のアプリ、アプリ拡張、またはApp Clipがアクセスできる情報の書き込みを許可しない。

- C56D.1

  Declare this reason if your third-party SDK is providing a wrapper function around user defaults API(s) for the app to use, and you only access the user defaults APIs when the app calls your wrapper function. This reason may only be declared by third-party SDKs. This reason may not be declared if your third-party SDK was created primarily to wrap required reason API(s).

  Information accessed for this reason, or any derived information, may not be used for your third-party SDK’s own purposes or sent off-device by your third-party SDK.

  サードパーティSDKが、アプリが使用するユーザーデフォルトAPIのラッパー関数を提供しており、アプリがラッパー関数を呼び出すときのみユーザーデフォルトAPIにアクセスする。この理由は、サードパーティSDKによってのみ宣言することができます。サードパーティSDKが、主に必要な理由APIをラップするために作成された場合、この理由を宣言することはできません。

  この理由のためにアクセスされる情報、あるいは、派生する情報は、サードパーティSDK自身の目的のために利用されたり、 サードパーティSDKによってデバイス外に送信されることはありません。

- AC6B.1

  Declare this reason to access user defaults to read the com.apple.configuration.managed key to retrieve the managed app configuration set by MDM, or to set the com.apple.feedback.managed key to store feedback information to be queried over MDM, as described in the Apple Mobile Device Management Protocol Reference documentation.

  Apple Mobile Device Management Protocol Referenceドキュメントに記載されているように、MDMによって設定された管理対象アプリの設定を取得するためにcom.apple.configuration.managedキーを読み取るためのユーザーデフォルトにアクセスする、またはMDMを介してクエリされるフィードバック情報を格納するためにcom.apple.feedback.managedキーを設定する。

---
### Note
[Describing use of required reason API](https://developer.apple.com/documentation/bundleresources/privacy_manifest_files/describing_use_of_required_reason_api)