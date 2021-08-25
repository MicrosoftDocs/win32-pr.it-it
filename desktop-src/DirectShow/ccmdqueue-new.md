---
description: Il metodo New inizializza un comando da eseguire e restituisce un nuovo oggetto CDeferredCommand.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: Metodo CCmdQueue.New (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.New
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b6ad22b67df863e699649f22f513a98ca1306751a1d449a683f306c9cc2938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910391"
---
# <a name="ccmdqueuenew-method"></a>Metodo CCmdQueue.New

Il `New` metodo inizializza un comando da eseguire e restituisce un nuovo oggetto [**CDeferredCommand.**](cdeferredcommand.md)

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT New(
   CDeferredCommand **ppCmd,
   LPUNKNOWN        pUnk,
   REFTIME          time,
   GUID             *iid,
   long             dispidMethod,
   short            wFlags,
   long             cArgs,
   VARIANT          *pDispParams,
   VARIANT          *pvarResult,
   short            *puArgErr,
   BOOL             bStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppCmd* 
</dt> <dd>

Indirizzo di un puntatore a un [**oggetto CDeferredCommand**](cdeferredcommand.md) tramite il quale un'applicazione può annullare il comando, impostare una nuova ora di presentazione o recuperare informazioni sulla stima.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore all'oggetto che eseguirà il comando.

</dd> <dt>

*time* 
</dt> <dd>

Ora in cui eseguire il comando o i comandi in coda.

</dd> <dt>

*Iid* 
</dt> <dd>

Puntatore all'identificatore univoco globale **(GUID)** dell'interfaccia da chiamare.

</dd> <dt>

*dispidMethod* 
</dt> <dd>

Metodo sull'interfaccia da chiamare.

</dd> <dt>

*Wflags* 
</dt> <dd>

Flag che descrivono il contesto della chiamata. Questo parametro supporta gli stessi flag del **metodo IDispatch::Invoke.**

</dd> <dt>

*cArgs* 
</dt> <dd>

Numero di argomenti passati.

</dd> <dt>

*pDispParams* 
</dt> <dd>

Puntatore all'elenco di tipi variant associati ai parametri dispatch.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Puntatore all'elenco in cui devono essere restituiti i risultati, se presenti.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Puntatore all'indice all'interno *dell'elenco di parametri pDispParams* in cui si è verificato l'ultimo errore.

</dd> <dt>

*bStream* 
</dt> <dd>

Valore che indica se il *parametro time* è un valore stream-time (**TRUE**) o un valore dell'ora di presentazione (**FALSE**).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo. Restituisce E \_ OUTOFMEMORY se *ppCmd* restituisce dalla creazione del nuovo oggetto [**CDeferredCommand**](cdeferredcommand.md) con valore **NULL.** In caso contrario, restituisce **un HRESULT** che indica un errore durante il tentativo di creare un nuovo **oggetto CDeferredCommand.** Se si verifica un errore, nessun oggetto è stato accodato.

## <a name="remarks"></a>Commenti

Il nuovo [**oggetto CDeferredCommand**](cdeferredcommand.md) verrà inizializzato con i parametri e verrà aggiunto alla coda durante la costruzione. Questo metodo è simile al **metodo IDispatch::Invoke.**

I valori per *il parametro wFlags* includono quanto segue:



| Valore                    | Descrizione                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| METODO \_ DISPATCH         | Il membro viene eseguito come metodo. Se una proprietà ha lo stesso nome, è possibile impostare sia questo che il flag DISPATCH \_ PROPERTYGET.                                       |
| DISPATCH \_ PROPERTYGET    | Il membro viene recuperato come proprietà o membro dati.                                                                                                          |
| PROPRIETÀ \_ DISPATCHPUT    | Il membro viene modificato come proprietà o membro dati.                                                                                                            |
| DISPATCH \_ PROPERTYPUTREF | Il membro viene modificato tramite un'assegnazione di riferimento, anziché un'assegnazione di valore. Questo valore è valido solo quando la proprietà accetta un riferimento a un oggetto . |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




