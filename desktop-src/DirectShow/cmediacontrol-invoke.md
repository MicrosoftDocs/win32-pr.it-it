---
description: "Metodo CMediaControl.Invoke: fornisce l'accesso alle proprietà e ai metodi esposti da un oggetto."
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: Metodo CMediaControl.Invoke (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe077b2c69f603eef8737cbf7ea8c514e9b90c85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085639"
---
# <a name="cmediacontrolinvoke-method"></a>Metodo CMediaControl.Invoke

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

Identificatore del membro. Usare [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md) o la documentazione dell'oggetto per ottenere l'identificatore di invio.

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

Flag che descrivono il contesto della `CMediaControl::Invoke` chiamata.

</dd> <dt>

*pdispparams* 
</dt> <dd>

Puntatore a una struttura contenente una matrice di argomenti, una matrice di ID dispatch di argomenti per argomenti denominati e conteggi per il numero di elementi nelle matrici.

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

Puntatore all'indice del primo argomento, all'interno della matrice **rgvarg** della struttura **DISPPARAMS,** che contiene un errore. Per altre informazioni su **DISPPARAMS,** vedere Platform SDK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce DISP \_ E \_ UNKNOWNINTERFACE se *riid* non è IID \_ NULL. Restituisce uno dei codici di errore da [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md) se la chiamata non riesce. In caso contrario, **restituisce il valore HRESULT** dalla chiamata a **IDispatch::Invoke.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaControl**](cmediacontrol.md)
</dt> </dl>

 

 




