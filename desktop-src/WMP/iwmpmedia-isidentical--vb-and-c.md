---
title: IWMPMedia.isIdentical (VB e C )
description: La proprietà isIdentical (il metodo get isIdentical in C\ ) ottiene un valore che indica se l'elemento multimediale specificato è uguale \_ a quello corrente.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- IWMPMedia.isIdentical (VB e C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPMedia.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e8de133003bdddcf0438e5a13dc3fa74227ede7bf42350e2b7c3c96f2c197e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003581"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a>IWMPMedia.isIdentical (VB e C#)

La **proprietà isIdentical** (metodo **get \_ isIdentical** in C#) ottiene un valore che indica se l'elemento multimediale specificato è uguale a quello corrente.


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPMedia As IWMPMedia
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPMedia pIWMPMedia
);
```



## <a name="parameters"></a>Parametri

*pIWMPMedia*

Interfaccia **WMPLib.IWMPMedia** per l'elemento multimediale da confrontare con l'elemento multimediale corrente.

## <a name="property-value"></a>Valore della proprietà

Valore **System.Boolean** che indica se i due elementi multimediali sono identici.

## <a name="remarks"></a>Commenti

**IWMPMedia.isIdentical** è una proprietà in Visual Basic che accetta un parametro. In C# viene definito metodo **IWMPMedia.get \_ isIdentical.**

## <a name="examples"></a>Esempio

Nell'esempio seguente viene utilizzata la proprietà **isIdentical** (metodo **get \_ isIdentical** in C#) per verificare se un elemento multimediale denominato newMedia è uguale all'elemento multimediale corrente. Se non sono uguali, viene riprodotto il nuovo elemento multimediale. In caso contrario, il supporto corrente continua a essere riprodotto senza interruzioni. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
if (newMedia.get_isIdentical(player.currentMedia) != true)
{
    // Change the current media to the new media item.
    player.currentMedia = newMedia;

    // Play the new media item.
    player.Ctlcontrols.play();
}
```


```VB

If (newMedia.isIdentical(player.currentMedia) <> True) Then

    &#39; Change the current media to the new media item.
    player.currentMedia = newMedia

    &#39; Play the new media item.
    player.Ctlcontrols.play()

End If
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

 

 





