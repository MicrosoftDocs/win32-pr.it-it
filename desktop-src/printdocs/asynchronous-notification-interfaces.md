---
description: Le interfacce seguenti vengono utilizzate nella comunicazione asincrona tra le applicazioni e i componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitoraggi delle porte.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Interfacce di notifica di stampa asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7da8d320b33224e81852542e39f435b45b6dab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759557"
---
# <a name="asynchronous-printing-notification-interfaces"></a>Interfacce di notifica di stampa asincrone

Le interfacce seguenti vengono utilizzate nella comunicazione asincrona tra le applicazioni e i componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitoraggi delle porte.

## <a name="in-this-section"></a>Contenuto della sezione



| Interfaccia                                                                     | Descrizione                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintAsyncNotifyCallback**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | Crea e gestisce un canale di comunicazione utilizzato dalle applicazioni e dai componenti ospitati dallo spooler di stampa.<br/>                                                                                                                              |
| [**IPrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | Rappresenta un canale di comunicazione utilizzato dai componenti ospitati dallo spooler di stampa per inviare notifiche alle applicazioni. Se il canale è bidirezionale, le applicazioni possono utilizzare lo stesso canale per restituire risposte al componente.<br/> |
| [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | Incapsula i dati inviati in un canale di notifica. <br/>                                                                                                                                                                                             |



 

 

 




