---
title: IWMPPlaylist. AttributeName (VB e C)
description: La proprietà AttributeName (il \_ metodo Get AttributeName in C \) ottiene il nome di un attributo della playlist specificato da un indice.
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- IWMPPlaylist. AttributeName (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeName (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 727d58a0cf875ed29efe9235448c1d597e81656a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324224"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a>IWMPPlaylist. AttributeName (VB e C#)

La proprietà **attributeName** (il metodo **get \_ attributeName** in C#) ottiene il nome di un attributo della playlist specificato da un indice.


```
[Visual Basic]
ReadOnly Property attributeName(
  lIndex As System.Int32
) As System.String
```




```
[C#]
System.String get_attributeName(
  System.Int32 lIndex
);
```



## <a name="parameters"></a>Parametri

*lIndex*

**System. Int32** che rappresenta l'indice dell'attributo playlist.

## <a name="return-value"></a>Valore restituito

**System. String** che rappresenta il nome dell'attributo playlist.

## <a name="remarks"></a>Commenti

**IWMPPlaylist. AttributeName** è una proprietà di sola lettura in Visual Basic che accetta un parametro, mentre in C# viene chiamato il metodo **IWMPPlaylist. Get \_ attributeName** .

Il numero di attributi associati a una playlist viene restituito dalla proprietà **IWMPPlaylist. attributeCount** .

Il nome restituito da questa proprietà può essere fornito ai metodi **setItemInfo** o **GetItemInfo** per specificare o recuperare un valore per l'attributo denominato.

Prima di utilizzare questa proprietà, è necessario disporre dell'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Per ulteriori informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).

## <a name="examples"></a>Esempio

Per il codice di esempio che usa questa proprietà, vedere la proprietà [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. attributeCount (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. getItemInfo (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. setItemInfo (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





