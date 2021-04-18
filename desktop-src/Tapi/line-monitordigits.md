---
description: Il messaggio MONITORDIGITS della linea TAPI \_ viene inviato quando viene rilevata una cifra. L'invio di questo messaggio viene controllato con la funzione lineMonitorDigits.
ms.assetid: 1c1a729c-a6bb-4432-9617-4a892c76cb8d
title: Messaggio di LINE_MONITORDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6e85ed515d20c18c6e41cdb185b036312c54ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328426"
---
# <a name="line_monitordigits-message"></a>\_Messaggio linea MONITORDIGITS

Il messaggio **\_ MONITORDIGITS della linea** TAPI viene inviato quando viene rilevata una cifra. L'invio di questo messaggio viene controllato con la funzione [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) .


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

Istanza di callback fornita all'apertura della riga della chiamata.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Il byte di ordine inferiore contiene l'ultima cifra ricevuta in una rappresentazione di testo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Modalità di cifra rilevata. Questo parametro deve essere costituito solo da una delle [**\_ costanti LINEDIGITMODE**](linedigitmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Il "conteggio dei segni" (numero di millisecondi dall'avvio di Windows) in corrispondenza del quale è stata rilevata la cifra specificata. Per le versioni TAPI precedenti alla 2,0, questo parametro è inutilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il messaggio di **riga \_ MONITORDIGITS** viene inviato all'applicazione che ha abilitato il monitoraggio delle cifre.

Poiché questo timestamp potrebbe essere stato generato in un computer diverso da quello in cui l'applicazione è in esecuzione, è utile solo per il confronto con altri messaggi con timestamp analoghi generati sullo stesso dispositivo a linee ( [**linea \_ GATHERDIGITS**](line-gatherdigits.md), [**riga \_ generazione**](line-generate.md), [**riga \_ MONITORMEDIA**](line-monitormedia.md), [**riga \_ MONITORTONE**](line-monitortone.md)), per determinare la tempistica relativa (separazione tra gli eventi). Il numero di cicli può essere "avvolto" dopo circa 49,7 giorni. Quando si eseguono calcoli, le applicazioni devono tenere conto di questo.

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

[**\_generazione riga**](line-generate.md)
</dt> <dt>

[**LINEA \_ MONITORMEDIA**](line-monitormedia.md)
</dt> <dt>

[**LINEA \_ MONITORTONE**](line-monitortone.md)
</dt> <dt>

[**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)
</dt> </dl>

 

 




