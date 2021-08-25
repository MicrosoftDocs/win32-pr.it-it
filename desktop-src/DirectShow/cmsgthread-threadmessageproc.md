---
description: Elabora le richieste. Si tratta di una funzione membro virtuale pura.
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: Metodo CMsgThread.ThreadMessageProc (Msgthrd.h)
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
ms.openlocfilehash: cb11a7cac567bd645d0e3fd1c294636b5df9410fbc54012633ec0c0d161b43d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909701"
---
# <a name="cmsgthreadthreadmessageproc-method"></a>Metodo CMsgThread.ThreadMessageProc

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

*Umsg* 
</dt> <dd>

Richiedere il codice.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Parametro flag facoltativo da richiedere.

</dd> <dt>

*lpParam* 
</dt> <dd>

Puntatore facoltativo a dati aggiuntivi o a un blocco di dati restituiti.

</dd> <dt>

*Pevent* 
</dt> <dd>

Puntatore facoltativo a un oggetto evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Qualsiasi valore restituito diverso da zero causa la chiusura del thread. Restituisce zero a meno che una richiesta di uscita non sia stata elaborata di recente.

## <a name="remarks"></a>Commenti

Questa funzione virtuale pura deve essere sottoposta a override nella classe derivata. Verrà chiamato una volta per ogni richiesta accodata da una chiamata alla funzione membro [**CMsgThread::P utThreadMsg.**](cmsgthread-putthreadmsg.md)

La funzione membro definisce i quattro parametri. In genere, usare *il parametro uMsg* per indicare la richiesta e gli altri tre parametri saranno parametri aggiuntivi facoltativi. L'applicazione chiamante può fornire un puntatore a un [**oggetto CAMEvent**](camevent.md) nel *parametro pEvent* se richiesto dall'applicazione. È necessario impostare questo evento dopo l'elaborazione dell'evento usando un'espressione come:


```C++
pEvent->SetEvent
```



Un codice di richiesta deve essere accantonato per indicare l'uscita del thread di lavoro. Quando si riceve questa richiesta, restituire 1 da questa funzione membro. Restituisce 0 se non si vuole che il thread di lavoro si chieva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




