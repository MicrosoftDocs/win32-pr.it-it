---
description: Le interfacce seguenti vengono utilizzate nella comunicazione asincrona tra le applicazioni e i componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitoraggi delle porte.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Funzioni di notifica di stampa asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fa7b0b61de15af9f7117e7c36104eb51abbb7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318037"
---
# <a name="asynchronous-printing-notification-functions"></a>Funzioni di notifica di stampa asincrone

Le interfacce seguenti vengono utilizzate nella comunicazione asincrona tra le applicazioni e i componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitoraggi delle porte.

## <a name="in-this-section"></a>Contenuto della sezione



| Funzione                                                                                        | Descrizione                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | Consente di creare un canale di comunicazione tra un componente di stampa ospitato da spooler di stampa, ad esempio un driver di stampa o un monitor di porta, e un'applicazione che riceve le notifiche dal componente.<br/> |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | Consente a un'applicazione di registrarsi per le notifiche dai componenti di stampa ospitati dallo spooler di stampa, ad esempio driver della stampante, processori di stampa e monitoraggi delle porte.<br/>                              |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | Consente a un'applicazione che ha effettuato la registrazione di ricevere notifiche da componenti di stampa ospitati da spooler di stampa per annullare la registrazione.<br/>                                                              |



 

 

 




