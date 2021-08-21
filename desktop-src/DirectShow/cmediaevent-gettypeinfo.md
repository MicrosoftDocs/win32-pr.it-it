---
description: "Metodo CMediaEvent.GetTypeInfo: recupera un oggetto di informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia."
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: Metodo CMediaEvent.GetTypeInfo (Ctlutil.h)
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
ms.openlocfilehash: 3ef3f84cce1bad88b0f1103be3584ff350afac0fd7047b5a75a5fb473a4bedcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156989"
---
# <a name="cmediaeventgettypeinfo-method"></a>Metodo CMediaEvent.GetTypeInfo

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

Digitare le informazioni da restituire. Passare zero per recuperare le informazioni sul tipo per **l'implementazione di IDispatch.**

</dd> <dt>

*lcid* 
</dt> <dd>

ID delle impostazioni locali per le informazioni sul tipo. Per le classi che supportano nomi di membri localizzati, un oggetto potrebbe essere in grado di restituire informazioni sul tipo diverse per lingue diverse. Per le classi che non supportano nomi di membri localizzati, questo parametro può essere ignorato.

</dd> <dt>

*pptinfo* 
</dt> <dd>

Indirizzo di un puntatore all'oggetto informazioni sul tipo richiesto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore E \_ se *pptinfo* non è valido. Restituisce TYPE \_ E \_ ELEMENTNOTFOUND se *itinfo* è diverso da zero. Restituisce S \_ OK se ha esito positivo. In caso contrario, restituisce **un HRESULT** da una delle chiamate per recuperare il tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




