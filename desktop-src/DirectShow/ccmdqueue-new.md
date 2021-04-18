---
description: Il nuovo metodo inizializza un comando da eseguire e restituisce un nuovo oggetto CDeferredCommand.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: Metodo CCmdQueue. New (Winutil. h)
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
ms.openlocfilehash: 58c3aee63005010b9ed7366cfb63a69fcc7348b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324474"
---
# <a name="ccmdqueuenew-method"></a>CCmdQueue. New, metodo

Il `New` Metodo Inizializza un comando da eseguire e restituisce un nuovo oggetto [**CDeferredCommand**](cdeferredcommand.md) .

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

Indirizzo di un puntatore a un oggetto [**CDeferredCommand**](cdeferredcommand.md) tramite il quale un'applicazione può annullare il comando, impostare una nuova ora di presentazione per esso oppure recuperare le informazioni relative alla stima.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntatore all'oggetto che eseguirà il comando.

</dd> <dt>

*time* 
</dt> <dd>

Ora in cui eseguire il comando o i comandi in coda.

</dd> <dt>

*IID* 
</dt> <dd>

Puntatore all'identificatore univoco globale (**GUID**) dell'interfaccia da chiamare.

</dd> <dt>

*dispidMethod* 
</dt> <dd>

Metodo sull'interfaccia da chiamare.

</dd> <dt>

*wFlags* 
</dt> <dd>

Flag che descrivono il contesto della chiamata. Questo parametro supporta gli stessi flag del metodo **IDispatch:: Invoke** .

</dd> <dt>

*cArgs* 
</dt> <dd>

Numero di argomenti passati.

</dd> <dt>

*pDispParams* 
</dt> <dd>

Puntatore all'elenco di tipi Variant associati ai parametri di invio.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Puntatore all'elenco in cui devono essere restituiti i risultati, se presenti.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Puntatore all'indice all'interno dell'elenco di parametri *pDispParams* in cui si è verificato l'ultimo errore.

</dd> <dt>

*bStream* 
</dt> <dd>

Valore che indica se il parametro di *ora* è un valore in fase di flusso (**true**) o un valore della fase di presentazione (**false**).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo. Restituisce E \_ OutOfMemory se *ppCmd* restituisce un valore **null** per la creazione del nuovo oggetto [**CDeferredCommand**](cdeferredcommand.md) . In caso contrario, restituisce un valore **HRESULT** che indica un errore durante il tentativo di creazione di un nuovo oggetto **CDeferredCommand** . Se si verifica un errore, nessun oggetto è stato accodato.

## <a name="remarks"></a>Commenti

Il nuovo oggetto [**CDeferredCommand**](cdeferredcommand.md) verrà inizializzato con i parametri e verrà aggiunto alla coda durante la costruzione. Questo metodo è simile al metodo **IDispatch:: Invoke** .

I valori per il parametro *wFlags* sono i seguenti:



| Valore                    | Descrizione                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_metodo Dispatch         | Il membro viene eseguito come metodo. Se una proprietà ha lo stesso nome, è possibile impostare sia questo che il \_ flag PropertyGet (di invio.                                       |
| \_PROPERTYGET (dispatch    | Il membro viene recuperato come una proprietà o un membro dati.                                                                                                          |
| \_PROPERTYPUT dispatch    | Il membro viene modificato come una proprietà o un membro dati.                                                                                                            |
| \_PROPERTYPUTREF dispatch | Il membro viene modificato tramite un'assegnazione di riferimento, anziché un'assegnazione di valore. Questo valore è valido solo quando la proprietà accetta un riferimento a un oggetto. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




