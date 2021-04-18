---
description: Fornisce l'accesso a proprietà e metodi esposti da un oggetto.
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: Metodo CMediaControl. Invoke (Ctlutil. h)
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
ms.openlocfilehash: 7b9a29d163180ffc609ca44f2bbbfb2870c5faef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328630"
---
# <a name="cmediacontrolinvoke-method"></a>Metodo CMediaControl. Invoke

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

Identificatore del membro. Usare [**CMediaControl:: GetIDsOfNames**](cmediacontrol-getidsofnames.md) o la documentazione dell'oggetto per ottenere l'identificatore di invio.

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

Flag che descrivono il contesto della `CMediaControl::Invoke` chiamata.

</dd> <dt>

*pDispParams* 
</dt> <dd>

Puntatore a una struttura contenente una matrice di argomenti, una matrice di ID di invio di argomenti per gli argomenti denominati e i conteggi per il numero di elementi nelle matrici.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Puntatore alla posizione in cui deve essere archiviato il risultato oppure **null** se il chiamante non prevede alcun risultato.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Puntatore a una struttura contenente informazioni sull'eccezione.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Puntatore all'indice del primo argomento, all'interno della matrice **rgvarg** della struttura **DISPPARAMS** , che contiene un errore. Per ulteriori informazioni su **DISPPARAMS**, vedere Platform SDK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce DISP \_ E \_ UNKNOWNINTERFACE se *riid* non è IID \_ null. Restituisce uno dei codici di errore di [**CMediaControl:: GetTypeInfo**](cmediacontrol-gettypeinfo.md) se la chiamata ha esito negativo. In caso contrario, restituisce il valore **HRESULT** dalla chiamata a **IDispatch:: Invoke**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaControl**](cmediacontrol.md)
</dt> </dl>

 

 




