---
title: Registrazione di applicazioni COM
description: Registrazione di applicazioni COM
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63caaba090c38e5917e6c85884fdf5a76e2353f6a57527ad5870d0fbd984b173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129983"
---
# <a name="registering-com-applications"></a>Registrazione di applicazioni COM

Il Registro di sistema è un database di sistema che contiene informazioni sulla configurazione dell'hardware e del software di sistema, nonché sugli utenti del sistema. Qualsiasi Windows programma basato su windows può aggiungere informazioni al Registro di sistema e leggere le informazioni dal Registro di sistema. I client ricercano nel Registro di sistema i componenti interessanti da usare.

Il Registro di sistema gestisce le informazioni su tutti gli oggetti COM installati nel sistema. Ogni volta che un'applicazione crea un'istanza di un componente COM, viene consultato il Registro di sistema per risolvere il CLSID o il ProgID del componente nel percorso della DLL del server o dell'EXE che lo contiene. Dopo aver determinato il server del componente, Windows carica il server nello spazio di elaborazione dell'applicazione client (componenti in-process) o avvia il server nel proprio spazio di elaborazione (server locali e remoti). Il server crea un'istanza del componente e restituisce al client un riferimento a una delle interfacce del componente.

Per altre informazioni sul registro Windows, vedere gli argomenti seguenti:

-   [Gerarchia del Registro di sistema](registry-hierarchy.md)
-   [Classi e server](classes-and-servers.md)
-   [Classificazione dei componenti](classifying-components.md)
-   [Uso di OleView](using-oleview.md)
-   [Registrazione dei componenti](registering-components.md)
-   [Controllo della registrazione](checking-registration.md)
-   [Tipi di utente sconosciuti](unknown-user-types.md)
-   [Chiavi del Registro di sistema COM](com-registry-keys.md)

 

 




