---
title: Metodo IWMPMediaCollection2 getPlaylistByQuery
description: Il metodo getPlaylistByQuery restituisce un'interfaccia IWMPPlaylist che fornisce l'accesso agli elementi multimediali che soddisfano le condizioni della query.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- Metodo getPlaylistByQuery Windows Media Player
- Metodo getPlaylistByQuery Windows Media Player, interfaccia IWMPMediaCollection2
- Interfaccia IWMPMediaCollection2 Windows Media Player, metodo getPlaylistByQuery
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
ms.openlocfilehash: 109f6e49e77d1cfa8c6d3b45bef1d011faf21a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329064"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a>Metodo IWMPMediaCollection2:: getPlaylistByQuery

Il `getPlaylistByQuery` metodo restituisce un'interfaccia **IWMPPlaylist** che consente di accedere agli elementi multimediali che corrispondono alle condizioni della query.

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

*pQuery* \[ in\]
</dt> <dd>

Interfaccia **wmplib. IWMPQuery** che rappresenta la query.

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

Valore **System. Boolean** che indica se la playlist deve essere ordinata in ordine crescente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **wmplib. IWMPPlaylist** per la playlist recuperata.

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

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPQuery (VB e C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Attributo MediaType**](mediatype-attribute.md)
</dt> </dl>

 

 





