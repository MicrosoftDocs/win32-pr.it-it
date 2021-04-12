---
title: Ricezione di notifiche di modifiche
description: Molti client possono aggiornare contemporaneamente la tabella di routing e i client devono ricevere una notifica quando si verificano modifiche alle informazioni di routing.
ms.assetid: d42e16e2-32b2-4178-967b-e937730b3cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacd8d1d0329cf29be82a890be30b602b9330249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395755"
---
# <a name="receiving-notification-of-changes"></a>Ricezione di notifiche di modifiche

Molti client possono aggiornare contemporaneamente la tabella di routing e i client devono ricevere una notifica quando si verificano modifiche alle informazioni di routing. Ad esempio, un client che non riceve alcuna notifica delle modifiche di un altro client alla tabella di routing potrebbe annunciare informazioni sulle route obsolete. Questa operazione può essere impedita tramite la programmazione dei client per la registrazione con gestione tabelle di routing per ricevere notifiche delle modifiche apportate alla tabella di routing. Gestione tabelle di routing invia le notifiche delle modifiche a tutti i client registrati per riceverli.

La notifica delle modifiche è valida solo per le destinazioni. Non è possibile eseguire query su Gestione tabelle di routing per apportare modifiche a una route specifica.

Quando viene apportata una modifica a una delle route a una destinazione, il servizio di gestione delle tabelle di routing invia una notifica che indica che si è verificata una modifica. Questa notifica viene inviata solo ai client che hanno eseguito la registrazione con gestione tabelle di routing per il tipo di modifica che si è verificata. Tutte le modifiche apportate alle informazioni di routing in Gestione tabelle di routing si verificano in una o più viste e i messaggi di notifica delle modifiche possono essere richiesti in qualsiasi subset di visualizzazioni supportate.

Attualmente sono disponibili tre tipi di notifiche di modifica per le quali un client può registrarsi:

-   Notifica di qualsiasi modifica apportata alle route per la destinazione. Questa richiesta viene eseguita utilizzando il \_ flag di modifica \_ tipo RTM \_ all.
-   Notifica se il percorso migliore per la destinazione cambia o una delle informazioni seguenti per le modifiche più recenti alla route:

    -   Preferenza
    -   Hop successivi
    -   Flag di route

    Questa richiesta viene eseguita utilizzando il \_ flag di \_ tipo modifica RTM \_ .

-   Notifica di tutte le modifiche apportate al \_ tipo di modifica RTM \_ \_ , eccetto le modifiche apportate ai flag non di inoltro nella migliore route. Ad esempio, gestione router attende le modifiche di questo tipo nella visualizzazione unicast e aggiorna le informazioni nel server d'avvio unicast. Questa richiesta viene effettuata utilizzando il \_ flag di invio del tipo di modifica RTM \_ \_ .

È anche possibile limitare le richieste di notifiche delle modifiche a un subset di destinazioni eseguendo la registrazione per le notifiche delle modifiche solo alle destinazioni "contrassegnate". Il client può contrassegnare una destinazione per la notifica di modifica chiamando [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification).

Quando si verifica una modifica, gestione tabelle di routing verifica se sono presenti client che devono ricevere notifiche relative a questa modifica. Un client deve ricevere una notifica di una modifica se vengono soddisfatte tutte le condizioni seguenti:

-   Il tipo di modifica che si è verificato è un tipo per il quale il client ha effettuato la registrazione per la notifica
-   Le modifiche apportate a una destinazione contrassegnata dal client sono state eseguite o da qualsiasi destinazione, se il client ha richiesto modifiche per tutte le destinazioni
-   Il client ha richiesto una notifica di modifica per la vista in cui si è verificata questa modifica

Se la modifica soddisfa tutti i criteri sopra indicati, la modifica viene memorizzata nella cache e il client riceve una notifica.

La notifica non specifica le modifiche effettive che si sono verificate. Il client deve recuperare le modifiche chiamando [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) usando l'handle di notifica ottenuto da una precedente chiamata a [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification).

 

 




