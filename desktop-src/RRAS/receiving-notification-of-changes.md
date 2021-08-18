---
title: Ricezione della notifica delle modifiche
description: Molti client possono aggiornare contemporaneamente la tabella di routing e i client devono ricevere una notifica quando si verificano modifiche alle informazioni di routing.
ms.assetid: d42e16e2-32b2-4178-967b-e937730b3cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6eddc92404acb921b31bab22736561cbbc83e4c1c641da80a8ff95352e52f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788711"
---
# <a name="receiving-notification-of-changes"></a>Ricezione della notifica delle modifiche

Molti client possono aggiornare contemporaneamente la tabella di routing e i client devono ricevere una notifica quando si verificano modifiche alle informazioni di routing. Ad esempio, un client che non viene informato delle modifiche apportate da un altro client alla tabella di routing potrebbe annunciare informazioni sulla route non aggiornate. Questa operazione può essere impedita dalla programmazione dei client per la registrazione con il gestore tabelle di routing per ricevere notifiche delle modifiche nella tabella di routing. Il gestore tabelle di routing invia notifiche di modifiche a tutti i client che si registrano per riceverle.

La notifica di modifica si applica solo alle destinazioni. Non è possibile eseguire query sul gestore tabelle di routing per le modifiche apportate a una route specifica.

Quando viene apportata una modifica a una delle route verso una destinazione, il gestore tabelle di routing invia una notifica che indica che si è verificata una modifica. Questa notifica viene inviata solo ai client registrati con gestione tabelle di routing per il tipo di modifica che si è verificata. Tutte le modifiche alle informazioni di routing in Gestione tabelle di routing si verificano in una o più viste e i messaggi di notifica delle modifiche possono essere richiesti in qualsiasi subset di viste supportate.

Esistono attualmente tre tipi di notifiche di modifica per cui un client può eseguire la registrazione:

-   Notifica di qualsiasi modifica alle route per la destinazione. Questa richiesta viene effettuata usando il \_ flag RTM CHANGE \_ TYPE \_ ALL.
-   Notifica se la route migliore per la destinazione cambia o una delle informazioni seguenti per la route migliore corrente cambia:

    -   Preferenza
    -   Hop successivi
    -   Flag di route

    Questa richiesta viene effettuata usando il \_ flag RTM CHANGE \_ TYPE \_ BEST.

-   Notifica di tutte le modifiche del tipo RTM CHANGE TYPE BEST, ad eccezione delle modifiche nei flag di non inoltro \_ \_ nella route \_ migliore. Ad esempio, gestione router attende le modifiche di questo tipo nella visualizzazione unicast e aggiorna le informazioni nel server d'inoltro unicast. Questa richiesta viene effettuata usando il \_ flag RTM CHANGE \_ TYPE \_ FORWARDING.

Le richieste di notifiche delle modifiche possono anche essere limitate a un subset di destinazioni registrando per le notifiche delle modifiche solo alle destinazioni "contrassegnate". Il client può contrassegnare una destinazione per la notifica delle modifiche chiamando [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification).

Quando si verifica una modifica, gestione tabelle di routing verifica se sono presenti client che devono ricevere una notifica di questa modifica. Un client deve ricevere una notifica di una modifica se vengono soddisfatte tutte le condizioni seguenti:

-   Il tipo di modifica che si è verificato è un tipo per il quale il client ha registrato per la notifica
-   Si sono verificate modifiche a una destinazione contrassegnata dal client o a qualsiasi destinazione, se il client ha richiesto modifiche per tutte le destinazioni
-   Notifica di modifica richiesta dal client per la vista in cui si è verificata la modifica

Se la modifica soddisfa tutti i criteri precedenti, la modifica viene memorizzata nella cache e il client viene informato.

La notifica non specifica quali sono le modifiche effettive, ma solo che si sono verificate. Il client deve recuperare le modifiche chiamando [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) usando l'handle di notifica ottenuto da una chiamata precedente a [**RtmRegisterForChangeNotification.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)

 

 




