---
description: Il messaggio della linea TAPI \_ GATHERDIGITS viene inviato quando la richiesta corrente di raccolta di cifre memorizzata nel buffer viene terminata o annullata. Il buffer delle cifre può essere esaminato dopo che il messaggio è stato ricevuto dall'applicazione.
ms.assetid: 0d27904d-9743-44bf-a7bc-132459351e01
title: Messaggio di LINE_GATHERDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0c67c5a9bbd3f798a8f4343b36c311309633ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327408"
---
# <a name="line_gatherdigits-message"></a>\_Messaggio linea GATHERDIGITS

Il messaggio della **linea TAPI \_ GATHERDIGITS** viene inviato quando la richiesta corrente di raccolta di cifre memorizzata nel buffer viene terminata o annullata. Il buffer delle cifre può essere esaminato dopo che il messaggio è stato ricevuto dall'applicazione.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle della chiamata.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Motivo per cui la raccolta di cifre è stata terminata. Questo parametro deve essere costituito solo da una delle [**\_ costanti LINEGATHERTERM**](linegatherterm--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*dwParam3* 
</dt> <dd>

"Conteggio dei cicli" (numero di millisecondi dall'avvio di Windows) in corrispondenza del quale è stata completata la raccolta delle cifre. Per le versioni TAPI precedenti alla 2,0, questo parametro è inutilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il messaggio di **riga \_ GATHERDIGITS** viene inviato all'applicazione che ha avviato la raccolta di cifre sulla chiamata usando [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).

Se la funzione [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) viene usata per annullare una richiesta precedente per la raccolta di cifre, TAPI invia un messaggio di **\_ GATHERDIGITS di riga** con *dwParam1* impostato su LINEGATHERTERM \_ Annulla per l'applicazione che indica che il buffer specificato in origine contiene le cifre raccolte fino all'annullamento.

Poiché è possibile che il timestamp specificato da *dwParam3* sia stato generato in un computer diverso da quello in cui è in esecuzione l'applicazione, è utile solo per il confronto con altri messaggi con timestamp analoghi generati sullo stesso dispositivo a linee ( [**riga \_ generazione**](line-generate.md), [**riga \_ MONITORDIGITS**](line-monitordigits.md), [**riga \_ MONITORMEDIA**](line-monitormedia.md), [**riga \_ MONITORTONE**](line-monitortone.md)), per determinare la tempistica relativa (separazione tra gli eventi). Il numero di cicli può essere "avvolto" dopo circa 49,7 giorni. Quando si eseguono calcoli, le applicazioni devono tenere conto di questo.

Se il provider di servizi non genera il timestamp (ad esempio, se è stato creato con una versione precedente di TAPI), TAPI fornisce un timestamp nel punto più vicino al provider di servizi che genera l'evento in modo che il timestamp sintetizzato sia il più accurato possibile.

> [!Note]  
> Quando un'applicazione richiama qualsiasi operazione asincrona che scrive i dati nella memoria dell'applicazione, l'applicazione deve mantenuta la memoria disponibile per la scrittura fino a quando non viene ricevuta una [**\_ risposta di riga**](line-reply.md) o un messaggio **\_ GATHERDIGITS** .

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_generazione riga**](line-generate.md)
</dt> <dt>

[**LINEA \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LINEA \_ MONITORMEDIA**](line-monitormedia.md)
</dt> <dt>

[**LINEA \_ MONITORTONE**](line-monitortone.md)
</dt> <dt>

[**\_risposta riga**](line-reply.md)
</dt> <dt>

[**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)
</dt> </dl>

 

 




