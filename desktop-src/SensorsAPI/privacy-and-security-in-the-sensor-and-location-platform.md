---
description: La piattaforma sensore e posizione di Windows include le impostazioni di privacy per aiutare a proteggere le informazioni personali degli utenti.
ms.assetid: 24425ed2-7b94-4b05-b117-9118d2074f49
title: Privacy e sicurezza nella piattaforma sensore e posizione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb0bf50cd27de1fc7fd4f42bd7a8455a549eea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306363"
---
# <a name="privacy-and-security-in-the-windows-sensor-and-location-platform"></a>Privacy e sicurezza nella piattaforma sensore e posizione di Windows

La piattaforma sensore e posizione di Windows include le impostazioni di privacy per aiutare a proteggere le informazioni personali degli utenti.

La piattaforma consente di garantire che i dati dei sensori rimangano privati, quando è necessaria la riservatezza, nei modi seguenti:

-   Per impostazione predefinita, i sensori sono spenti. Poiché la progettazione della piattaforma presuppone che qualsiasi sensore possa fornire dati personali, ogni sensore viene disabilitato fino a quando l'utente non fornisce il consenso esplicito per accedere ai dati del sensore.
-   Windows fornisce messaggi di divulgazione e contenuto della Guida per l'utente. Questo contenuto consente agli utenti di comprendere in che modo i sensori possono influenzare la privacy dei dati personali e aiutare gli utenti a prendere decisioni informate.
-   Per fornire l'autorizzazione per un sensore sono necessari i diritti di amministratore.
-   Quando è abilitata, un dispositivo sensore funziona per tutti i programmi in esecuzione con un determinato account utente (o per tutti gli account utente). Sono inclusi gli utenti e i servizi non interattivi, ad esempio ASPNET o SYSTEM. Ad esempio, se si Abilita un sensore GPS per l'account utente, solo i programmi in esecuzione con l'account utente hanno accesso al GPS. Se si Abilita il GPS per tutti gli utenti, qualsiasi programma in esecuzione con qualsiasi account utente avrà accesso al GPS.
-   I programmi che usano i sensori possono chiamare un metodo per aprire una finestra di dialogo di sistema che richiede agli utenti di abilitare i dispositivi sensori necessari. Questa funzionalità rende più semplice per gli sviluppatori e gli utenti verificare che i sensori funzionino quando sono necessari ai programmi, mantenendo al tempo stesso il controllo della divulgazione dei dati del sensore.
-   I driver dei sensori utilizzano un oggetto speciale che elabora tutte le richieste di I/O. Questo oggetto assicura che solo i programmi che dispongono dell'autorizzazione utente possano accedere ai dati del sensore.

 

 



