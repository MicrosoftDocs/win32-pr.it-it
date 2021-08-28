---
title: AxWindowsMediaPlayer.URL - proprietà
description: La proprietà URL ottiene o imposta il nome dell'elemento multimediale da riprodurre.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- Proprietà URL Windows Media Player
- Proprietà URL Windows Media Player classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player , proprietà URL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.URL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d953f2d85fc1fd83edcd37a491cb2f7cbabc3e3dfaf61e48feb1cd30e6d01934
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123881"
---
# <a name="axwindowsmediaplayerurl-property"></a>AxWindowsMediaPlayer.URL - proprietà

La proprietà URL ottiene o imposta il nome dell'elemento multimediale da riprodurre.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a>Valore proprietà

Oggetto System.String che rappresenta l'URL dell'elemento multimediale.

## <a name="remarks"></a>Commenti

Questa proprietà può essere impostata solo su un URL in un'area di sicurezza uguale o meno restrittiva rispetto all'area di sicurezza del programma chiamante o della pagina Web.

Le applicazioni che aprono elementi multimediali da dietro un firewall avranno prestazioni migliori se l'indirizzo viene specificato usando il nome DNS (Domain Name Server) anziché l'indirizzo IP.

Non chiamare questo metodo dal codice del gestore eventi. La **chiamata dell'URL** da un gestore eventi può produrre risultati imprevisti.

## <a name="examples"></a>Esempio

L'esempio seguente consente all'utente di specificare un file multimediale immettendo un percorso di file in una casella di testo. Quando si fa clic su un pulsante, la proprietà URL viene impostata sul file specificato e il file viene riprodotto. L'oggetto AxWMPLib.AxWindowsMediaPlayer è rappresentato dalla variabile denominata player.


```CSharp
private void openMedia_Click(object sender, System.EventArgs e)
{
    // Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text;

    // Play the media file. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub openMedia_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles openMedia.Click

    &#39; Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text

    &#39; Play the media file. 
    player.Ctlcontrols.play()

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

 

 





