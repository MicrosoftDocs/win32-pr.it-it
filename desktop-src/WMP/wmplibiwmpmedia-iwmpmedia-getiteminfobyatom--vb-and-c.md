---
title: Metodo IWMPMedia getItemInfoByAtom
description: Il metodo getItemInfoByAtom restituisce il valore dell'attributo con il numero di indice specificato.
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- Metodo getItemInfoByAtom Windows Media Player
- Metodo getItemInfoByAtom Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, metodo getItemInfoByAtom
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfoByAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb37243960360120fbfe508a39db31e37728ac39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332403"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a>Metodo IWMPMedia:: getItemInfoByAtom

Il metodo **getItemInfoByAtom** restituisce il valore dell'attributo con il numero di indice specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String getItemInfoByAtom(
  System.Int32 lAtom
);
```


```VB

Public Function getItemInfoByAtom( _
  ByVal lAtom As System.Int32 _
) As System.String
Implements IWMPMedia.getItemInfoByAtom
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*latore* \[ in\]
</dt> <dd>

**System. Int32** che specifica l'indice in corrispondenza del quale si trova l'attributo richiesto all'interno del set di attributi disponibili.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. String** che rappresenta il valore dell'attributo.

## <a name="remarks"></a>Commenti

Questo metodo può essere utilizzato per recuperare i metadati per un elemento multimediale specifico utilizzando un numero di indice dell'attributo. È possibile utilizzare la proprietà **attributeCount** per determinare il numero di attributi disponibili per l'elemento multimediale.

Il metodo **getMediaAtom** dell'interfaccia **IWMPMediaCollection** può essere utilizzato anche per recuperare l'indice di un attributo specifico. Questa tecnica è in genere più efficiente rispetto ai metodi **GetItemInfo** o **getItemInfoByType** quando si lavora con playlist di grandi dimensioni.

Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB e C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. setItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection. getMediaAtom (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 





