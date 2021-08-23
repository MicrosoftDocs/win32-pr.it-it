---
title: Metodo IWMPMediaCollection2 getPlaylistByQuery
description: Il metodo getPlaylistByQuery restituisce un'interfaccia IWMPPlaylist che fornisce l'accesso agli elementi multimediali che soddisfano le condizioni della query.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- Metodo getPlaylistByQuery Windows Media Player
- Metodo getPlaylistByQuery Windows Media Player, interfaccia IWMPMediaCollection2
- Interfaccia IWMPMediaCollection2 Windows Media Player metodo , getPlaylistByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getPlaylistByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd80467c78aac832c5ac2784281abcf07975a1956ee304c734b2b45b82901fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053579"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a>Metodo IWMPMediaCollection2::getPlaylistByQuery

Il `getPlaylistByQuery` metodo restituisce **un'interfaccia IWMPPlaylist** che fornisce l'accesso agli elementi multimediali che soddisfano le condizioni della query.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylist getPlaylistByQuery(
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getPlaylistByQuery( _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getPlaylistByQuery
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*pQuery* \[ Pollici\]
</dt> <dd>

Interfaccia **WMPLib.IWMPQuery** che rappresenta la query.

</dd> <dt>

*bstrMediaType* \[ Pollici\]
</dt> <dd>

**System.String che** rappresenta il tipo di supporto. Deve contenere uno dei valori seguenti: "audio", "video", "photo", "playlist" o "other".

</dd> <dt>

*bstrSortAttribute* \[ Pollici\]
</dt> <dd>

**System.String che è il** nome dell'attributo usato per l'ordinamento. Una stringa di lunghezza zero ("") indica che non viene applicato alcun ordinamento.

</dd> <dt>

*fSortAscending* \[ Pollici\]
</dt> <dd>

Valore **System.Boolean** che indica se la playlist deve essere ordinata in ordine crescente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **WMPLib.IWMPPlaylist** per la playlist recuperata.

## <a name="remarks"></a>Commenti

Le query composte che usano **IWMPQuery non** supportano la distinzione tra maiuscole e minuscole.

Quando la query composta specificata dal *parametro pQuery* contiene una condizione compilata in base all'attributo **MediaType,** tale condizione viene ignorata. Il valore per il *parametro bstrMediaType* viene sempre usato. Ad esempio, se la query composta contiene la condizione "MediaType Equals audio" e il valore per il *parametro bstrMediaType* è "video", la playlist risultante conterrà solo elementi video.

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

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPQuery (VB e C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Attributo MediaType**](mediatype-attribute.md)
</dt> </dl>

 

 





