---
description: "Metodo CMediaEvent.Invoke: fornisce l'accesso alle proprietà e ai metodi esposti da un oggetto."
ms.assetid: 2b091b57-0855-489a-9a33-cfc75f63ad07
title: Metodo CMediaEvent.Invoke (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37fadefe3163ed4211b8112ec17cc1cfb3fb3625b4aba207db06a25de3e27b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655225"
---
# <a name="cmediaeventinvoke-method"></a>Metodo CMediaEvent.Invoke

Fornisce l'accesso a proprietà e metodi esposti da un oggetto.

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

Identificatore del membro. Usare [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md) o la documentazione dell'oggetto per ottenere l'identificatore dispatch.

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

Flag che descrivono il contesto della `CMediaEvent::Invoke` chiamata.

</dd> <dt>

*pdispparams* 
</dt> <dd>

Puntatore a una struttura contenente una matrice di argomenti, una matrice di ID di invio di argomenti per argomenti denominati e conteggi per il numero di elementi nelle matrici.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Puntatore alla posizione in cui deve essere archiviato il risultato oppure **NULL** se il chiamante non prevede alcun risultato.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Puntatore a una struttura contenente informazioni sull'eccezione.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Puntatore all'indice del primo argomento, all'interno della matrice **rgvarg** della struttura **DISPPARAMS,** che presenta un errore. Per altre informazioni su **DISPPARAMS,** vedere Platform SDK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce DISP \_ E \_ UNKNOWNINTERFACE se *riid* non è IID \_ NULL. Restituisce uno dei codici di errore da [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md) se la chiamata ha esito negativo. In caso contrario, restituisce **HRESULT** dalla chiamata a **IDispatch::Invoke**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




