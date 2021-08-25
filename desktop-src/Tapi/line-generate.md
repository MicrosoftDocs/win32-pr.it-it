---
description: Il messaggio TAPI LINE GENERATE viene inviato per notificare all'applicazione che la generazione della cifra o del tono \_ corrente è terminata.
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: LINE_GENERATE messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3ab0d503d7515fec2cdbd1676eed235cced88e2adfa9fcc1dd354663929e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774241"
---
# <a name="line_generate-message"></a>MESSAGGIO LINE \_ GENERATE

Il messaggio TAPI **LINE \_ GENERATE viene** inviato per notificare all'applicazione che la generazione della cifra o del tono corrente è terminata. È possibile che sia in corso una sola richiesta di generazione di questo tipo in una determinata chiamata in qualsiasi momento. Questo messaggio viene inviato anche quando la generazione di numeri o toni viene annullata.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle per la chiamata.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Motivo per cui la generazione di numeri o toni è stata terminata. Questo parametro deve essere una sola delle costanti [**LINEGENERATETERM \_**](linegenerateterm--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Il "numero di tick" (numero di millisecondi dall'Windows avviata) in corrispondenza del quale è stata completata la generazione della cifra o del tono. Per le versioni dell'API precedenti alla 2.0, questo parametro non è usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il **messaggio LINE \_ GENERATE** viene inviato solo all'applicazione che ha richiesto la generazione della cifra o del tono.

Poiché il timestamp specificato da *dwParam3* può essere stato generato in un computer diverso da quello in cui è in esecuzione l'applicazione, è utile solo per il confronto con altri messaggi con timestamp simili generati sullo stesso dispositivo di riga ( [**LINE \_ GATHERDIGITS**](line-gatherdigits.md), [**LINE \_ MONITORDIGITS**](line-monitordigits.md), [**LINE \_ MONITORMEDIA**](line-monitormedia.md), [**LINE \_ MONITORTONE**](line-monitortone.md)), per determinare la relativa temporizzazione (separazione tra gli eventi). Il conteggio dei tick può essere "incapsulato" dopo circa 49,7 giorni; le applicazioni devono prendere in considerazione questo tipo di dati durante l'esecuzione di calcoli.

Se il provider di servizi non genera il timestamp (ad esempio, se è stato creato usando una versione precedente di TAPI), TAPI fornisce un timestamp nel punto più vicino al provider di servizi che genera l'evento in modo che il timestamp sintetizzato sia il più accurato possibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINE \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> <dt>

[**LINE \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LINE \_ MONITORMEDIA**](line-monitormedia.md)
</dt> <dt>

[**LINE \_ MONITORTONE**](line-monitortone.md)
</dt> </dl>

 

 




