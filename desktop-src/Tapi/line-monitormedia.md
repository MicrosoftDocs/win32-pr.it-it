---
description: Il messaggio LINE_MONITORMEDIA TAPI viene inviato quando viene rilevata una modifica nel tipo di supporto calls. L'invio di questo messaggio viene controllato con la funzione lineMonitorMedia
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: Messaggio di LINE_MONITORMEDIA (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b6e3d0d2928ab3256b844a27727657978dbe0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327785"
---
# <a name="line_monitormedia-message"></a>\_Messaggio linea MONITORMEDIA

Il messaggio **\_ MONITORMEDIA della linea** TAPI viene inviato quando viene rilevata una modifica nel tipo di supporto della chiamata. L'invio di questo messaggio viene controllato con la funzione [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) .


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

Nuovo tipo di supporto (o modalità). Questo parametro deve essere costituito solo da una delle [**\_ costanti LINEMEDIAMODE**](linemediamode--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Il "conteggio dei segni" (numero di millisecondi dall'avvio di Windows) in corrispondenza del quale è stato rilevato il supporto specificato. Per le versioni TAPI precedenti alla 2,0, questo parametro è inutilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il messaggio di **riga \_ MONITORMEDIA** viene inviato all'applicazione che ha abilitato il monitoraggio del supporto per il tipo di supporto rilevato.

Poiché questo timestamp potrebbe essere stato generato in un computer diverso da quello in cui l'applicazione è in esecuzione, è utile solo per il confronto con altri messaggi con timestamp analoghi generati sullo stesso dispositivo a linee ( [**linea \_ GATHERDIGITS**](line-gatherdigits.md), [**riga \_ generazione**](line-generate.md), [**riga \_ MONITORDIGITS**](line-monitordigits.md), [**riga \_ MONITORTONE**](line-monitortone.md)), per determinare la tempistica relativa (separazione tra gli eventi). Il numero di cicli può essere "avvolto" dopo circa 49,7 giorni. Quando si eseguono calcoli, le applicazioni devono tenere conto di questo.

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

[**LINEA \_ MONITORTONE**](line-monitortone.md)
</dt> </dl>

 

 




