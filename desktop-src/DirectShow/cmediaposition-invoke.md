---
description: Il metodo Invoke fornisce l'accesso alle proprietà e ai metodi esposti dall'oggetto.
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: Metodo CMediaPosition. Invoke (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3955848bf2a87e0983ddd7dc3bef48f157ae6648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332330"
---
# <a name="cmediapositioninvoke-method"></a>Metodo CMediaPosition. Invoke

Il `Invoke` metodo fornisce l'accesso alle proprietà e ai metodi esposti dall'oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dispidMember* 
</dt> <dd>

Identificatore del membro. Usare [**CMediaPosition:: GetIDsOfNames**](cmediaposition-getidsofnames.md) per ottenere l'identificatore dispatch.

</dd> <dt>

*riid* 
</dt> <dd>

Riservato per utilizzi futuri. Deve essere un IID \_ null.

</dd> <dt>

*lcid* 
</dt> <dd>

Contesto delle impostazioni locali in cui interpretare gli argomenti.

</dd> <dt>

*wFlags* 
</dt> <dd>

Flag che descrivono il contesto della chiamata.

</dd> <dt>

*pDispParams* 
</dt> <dd>

Puntatore a una struttura **DIPPARAMS** contenente gli argomenti.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Puntatore a un **Variant** che riceve il risultato oppure **null** se il chiamante non prevede alcun risultato.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Puntatore a una struttura che riceve informazioni sull'eccezione.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Puntatore a una variabile che riceve l'indice del primo argomento che causa un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                              | Descrizione                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                     | Esito positivo.<br/>                              |
| <dl> <dt>**DISP \_ E \_ UNKNOWNINTERFACE**</dt> </dl> | Il parametro *riid* non è IID \_ null<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




