---
title: Metodo IWMPMediaCollection getMediaAtom
description: Il metodo getMediaAtom restituisce l'indice di un attributo specificato all'interno del set di attributi disponibili.
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- Metodo getMediaAtom Windows Media Player
- Metodo getMediaAtom Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player, metodo getMediaAtom
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08487cf60c351ff4f8e0741209655cb78c30c3f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333404"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a>Metodo IWMPMediaCollection:: getMediaAtom

Il `getMediaAtom` metodo restituisce l'indice di un attributo specificato all'interno del set di attributi disponibili.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrItemName* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome dell'elemento per il quale recuperare l'indice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. Int32** che rappresenta l'indice.

## <a name="remarks"></a>Commenti

Il numero di indice recuperato con questo metodo può essere passato a **IWMPMedia. getItemInfoByAtom** per accedere ai valori di attributo. Questa tecnica è in genere più efficiente quando si lavora con playlist di grandi dimensioni rispetto all'accesso a un valore di attributo in base al nome tramite **IWMPMedia. GetItemInfo**.

Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMPMedia. getItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfoByAtom (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





