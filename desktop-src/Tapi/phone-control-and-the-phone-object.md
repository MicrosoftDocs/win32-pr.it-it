---
description: TAPI 3,1 introduce i controlli telefono basati su COM. Si presuppone una certa familiarità con COM, automazione OLE e scripting, così come è la conoscenza del modello a oggetti TAPI 3. È inoltre utile conoscere le funzioni di controllo del telefono TAPI 2.
ms.assetid: e56aef54-e358-429b-9f0f-c8776507d95f
title: Controllo telefono e oggetto telefono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e9344d54a63efcf1692af361a5f8e88121981e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310716"
---
# <a name="phone-control-and-the-phone-object"></a>Controllo telefono e oggetto telefono

TAPI 3,1 introduce i controlli telefono basati su COM. Si presuppone una certa familiarità con COM, automazione OLE e scripting, così come è la conoscenza del modello a oggetti TAPI 3. È inoltre utile conoscere le funzioni di controllo del telefono TAPI 2.

Il controllo telefonico viene implementato a tre livelli di funzionalità, ciascuno dei quali si basa su quello precedente:

-   Oggetto Phone. Il primo livello definisce il modo in cui i dispositivi telefonici TAPI 2. x (API, costanti e messaggi che iniziano con "Phone") vengono esposti nel modello a oggetti TAPI 3,1. Si tratta di un nuovo oggetto Phone esposto da TAPI 3,1, con [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) come interfaccia predefinita nel nuovo oggetto. L'interfaccia **ITPhone** , insieme alle costanti associate, ai tipi enumerati e agli eventi, in genere espone lo stesso livello di dettaglio e funzionalità delle funzioni TAPI 2. x, delle costanti, delle strutture e dei messaggi che iniziano con la parola "Phone". Questo livello include anche nuove interfacce su diversi oggetti TAPI 3. x esistenti per facilitare la creazione di oggetti telefono e l'associazione di oggetti telefono ad altri oggetti a cui sono correlati.
-   Controllo telefonico automatico e gestione chiamate. Il secondo livello è costituito da un'interfaccia aggiuntiva denominata [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) e dalle costanti associate, dai tipi enumerati e dagli eventi. Si tratta di un'interfaccia secondaria nell'oggetto Phone. Se il dispositivo telefonico è stato aperto con il privilegio proprietario, usare il metodo **QueryInterface** sull'interfaccia [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) per ottenere un puntatore a interfaccia **ITAutomatedPhoneControl** .
-   Connessione telefonica Windows 2000. Il terzo livello è costituito dalle modifiche apportate all'applicazione di connessione telefonica Windows 2000 per implementare interazioni utente specifiche.

Microsoft o gli sviluppatori di terze parti possono utilizzare il modello a oggetti di TAPI 3,1 per implementare applicazioni o servizi più avanzati che coinvolgono telefoni, incluso un servizio che consente l'utilizzo di telefoni USB (Universal Serial Bus), ad esempio, per le chiamate telefoniche anche se nessun utente è connesso e non è stata avviata in modo esplicito nessun'altra applicazione TAPI.

In TAPI 3,0, un MSP del telefono ha tentato di migliorare i dispositivi telefonici associati alle linee usate per le chiamate TAPI 3,0. Questo sviluppo ha lo scopo di supportare modem con vivavoce con commutazione software. Le applicazioni TAPI 3,1 che usano questo tipo di modem devono usare gli oggetti telefono TAPI 3,1 per modificare lo stato hookswitch del modem.

Per altre informazioni e per un elenco di tutte le interfacce associate all'oggetto Phone, vedere [interfacce di oggetti telefono](phone-object-interfaces.md). Le interfacce del controllo telefonico espongono metodi che consentono di controllare i set di telefono utilizzando COM.

 

 



