---
title: IWMPMedia. è identico (VB e C)
description: La proprietà IsValid (il metodo Get è \_ identico in C \) ottiene un valore che indica se l'elemento multimediale specificato è uguale a quello corrente.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- Windows Media Player IWMPMedia. è identico (VB e C)
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
ms.openlocfilehash: b3a488ad300362c1f8dccfd0fa6f6c7e4dee7676
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331390"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a>IWMPMedia. è identico (VB e C#)

La **proprietà IsValid (il** metodo **Get è \_ identico** in C#) ottiene un valore che indica se l'elemento multimediale specificato è uguale a quello corrente.


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

Interfaccia **wmplib. IWMPMedia** per l'elemento multimediale da confrontare con l'elemento multimediale corrente.

## <a name="property-value"></a>Valore della proprietà

Valore **System. Boolean** che indica se i due elementi multimediali sono identici.

## <a name="remarks"></a>Commenti

**IWMPMedia. is identico** è una proprietà in Visual Basic che accetta un parametro. In C# viene indicato come il metodo **IWMPMedia. Get è \_ identico** .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene utilizzata **la proprietà IsValid** ( **get \_ unidential** Method in C#) per verificare se un elemento multimediale denominato newMedia è uguale all'elemento multimediale corrente. Se non sono uguali, viene riprodotto il nuovo elemento multimediale. In caso contrario, i supporti correnti continueranno a essere riprodotti senza interruzioni. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





