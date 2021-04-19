---
description: Recupera un oggetto informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia.
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: Metodo CMediaEvent. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e351d3b8b06bea4f6f9a1a160802972a8fa50f82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332335"
---
# <a name="cmediaeventgettypeinfo-method"></a>CMediaEvent. GetTypeInfo, metodo

Recupera un oggetto informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*itinfo* 
</dt> <dd>

Informazioni sul tipo da restituire. Passare zero per recuperare le informazioni sul tipo per l'implementazione di **IDispatch** .

</dd> <dt>

*lcid* 
</dt> <dd>

ID delle impostazioni locali per le informazioni sul tipo. Per le classi che supportano i nomi dei membri localizzati, un oggetto potrebbe essere in grado di restituire informazioni sul tipo diverse per le diverse lingue. Per le classi che non supportano i nomi dei membri localizzati, questo parametro può essere ignorato.

</dd> <dt>

*ppTInfo* 
</dt> <dd>

Indirizzo di un puntatore all'oggetto di informazioni sul tipo richiesto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un \_ puntatore E se *ppTInfo* non è valido. Restituisce il tipo \_ E \_ ELEMENTNOTFOUND se *itinfo* è diverso da zero. Restituisce \_ OK se ha esito positivo. In caso contrario, restituisce un valore **HRESULT** da una delle chiamate per recuperare il tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




