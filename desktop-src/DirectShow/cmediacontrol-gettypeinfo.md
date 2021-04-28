---
description: "Metodo CMediaControl.GetTypeInfo: recupera un oggetto di informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia."
ms.assetid: 2014485f-d937-415d-a2fc-0c69269b5237
title: Metodo CMediaControl.GetTypeInfo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857dbdeee9a2add9ab77cae0ff97d69699d2dd2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099129"
---
# <a name="cmediacontrolgettypeinfo-method"></a>Metodo CMediaControl.GetTypeInfo

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

Informazioni sul tipo da restituire. Passare zero per recuperare le informazioni sul tipo per **l'implementazione di IDispatch.**

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

Restituisce un PUNTATORE E \_ se *pptinfo* non è valido. Restituisce TYPE \_ E \_ ELEMENTNOTFOUND se *itinfo* è diverso da zero. Restituisce S \_ OK se ha esito positivo. In caso contrario, **restituisce un HRESULT** da una delle chiamate per recuperare il tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaControl**](cmediacontrol.md)
</dt> </dl>

 

 




