---
title: Proprietà IWMPMedia imageSourceWidth
description: La proprietà imageSourceWidth ottiene la larghezza dell'elemento multimediale corrente in pixel.
ms.assetid: d3644217-6faf-415e-b0c0-23db85c31a3a
keywords:
- Proprietà imageSourceWidth Windows Media Player
- proprietà imageSourceWidth Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player proprietà imageSourceWidth
topic_type:
- apiref
api_name:
- IWMPMedia.imageSourceWidth
- IWMPMedia.get_imageSourceWidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c24d9cb6d6c8cdec29984fa66b6cb12e254413ca518ed12a3089627aeeb08e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098791"
---
# <a name="iwmpmediaimagesourcewidth-property"></a>Proprietà IWMPMedia::imageSourceWidth

La **proprietà imageSourceWidth** ottiene la larghezza dell'elemento multimediale corrente in pixel.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 imageSourceWidth {get;}
```


```VB

Public ReadOnly Property imageSourceWidth As System.Int32
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.Int32** che rappresenta la larghezza dell'elemento multimediale.

## <a name="remarks"></a>Commenti

Se l'elemento multimediale non è quello corrente, questa proprietà restituisce zero.

Prima di usare questa proprietà, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

L'esempio seguente usa **imageSourceWidth** per visualizzare le dimensioni dell'immagine, in pixel, dell'elemento multimediale corrente in una casella di testo. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the new media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
        // Store the height and width of the new media item.
        int height = player.currentMedia.imageSourceHeight;
        int width = player.currentMedia.imageSourceWidth;

        // Clear all the information in the text box.
        videoSize.Clear();

        // Test whether an image is visible.
        if (height != 0 && width != 0)
        {
            // Display the image size information.
            videoSize.Text = (width.ToString() + " x " + height.ToString());
        }
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the new media item is open.
    If (e.newState = WMPLib.WMPOpenState.wmposMediaOpen) Then

        &#39; Store the height and width of the new media item.
        Dim Height As Integer = player.currentMedia.imageSourceHeight
        Dim Width As Integer = player.currentMedia.imageSourceWidth

        &#39; Clear all the information in the text box.
        videoSize.Clear()

        &#39; Test whether an image is visible.
        If (Height <> 0 And Width <> 0) Then

            &#39; Display the image size information.
            videoSize.Text = (Width.ToString() + &quot; x &quot; + Height.ToString())

        End If

    End If

End Sub
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





