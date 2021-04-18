---
title: Stili del controllo selezione data e ora (CommCtrl. h)
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
ms.openlocfilehash: 2d24e7543e4e843fc70e0ccacdab670e18e46cf3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327246"
---
# <a name="date-and-time-picker-control-styles"></a>Stili del controllo selezione data e ora

Gli stili della finestra elencati di seguito sono specifici dei controlli selezione data e ora.



| Costante                                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DTS_APPCANPARSE"></span><span id="dts_appcanparse"></span><dl> <dt>**\_APPCANPARSE DTS**</dt> </dl>                                  | Consente al proprietario di analizzare l'input dell'utente ed eseguire l'azione necessaria. Consente agli utenti di modificare all'interno dell'area client del controllo quando preme il tasto F2. Il controllo Invia i codici di notifica [ \_ USERSTRING di DTN](dtn-userstring.md) al termine degli utenti.<br/>                                                                                                                                                                                                                                                                    |
| <span id="DTS_LONGDATEFORMAT"></span><span id="dts_longdateformat"></span><dl> <dt>**\_LONGDATEFORMAT DTS**</dt> </dl>                         | Visualizza la data nel formato lungo. La stringa di formato predefinita per questo stile è definita dalle impostazioni locali \_ SLONGDATEFORMAT, che producono output come "Friday, 19 aprile 1996". Quando si usa questo stile, il pulsante a discesa non visualizza un'icona.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="DTS_RIGHTALIGN"></span><span id="dts_rightalign"></span><dl> <dt>**\_RIGHTALIGN DTS**</dt> </dl>                                     | Il calendario mensile a discesa verrà allineato a destra con il controllo anziché allineato a sinistra, che è l'impostazione predefinita. <br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHOWNONE"></span><span id="dts_shownone"></span><dl> <dt>**\_SHOWNONE DTS**</dt> </dl>                                           | Nel controllo è possibile che non sia attualmente selezionata alcuna data. Con questo stile, il controllo Visualizza una casella di controllo che viene selezionata automaticamente ogni volta che viene scelta o immessa una data. Se la casella di controllo viene successivamente deselezionata, l'applicazione non può recuperare la data dal controllo perché, in sostanza, il controllo non ha una data. Lo stato della casella di controllo può essere impostato con il [**messaggio \_ SETSYSTEMTIME di DTM**](dtm-setsystemtime.md) o con il messaggio [**\_ GETSYSTEMTIME di DTM**](dtm-getsystemtime.md) .<br/> |
| <span id="DTS_SHORTDATEFORMAT"></span><span id="dts_shortdateformat"></span><dl> <dt>**\_SHORTDATEFORMAT DTS**</dt> </dl>                      | Visualizza la data in formato breve. La stringa di formato predefinita per questo stile è definita dalle impostazioni locali \_ SSHORTDATE, che producono output come "4/19/96".<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHORTDATECENTURYFORMAT"></span><span id="dts_shortdatecenturyformat"></span><dl> <dt>**\_SHORTDATECENTURYFORMAT DTS**</dt> </dl> | **Versione 5,80.** Simile allo stile **DTS \_ SHORTDATEFORMAT** , ad eccezione del fatto che year è un campo a quattro cifre. La stringa di formato predefinita per questo stile è basata sulle impostazioni locali \_ SSHORTDATE. L'output ha un aspetto simile al seguente: "4/19/1996".<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="DTS_TIMEFORMAT"></span><span id="dts_timeformat"></span><dl> <dt>**\_TimeFormat DTS**</dt> </dl>                                     | Consente di visualizzare l'ora. La stringa di formato predefinita per questo stile è definita dalle impostazioni locali \_ STIMEFORMAT, che producono output come "5:31:42 PM".<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="DTS_UPDOWN"></span><span id="dts_updown"></span><dl> <dt>**stato \_ attivo DTS**</dt> </dl>                                                 | Inserisce un controllo di scorrimento a destra del controllo DTP per modificare i valori di data e ora. Questo stile può essere utilizzato al posto del calendario mensile a discesa, che è lo stile predefinito.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Commenti

Gli \_ stili DTS XXXFORMAT che definiscono il formato di visualizzazione non possono essere combinati. Se nessuno degli stili di formato è adatto, usare un messaggio di tipo [**\_ seformativo DTM**](dtm-setformat.md) per definire un formato personalizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





