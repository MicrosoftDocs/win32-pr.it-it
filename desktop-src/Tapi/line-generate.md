---
description: Il messaggio di generazione della linea TAPI \_ viene inviato per notificare all'applicazione che la cifra corrente o la generazione di un tono è stata interrotta.
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: Messaggio di LINE_GENERATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916dc95d1a6343b0f8ebc0eef9e589b04aa2112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330743"
---
# <a name="line_generate-message"></a>\_Messaggio di generazione riga

Il messaggio **di \_ generazione della linea** TAPI viene inviato per notificare all'applicazione che la cifra corrente o la generazione di un tono è stata interrotta. Solo una di queste richieste di generazione può essere in corso una determinata chiamata in qualsiasi momento. Questo messaggio viene inviato anche quando viene annullata la generazione di numeri o toni.


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

Motivo per cui la generazione di numeri o toni è stata terminata. Questo parametro deve essere costituito solo da una delle [**\_ costanti LINEGENERATETERM**](linegenerateterm--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*dwParam3* 
</dt> <dd>

"Conteggio dei cicli" (numero di millisecondi dall'avvio di Windows) in corrispondenza del quale la cifra o la generazione del tono è stata completata. Per le versioni API precedenti alla 2,0, questo parametro è inutilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il **messaggio \_ di generazione riga** viene inviato solo all'applicazione che ha richiesto la generazione di numeri o toni.

Poiché è possibile che il timestamp specificato da *dwParam3* sia stato generato in un computer diverso da quello in cui è in esecuzione l'applicazione, è utile solo per il confronto con altri messaggi con timestamp analoghi generati sullo stesso dispositivo a linee ( [**linea \_ GATHERDIGITS**](line-gatherdigits.md), [**linea \_ MONITORDIGITS**](line-monitordigits.md), [**riga \_ MONITORMEDIA**](line-monitormedia.md), [**linea \_ MONITORTONE**](line-monitortone.md)), per determinare la tempistica relativa (separazione tra gli eventi). Il numero di cicli può essere "avvolto" dopo circa 49,7 giorni. Quando si eseguono calcoli, le applicazioni devono tenere conto di questo.

Se il provider di servizi non genera il timestamp (ad esempio, se è stato creato con una versione precedente di TAPI), TAPI fornisce un timestamp nel punto più vicino al provider di servizi che genera l'evento in modo che il timestamp sintetizzato sia il più accurato possibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEA \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> <dt>

[**LINEA \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LINEA \_ MONITORMEDIA**](line-monitormedia.md)
</dt> <dt>

[**LINEA \_ MONITORTONE**](line-monitortone.md)
</dt> </dl>

 

 




