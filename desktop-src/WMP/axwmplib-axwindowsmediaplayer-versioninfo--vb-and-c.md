---
title: AxWindowsMediaPlayer.versionInfo - proprietà
description: La proprietà versionInfo ottiene un valore che specifica la versione del Windows Media Player.
ms.assetid: e128bec5-1ae9-4710-800e-4f97df362909
keywords:
- proprietà versionInfo Windows Media Player
- proprietà versionInfo Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player proprietà versionInfo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.versionInfo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd7491af0fc102f03da9855b78ecef79ac0a09ca9b3ab8b49f9bf6b948f0d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118841162"
---
# <a name="axwindowsmediaplayerversioninfo-property"></a>AxWindowsMediaPlayer.versionInfo - proprietà

La proprietà versionInfo ottiene un valore che specifica la versione del Windows Media Player.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String versionInfo {get;}
```


```VB

Public ReadOnly Property versionInfo As System.String
```





## <a name="property-value"></a>Valore proprietà

Oggetto System.String che rappresenta le informazioni sulla versione nel formato seguente: "*X*.0.0. *AAAA*" dove *X* rappresenta il numero di versione principale e *AAAA rappresenta* il numero di build.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un pulsante che, quando si fa clic, visualizza una finestra di messaggio contenente le informazioni sulla versione per Windows Media Player. L'oggetto AxWMPLib.AxWindowsMediaPlayer è rappresentato dalla variabile denominata player.


```CSharp
private void showVersion_Click(object sender, System.EventArgs e)
{
    // Build the message containing the version info. 
    string message = ("Windows Media Player Version: " + player.versionInfo);

    // Display the message. 
    System.Windows.Forms.MessageBox.Show(message);
}
```


```VB

Public Sub showVersion_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showVersion.Click

    &#39; Build the message containing the version info. 
    Dim message As String = (&quot;Windows Media Player Version: &quot; + player.versionInfo)

    &#39; Display the message. 
    System.Windows.Forms.MessageBox.Show(message)

End Sub
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





