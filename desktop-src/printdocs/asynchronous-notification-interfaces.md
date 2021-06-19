---
description: Informazioni sulle interfacce usate nella comunicazione asincrona tra applicazioni e componenti ospitati dallo spooler di stampa.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Interfacce di notifica per la stampa asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe0de2cf8510b1bb039907067b62fce08a4145
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396096"
---
# <a name="asynchronous-printing-notification-interfaces"></a>Interfacce di notifica per la stampa asincrona

Le interfacce seguenti vengono usate nella comunicazione asincrona tra applicazioni e componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitoraggi delle porte.

## <a name="in-this-section"></a>Contenuto della sezione



| Interfaccia                                                                     | Descrizione                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintAsyncNotifyCallback**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | Crea e gestisce un canale di comunicazione utilizzato dalle applicazioni e dai componenti ospitati dallo spooler di stampa.<br/>                                                                                                                              |
| [**IPrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | Rappresenta un canale di comunicazione utilizzato dai componenti ospitati dallo spooler di stampa per inviare notifiche alle applicazioni. Se il canale è bidirezionale, le applicazioni possono usare lo stesso canale per inviare le risposte al componente.<br/> |
| [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | Incapsula i dati inviati in un canale di notifica. <br/>                                                                                                                                                                                             |



 

 

 




