---
description: Elabora le richieste. Si tratta di una funzione membro virtuale pura.
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: Metodo CMsgThread. ThreadMessageProc (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ThreadMessageProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf47eb63a6f9d8fe4921985bb64567de6678b44c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330222"
---
# <a name="cmsgthreadthreadmessageproc-method"></a>CMsgThread. ThreadMessageProc, metodo

Elabora le richieste. Si tratta di una funzione membro virtuale pura.

## <a name="syntax"></a>Sintassi


```C++
virtual LRESULT ThreadMessageProc(
   UINT     uMsg,
   DWORD    dwFlags,
   LPVOID   lpParam,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uMsg* 
</dt> <dd>

Codice della richiesta.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Parametro facoltativo del flag da richiedere.

</dd> <dt>

*lpParam* 
</dt> <dd>

Puntatore facoltativo a dati aggiuntivi o a un blocco di dati restituito.

</dd> <dt>

*pEvent* 
</dt> <dd>

Puntatore facoltativo a un oggetto evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Qualsiasi valore restituito diverso da zero causa la chiusura del thread. Restituisce zero a meno che non sia stata elaborata di recente una richiesta di uscita.

## <a name="remarks"></a>Commenti

Questa funzione virtuale pura deve essere sottoposta a override nella classe derivata. Verrà chiamata una volta per ogni richiesta accodata da una chiamata alla funzione membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) .

La funzione membro definisce i quattro parametri. In genere, usare il parametro *uMsg* per indicare la richiesta e gli altri tre parametri saranno parametri aggiuntivi facoltativi. Se l'applicazione lo richiede, l'applicazione chiamante può fornire un puntatore a un oggetto [**CAMEvent**](camevent.md) nel parametro *pEvent* . È necessario impostare questo evento dopo l'elaborazione dell'evento usando un'espressione simile alla seguente:


```C++
pEvent->SetEvent
```



È necessario riservare un codice di richiesta per indicare al thread di lavoro di uscire. Al momento della ricezione della richiesta, restituire 1 da questa funzione membro. Restituisce 0 se non si desidera che il thread di lavoro venga chiuso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




