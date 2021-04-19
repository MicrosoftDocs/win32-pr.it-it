---
title: Metodo IWMPMediaCollection2 getStringCollectionByQuery
description: Il metodo getStringCollectionByQuery restituisce un'interfaccia IWMPStringCollection che fornisce l'accesso al set di tutti i valori stringa per un attributo specificato che soddisfano le condizioni della query.
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- Metodo getStringCollectionByQuery Windows Media Player
- Metodo getStringCollectionByQuery Windows Media Player, interfaccia IWMPMediaCollection2
- Interfaccia IWMPMediaCollection2 Windows Media Player, metodo getStringCollectionByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getStringCollectionByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322781bc9ddec3e6f8d74d7229f16ce38e519f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329063"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a>Metodo IWMPMediaCollection2:: getStringCollectionByQuery

Il `getStringCollectionByQuery` metodo restituisce un'interfaccia **IWMPStringCollection** che consente di accedere al set di tutti i valori stringa per un attributo specificato che soddisfano le condizioni della query.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPStringCollection getStringCollectionByQuery(
  System.String bstrAttribute,
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getStringCollectionByQuery( _
  ByVal bstrAttribute As System.String, _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPStringCollection
Implements IWMPMediaCollection2.getStringCollectionByQuery
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrAttribute* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome dell'attributo.

</dd> <dt>

*pQuery* \[ in\]
</dt> <dd>

Interfaccia **wmplib. IWMPQuery** che rappresenta la query che definisce le condizioni utilizzate per recuperare la raccolta di stringhe.

</dd> <dt>

*bstrMediaType* \[ in\]
</dt> <dd>

**System. String** che rappresenta il tipo di supporto. Deve contenere uno dei valori seguenti: "audio", "video", "Photo", "playlist" o "other".

</dd> <dt>

*bstrSortAttribute* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome dell'attributo utilizzato per l'ordinamento. Una stringa di lunghezza zero ("") indica che non viene applicato alcun ordinamento.

</dd> <dt>

*fSortAscending* \[ in\]
</dt> <dd>

Valore **System. Boolean** che indica se il set di valori di stringa deve essere ordinato in ordine crescente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **wmplib. IWMPStringCollection** per il set recuperato di valori stringa.

## <a name="remarks"></a>Commenti

Le query composte con **IWMPQuery** non fanno distinzione tra maiuscole e minuscole

Quando la query composta specificata dal parametro *pQuery* contiene una condizione compilata sull'attributo **mediaType** , tale condizione viene ignorata. Viene sempre usato il valore per il parametro *bstrMediaType* . Se, ad esempio, la query composta contiene la condizione "MediaType Equals audio" e il valore per il parametro *bstrMediaType* è "video", la playlist risultante conterrà solo elementi video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMediaCollection2 (VB e C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPQuery (VB e C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPStringCollection (VB e C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**Attributo MediaType**](mediatype-attribute.md)
</dt> </dl>

 

 





