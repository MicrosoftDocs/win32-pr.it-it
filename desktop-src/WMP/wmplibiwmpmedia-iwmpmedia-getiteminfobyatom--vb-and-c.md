---
title: Metodo IWMPMedia getItemInfoByAtom
description: Il metodo getItemInfoByAtom restituisce il valore dell'attributo con il numero di indice specificato.
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- Metodo getItemInfoByAtom Windows Media Player
- Metodo getItemInfoByAtom Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player metodo , getItemInfoByAtom
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
ms.openlocfilehash: 72a8820618b39418aa7be82faeef15a372e0e0f90c0db025e99c55be49d8c13e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115696"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a>Metodo IWMPMedia::getItemInfoByAtom

Il **metodo getItemInfoByAtom** restituisce il valore dell'attributo con il numero di indice specificato.

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

*lAtom* \[ Pollici\]
</dt> <dd>

Oggetto **System.Int32** che specifica l'indice in corrispondenza del quale si trova l'attributo richiesto all'interno del set di attributi disponibili.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto **System.String** che rappresenta il valore dell'attributo.

## <a name="remarks"></a>Commenti

Questo metodo può essere usato per recuperare i metadati per un elemento multimediale specifico usando un numero di indice dell'attributo. La **proprietà attributeCount** può essere usata per determinare il numero di attributi disponibili per l'elemento multimediale.

Il **metodo getMediaAtom** dell'interfaccia **IWMPMediaCollection** può essere usato anche per recuperare l'indice di un attributo specifico. Questa tecnica è in genere più efficiente dei **metodi getItemInfo** o **getItemInfoByType** quando si lavora con playlist di grandi dimensioni.

Prima di chiamare questo metodo, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.attributeCount (VB e C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.getItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.setItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getItemInfoByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection.getMediaAtom (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 





