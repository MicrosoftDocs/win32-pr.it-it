---
description: Metodo del costruttore.
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: Costruttore CDeferredCommand. CDeferredCommand (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.CDeferredCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e92a2ffc5129ee38fc5061b28ea7ffef49da0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333483"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a>Costruttore CDeferredCommand. CDeferredCommand

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CDeferredCommand(
   CCmdQueue *pQ,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   LPUNKNOWN pUnkExecutor,
   REFTIME   time,
   GUID      *iid,
   long      dispidMethod,
   short     wFlags,
   long      cArgs,
   VARIANT   *pDispParams,
   VARIANT   *pvarResult,
   short     *puArgErr,
   BOOL      bStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pQ* 
</dt> <dd>

Puntatore a un oggetto che espone l'interfaccia [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) .

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown** esterna per l'aggregazione.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a un valore **HRESULT** restituito.

</dd> <dt>

*pUnkExecutor* 
</dt> <dd>

Puntatore all'oggetto che effettuerà questo comando.

</dd> <dt>

*time* 
</dt> <dd>

Ora in cui verrà eseguito il comando.

</dd> <dt>

*IID* 
</dt> <dd>

Puntatore all'identificatore univoco globale (**GUID**) dell'interfaccia che contiene il metodo.

</dd> <dt>

*dispidMethod* 
</dt> <dd>

Metodo sull'interfaccia da chiamare.

</dd> <dt>

*wFlags* 
</dt> <dd>

Contesto della chiamata.

</dd> <dt>

*cArgs* 
</dt> <dd>

Numero di argomenti passati.

</dd> <dt>

*pDispParams* 
</dt> <dd>

Puntatore a un elenco di tipi Variant di argomento.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Puntatore a un elenco di tipi Variant restituito, se presente.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Puntatore all'ultimo argomento nell'elenco di parametri *pDispParams* con un errore.

</dd> <dt>

*bStream* 
</dt> <dd>

Valore che indica se l'ora del comando rinviata è in tempo di flusso (**true**) o ora di presentazione (**false**).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




