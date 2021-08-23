---
description: Il messaggio di LINE_MONITORMEDIA TAPI viene inviato quando viene rilevata una modifica nel tipo di supporto delle chiamate. L'invio di questo messaggio viene controllato con la funzione lineMonitorMedia
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: LINE_MONITORMEDIA messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fec42f0e8aa630b518f989a9237762edc71281767b281f7af78eb54210138d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519021"
---
# <a name="line_monitormedia-message"></a>MESSAGGIO LINE \_ MONITORMEDIA

Il messaggio TAPI **LINE \_ MONITORMEDIA** viene inviato quando viene rilevata una modifica nel tipo di supporto della chiamata. L'invio di questo messaggio viene controllato con la [**funzione lineMonitorMedia.**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia)


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

Nuovo tipo di supporto (o modalità). Questo parametro deve essere una sola delle costanti [**LINEMEDIAMODE \_**](linemediamode--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*dwParam3* 
</dt> <dd>

"tick count" (numero di millisecondi dall'Windows avviato) in cui è stato rilevato il supporto specificato. Per le versioni TAPI precedenti alla 2.0, questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il **messaggio LINE \_ MONITORMEDIA** viene inviato all'applicazione che ha abilitato il monitoraggio dei supporti per il tipo di supporto rilevato.

Poiché questo timestamp può essere stato generato in un computer diverso da quello in cui è in esecuzione l'applicazione, è utile solo per il confronto con altri messaggi con timestamp simili generati nello stesso dispositivo di linea ( [**LINE \_ GATHERDIGITS**](line-gatherdigits.md), [**LINE \_ GENERATE**](line-generate.md), [**LINE \_ MONITORDIGITS**](line-monitordigits.md), [**LINE \_ MONITORTONE**](line-monitortone.md)), per determinarne la temporizzazione relativa (separazione tra eventi). Il conteggio dei tick può essere "incapsulato" dopo circa 49,7 giorni; le applicazioni devono prendere in considerazione questo problema durante l'esecuzione dei calcoli.

Se il provider di servizi non genera il timestamp ( ad esempio, se è stato creato usando una versione precedente di TAPI), TAPI fornisce un timestamp nel punto più vicino al provider di servizi che genera l'evento in modo che il timestamp sintetizzato sia il più accurato possibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINE \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> <dt>

[**LINE \_ GENERATE**](line-generate.md)
</dt> <dt>

[**LINE \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LINE \_ MONITORTONE**](line-monitortone.md)
</dt> </dl>

 

 




