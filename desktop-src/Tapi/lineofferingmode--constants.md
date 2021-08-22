---
description: Le costanti del flag di bit LINEOFFERINGMODE \_ (TAPI versioni 1.4 e successive) descrivono diversi sottostate di una chiamata di offerta.
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: LINEOFFERINGMODE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c2c36d18d006cdc1e2d9fc79095d58b6f56f1e58f4939c4e08ec6936af6855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518911"
---
# <a name="lineofferingmode_-constants"></a>Costanti LINEOFFERINGMODE \_

Le costanti del flag di bit **LINEOFFERINGMODE \_** (TAPI versioni 1.4 e successive) descrivono diversi sottostate di una chiamata di offerta. Una modalità è disponibile come stato della chiamata all'applicazione dopo lo stato della chiamata trdansitions all'offerta e all'interno del messaggio [**LINE \_ CALLSTATE**](line-callstate.md) che indica che la chiamata è in LINECALLSTATE \_ OFFERING. Questi valori vengono usati quando la chiamata si trova su un indirizzo condiviso (bridged) con altre stazioni (vedere [**Costanti LINEADDRESSSHARING), \_**](lineaddresssharing--constants.md)principalmente sistemi di chiave elettronica.

<dl> <dt>

<span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE \_ ACTIVE**
</dt> <dd> <dl> <dt>



Indica che la chiamata genera un avviso alla stazione corrente (sarà accompagnata da messaggi LINEDEVSTATE RINGING) e, se un'applicazione è impostata per rispondere automaticamente, può \_ farlo. Se la modalità di stato della chiamata è ZERO, l'applicazione deve presupporre che il valore sia attivo (che sarebbe la situazione in un indirizzo non con bridge). (TAPI versioni 1.4 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE \_ INATTIVO**
</dt> <dd> <dl> <dt>



Indica che la chiamata viene offerta in più di una stazione, ma la stazione corrente non sta inviando avvisi(ad esempio, potrebbe trattarsi di una stazione del guardiano in cui lo stato dell'offerta è consultivo, ad esempio lampeggiando una luce); Il software alla stazione impostata per la risposta automatica deve preferibilmente non rispondere alla chiamata, perché questa deve essere la prerogativa alla stazione primaria (avviso), ma è possibile usare [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) per connettere la chiamata. (TAPI versioni 1.4 e successive)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Non estendibile. Tutti i 32 bit sono riservati.

Per la compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata nella riga e non usare questi valori LINEOFFERINGMODE se non sono supportati nella versione \_ negoziata. Le applicazioni che non sono cognite di LINEOFFERINGMODE probabilmente presuppongono che una chiamata \_ in LINECALLSTATE OFFERING sia \_ in LINEOFFERINGMODE \_ ACTIVE.

I valori LINEOFFERINGMODE ACTIVE e LINEOFFERINGMODE INACTIVE vengono usati quando la chiamata si trova su un indirizzo condiviso con altre stazioni \_ \_ (bridged; vedere [Costanti LINEADDRESSSHARING), \_ ](lineaddresssharing--constants.md)principalmente sistemi di chiave elettronica. Se la modalità di stato della chiamata offerta è "attiva", significa che la chiamata genera un avviso alla stazione corrente (sarà accompagnata da messaggi LINEDEVSTATE RINGING) e se un'applicazione è impostata per rispondere automaticamente, può \_ farlo. Se la modalità di stato della chiamata è "inattiva", la chiamata viene offerta in più di una stazione, ma la stazione corrente non invia avvisi (ad esempio, potrebbe trattarsi di una stazione del guardiano in cui lo stato dell'offerta è consultivo, ad esempio lampeggiando una luce); Il software alla stazione impostata per la risposta automatica deve preferibilmente non rispondere alla chiamata, perché deve essere la prerogativa alla stazione primaria (avviso), ma è possibile usare [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) per connettere la chiamata. Se la modalità di stato della chiamata è ZERO, l'applicazione deve presupporre che il valore sia attivo (che sarebbe la situazione in un indirizzo non con bridge).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




