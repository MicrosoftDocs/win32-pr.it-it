---
title: Metodo AxWindowsMediaPlayer.launchURL
description: Il metodo launchURL invia un URL al browser predefinito dell'utente per il rendering. | Metodo AxWindowsMediaPlayer.launchURL
ms.assetid: 3e8dfdbb-b5ad-44ea-97a6-e860386b7fb4
keywords:
- Metodo launchURL Windows Media Player
- Metodo launchURL Windows Media Player , classe AxWindowsMediaPlayer
- La classe AxWindowsMediaPlayer Windows Media Player, metodo launchURL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.launchURL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b4f3ad10a6defe4e7db252a1703888550ff5a89fe2a0d0618dd9886fc5f74bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123991"
---
# <a name="axwindowsmediaplayerlaunchurl-method"></a>Metodo AxWindowsMediaPlayer.launchURL

Il metodo launchURL invia un URL al browser predefinito dell'utente per il rendering.

## <a name="syntax"></a>Sintassi


```CSharp
public void launchURL(
  System.String bstrURL
);
```


```VB

Public Sub launchURL( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrURL* 
</dt> <dd>

**System.String che** rappresenta l'URL da avviare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo apre solo le pagine Web che usano i protocolli HTTP o HTTPS.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un pulsante che, quando selezionato, visualizza il sito Web Microsoft in una nuova finestra del browser. L'oggetto AxWMPLib.AxWindowsMediaPlayer è rappresentato dalla variabile denominata player.


```CSharp
private void goToMS_Click(object sender, System.EventArgs e)
{
    // Open the Microsoft website. 
    player.launchURL("https://www.microsoft.com");
}
```


```VB

Public Sub goToMS_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles goToMS.Click

    &#39; Open the Microsoft website. 
    player.launchURL(&quot;https://www.microsoft.com&quot;)

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

 

 





