---
description: Informazioni sulle funzioni usate nella comunicazione asincrona tra applicazioni e componenti ospitati dallo spooler di stampa.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Funzioni di notifica per la stampa asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d533ad1a3d1a8201e5a2d91946a66daee6cecd796e7bcc8e9c14d2c593542c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720241"
---
# <a name="asynchronous-printing-notification-functions"></a>Funzioni di notifica per la stampa asincrona

Le funzioni seguenti vengono utilizzate nella comunicazione asincrona tra applicazioni e componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitor di porta.

## <a name="in-this-section"></a>Contenuto della sezione



| Funzione                                                                                        | Descrizione                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | Crea un canale di comunicazione tra un componente di stampa ospitato da Spooler di stampa, ad esempio un driver di stampa o un monitor di porta, e un'applicazione che riceve notifiche dal componente.<br/> |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | Consente a un'applicazione di registrarsi per le notifiche dai componenti di stampa ospitati da Spooler di stampa, ad esempio driver della stampante, processori di stampa e monitor di porta.<br/>                              |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | Consente a un'applicazione registrata di ricevere notifiche dai componenti di stampa ospitati da Spooler di stampa per annullare la registrazione.<br/>                                                              |



 

 

 




