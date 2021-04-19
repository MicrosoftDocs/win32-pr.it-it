---
description: Il messaggio della linea TAPI \_ MONITORTONE viene inviato quando viene rilevato un tono. L'invio di questo messaggio viene controllato con la funzione lineMonitorTones.
ms.assetid: ffdca615-5341-4f02-bb38-b8133cd9477d
title: Messaggio di LINE_MONITORTONE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de88863111dc0d00ea32953eeac76d4b570b5848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332690"
---
# <a name="line_monitortone-message"></a>\_Messaggio linea MONITORTONE

Il messaggio della **linea TAPI \_ MONITORTONE** viene inviato quando viene rilevato un tono. L'invio di questo messaggio viene controllato con la funzione [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) .


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

Membro **dwAppSpecific** specifico dell'applicazione della struttura [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) per il tono rilevato.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Il "conteggio dei segni" (numero di millisecondi dall'avvio di Windows) in corrispondenza del quale è stato rilevato il tono. Per le versioni API precedenti alla 2,0, questo parametro è inutilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il messaggio di **riga \_ MONITORTONE** viene inviato solo all'applicazione che ha richiesto il monitoraggio del tono.

Poiché questo timestamp potrebbe essere stato generato in un computer diverso da quello in cui l'applicazione è in esecuzione, è utile solo per il confronto con altri messaggi con timestamp analoghi generati sullo stesso dispositivo a linee ( [**linea \_ GATHERDIGITS**](line-gatherdigits.md), [**riga \_ generazione**](line-generate.md), [**riga \_ MONITORDIGITS**](line-monitordigits.md), **riga \_ MONITORTONE**), per determinare la tempistica relativa (separazione tra gli eventi). Il numero di cicli può essere "avvolto" dopo circa 49,7 giorni. Quando si eseguono calcoli, le applicazioni devono tenere conto di questo.

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

[**LINEA \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)
</dt> <dt>

[**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)
</dt> </dl>

 

 




