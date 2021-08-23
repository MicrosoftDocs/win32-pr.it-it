---
description: Informazioni sulle interfacce usate nella comunicazione asincrona tra applicazioni e componenti ospitati dallo spooler di stampa.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Interfacce di notifica per la stampa asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357610b30d01b89ed8fd7e2fe7354f727a44c8f04b41d71d846af622113aa435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720221"
---
# <a name="asynchronous-printing-notification-interfaces"></a>Interfacce di notifica per la stampa asincrona

Le interfacce seguenti vengono utilizzate nella comunicazione asincrona tra applicazioni e componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitor di porta.

## <a name="in-this-section"></a>Contenuto della sezione



| Interfaccia                                                                     | Descrizione                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintAsyncNotifyCallback**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | Crea e gestisce un canale di comunicazione utilizzato dalle applicazioni e dai componenti ospitati dallo spooler di stampa.<br/>                                                                                                                              |
| [**IPrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | Rappresenta un canale di comunicazione utilizzato dai componenti ospitati dallo spooler di stampa per inviare notifiche alle applicazioni. Se il canale è bidirezionale, le applicazioni possono usare lo stesso canale per inviare risposte al componente.<br/> |
| [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | Incapsula i dati inviati in un canale di notifica. <br/>                                                                                                                                                                                             |



 

 

 




