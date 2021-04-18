---
description: Le \_ costanti del flag di bit LINEOFFERINGMODE (versioni TAPI 1,4 e successive) descrivono i diversi sottostati di una chiamata a un'offerta.
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: Costanti LINEOFFERINGMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9e04720b4ea79f5b169e4a279a3af2e0cdda39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331259"
---
# <a name="lineofferingmode_-constants"></a>\_Costanti LINEOFFERINGMODE

Le costanti del flag di bit **LINEOFFERINGMODE \_** (versioni TAPI 1,4 e successive) descrivono i diversi sottostati di una chiamata a un'offerta. Una modalità è disponibile come stato della chiamata all'applicazione dopo lo stato di chiamata trdansitions all'offerta e all'interno del messaggio di [**riga \_ CALLSTATE**](line-callstate.md) che indica che la chiamata è nell' \_ offerta LINECALLSTATE. Questi valori vengono usati quando la chiamata si trova su un indirizzo condiviso (con bridging) con altre stazioni (vedere [**\_ costanti LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente sistemi di chiave elettronica.

<dl> <dt>

<span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE \_ attivo**
</dt> <dd> <dl> <dt>



Indica che la chiamata sta inviando avvisi alla stazione corrente (sarà accompagnata da messaggi di chiamata LINEDEVSTATE \_ ) e, se un'applicazione è configurata in modo da rispondere automaticamente, questa operazione può essere eseguita. Se la modalità di stato della chiamata è pari a ZERO, è necessario che l'applicazione presupponga che il valore sia attivo (che corrisponderebbe alla situazione di un indirizzo non con bridging). (Versioni TAPI 1,4 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE \_ INattivo**
</dt> <dd> <dl> <dt>



Indica che la chiamata viene offerta in più di una stazione, ma che la stazione corrente non sta inviando avvisi (ad esempio, potrebbe trattarsi di una stazione di supervisore in cui lo stato dell'offerta è consultivo, ad esempio lampeggiando una luce); il software nella stazione impostata per la risposta automatica dovrebbe preferibilmente non rispondere alla chiamata, perché questo dovrebbe essere la prerogativa della stazione primaria (avviso), ma è possibile usare [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) per connettere la chiamata. (Versioni TAPI 1,4 e successive)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Non estendibile. Tutti i 32 bit sono riservati.

Per compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata sulla riga e non usare questi \_ valori LINEOFFERINGMODE se non sono supportati nella versione negoziata. Per le applicazioni che non sono consapevoli di LINEOFFERINGMODE \_ , probabilmente si presuppone che una chiamata nell' \_ offerta LINECALLSTATE sia in LINEOFFERINGMODE \_ Active.

I \_ valori inattivi di LINEOFFERINGMODE Active e LINEOFFERINGMODE \_ vengono usati quando la chiamata si trova in un indirizzo condiviso con altre stazioni (Bridged; vedere [ \_ costanti LINEADDRESSSHARING](lineaddresssharing--constants.md)), principalmente sistemi a chiave elettronica. Se la modalità di stato della chiamata dell'offerta è "attiva", significa che la chiamata sta inviando avvisi alla stazione corrente (sarà accompagnata da messaggi di LINEDEVSTATE \_ squillanti) e se un'applicazione è configurata in modo da rispondere automaticamente, questa operazione può essere eseguita. Se la modalità di stato della chiamata è "inattiva", la chiamata viene offerta in più di una stazione, ma la stazione corrente non sta inviando avvisi (ad esempio, potrebbe trattarsi di una stazione di supervisore in cui lo stato dell'offerta è consultivo, ad esempio lampeggiando una luce); il software nella stazione impostata per la risposta automatica dovrebbe preferibilmente non rispondere alla chiamata, perché questo dovrebbe essere la prerogativa della stazione primaria (avviso), ma è possibile usare [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) per connettere la chiamata. Se la modalità di stato della chiamata è pari a ZERO, è necessario che l'applicazione presupponga che il valore sia attivo (che corrisponderebbe alla situazione di un indirizzo non con bridging).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




