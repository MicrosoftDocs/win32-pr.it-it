---
title: Stili del controllo Selezione data e ora (CommCtrl.h)
description: Gli stili della finestra elencati di seguito sono specifici dei controlli selezione data e ora.
ms.assetid: d3b95521-75ef-4cca-b801-94c6f749aa47
topic_type:
- apiref
api_name:
- DTS_APPCANPARSE
- DTS_LONGDATEFORMAT
- DTS_RIGHTALIGN
- DTS_SHOWNONE
- DTS_SHORTDATEFORMAT
- DTS_SHORTDATECENTURYFORMAT
- DTS_TIMEFORMAT
- DTS_UPDOWN
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f9740e0de413649b67cc8231d31425d212d2571dbc9a1b703f9f95c35e4981
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085761"
---
# <a name="date-and-time-picker-control-styles"></a>Stili del controllo Selezione data e ora

Gli stili della finestra elencati di seguito sono specifici dei controlli selezione data e ora.



| Costante                                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DTS_APPCANPARSE"></span><span id="dts_appcanparse"></span><dl> <dt>**DTS \_ APPCANPARSE**</dt> </dl>                                  | Consente al proprietario di analizzare l'input dell'utente ed eseguire le azioni necessarie. Consente agli utenti di modificare all'interno dell'area client del controllo quando premono il tasto F2. Il controllo invia [codici di notifica DTN \_ USERSTRING](dtn-userstring.md) al termine dell'operazione.<br/>                                                                                                                                                                                                                                                                    |
| <span id="DTS_LONGDATEFORMAT"></span><span id="dts_longdateformat"></span><dl> <dt>**DTS \_ LONGDATEFORMAT**</dt> </dl>                         | Visualizza la data in formato lungo. La stringa di formato predefinita per questo stile è definita da LOCALE SLONGDATEFORMAT, che produce output come \_ "Friday, April 19, 1996". Quando si usa questo stile, il pulsante a discesa non visualizza un'icona.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="DTS_RIGHTALIGN"></span><span id="dts_rightalign"></span><dl> <dt>**DTS \_ RIGHTALIGN**</dt> </dl>                                     | Il calendario mensile a discesa verrà allineato a destra con il controllo anziché a sinistra, che è l'impostazione predefinita. <br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHOWNONE"></span><span id="dts_shownone"></span><dl> <dt>**DTS \_ SHOWNONE**</dt> </dl>                                           | È possibile che nel controllo non sia attualmente selezionata alcuna data. Con questo stile, il controllo visualizza una casella di controllo che viene selezionata automaticamente ogni volta che viene selezionata o immessa una data. Se la casella di controllo viene successivamente deselezionata, l'applicazione non può recuperare la data dal controllo perché, in sostanza, il controllo non ha alcuna data. Lo stato della casella di controllo può essere impostato con il messaggio [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) o sottoposto a query con il [**messaggio DTM \_ GETSYSTEMTIME.**](dtm-getsystemtime.md)<br/> |
| <span id="DTS_SHORTDATEFORMAT"></span><span id="dts_shortdateformat"></span><dl> <dt>**DTS \_ SHORTDATEFORMAT**</dt> </dl>                      | Visualizza la data in formato breve. La stringa di formato predefinita per questo stile è definita da LOCALE SSHORTDATE, che genera un output come \_ "4/19/96".<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHORTDATECENTURYFORMAT"></span><span id="dts_shortdatecenturyformat"></span><dl> <dt>**DTS \_ SHORTDATECENTURYFORMAT**</dt> </dl> | **Versione 5.80.** Simile allo stile **\_ SHORTDATEFORMAT DTS,** ad eccezione del fatto che l'anno è un campo a quattro cifre. La stringa di formato predefinita per questo stile è basata su LOCALE \_ SSHORTDATE. L'output è simile al seguente: "4/19/1996".<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="DTS_TIMEFORMAT"></span><span id="dts_timeformat"></span><dl> <dt>**DTS \_ TIMEFORMAT**</dt> </dl>                                     | Visualizza l'ora. La stringa di formato predefinita per questo stile è definita da LOCALE STIMEFORMAT, che produce output come \_ "5:31:42 PM".<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="DTS_UPDOWN"></span><span id="dts_updown"></span><dl> <dt>**DTS \_ UPDOWN**</dt> </dl>                                                 | Posiziona un controllo di tipo up-down a destra del controllo DTP per modificare i valori di data e ora. Questo stile può essere usato al posto del calendario mensile a discesa, ovvero lo stile predefinito.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Commenti

Gli stili XXXFORMAT DTS \_ che definiscono il formato di visualizzazione non possono essere combinati. Se nessuno degli stili di formato è adatto, usare un [**messaggio \_ SETFORMAT DTM**](dtm-setformat.md) per definire un formato personalizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





