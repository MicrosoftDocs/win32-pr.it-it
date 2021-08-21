---
description: Il metodo Invoke fornisce l'accesso alle proprietà e ai metodi esposti dall'oggetto .
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: Metodo CMediaPosition.Invoke (Ctlutil.h)
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
ms.openlocfilehash: 6dac439b94a62e9dbd11ca9e12ab80023071fc00cf22abcf6b9b4b93b07c356c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156857"
---
# <a name="cmediapositioninvoke-method"></a>Metodo CMediaPosition.Invoke

Il `Invoke` metodo fornisce l'accesso alle proprietà e ai metodi esposti dall'oggetto .

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

Identificatore del membro. Usare [**CMediaPosition::GetIDsOfNames per**](cmediaposition-getidsofnames.md) ottenere l'identificatore dispatch.

</dd> <dt>

*Riid* 
</dt> <dd>

Riservato per utilizzi futuri. Deve essere IID \_ NULL.

</dd> <dt>

*lcid* 
</dt> <dd>

Contesto delle impostazioni locali in cui interpretare gli argomenti.

</dd> <dt>

*Wflags* 
</dt> <dd>

Flag che descrivono il contesto della chiamata.

</dd> <dt>

*pdispparams* 
</dt> <dd>

Puntatore a **una struttura DIPPARAMS** che contiene gli argomenti.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Puntatore a **un tipo VARIANT** che riceve il risultato oppure **NULL** se il chiamante non prevede alcun risultato.

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

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                              | Descrizione                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Operazione completata.<br/>                              |
| <dl> <dt>**DISP \_ E \_ UNKNOWNINTERFACE**</dt> </dl> | Il *parametro riid* non è IID \_ NULL<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




