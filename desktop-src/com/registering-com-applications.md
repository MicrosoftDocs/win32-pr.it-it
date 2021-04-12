---
title: Registrazione di applicazioni COM
description: Registrazione di applicazioni COM
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e115c4a8445e701809a7f418e0ce4ef72226eb0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331807"
---
# <a name="registering-com-applications"></a>Registrazione di applicazioni COM

Il registro di sistema è un database di sistema che contiene informazioni sulla configurazione dell'hardware e del software del sistema, nonché sugli utenti del sistema. Qualsiasi programma basato su Windows può aggiungere informazioni al registro di sistema e leggere le informazioni dal registro di sistema. I client cercano i componenti interessanti da usare nel registro di sistema.

Il registro di sistema mantiene le informazioni su tutti gli oggetti COM installati nel sistema. Ogni volta che un'applicazione crea un'istanza di un componente COM, viene consultato il registro di sistema per risolvere il CLSID o il ProgID del componente nel percorso della DLL del server o del file EXE che lo contiene. Dopo aver determinato il server del componente, Windows carica il server nello spazio di processo dell'applicazione client (componenti in-process) o avvia il server nello spazio di processo (server locali e remoti). Il server crea un'istanza del componente e restituisce al client un riferimento a una delle interfacce del componente.

Per ulteriori informazioni sul Registro di sistema di Windows, vedere gli argomenti seguenti:

-   [Gerarchia del registro di sistema](registry-hierarchy.md)
-   [Classi e server](classes-and-servers.md)
-   [Classificazione di componenti](classifying-components.md)
-   [Uso di OleView](using-oleview.md)
-   [Registrazione di componenti](registering-components.md)
-   [Verifica della registrazione](checking-registration.md)
-   [Tipi di utente sconosciuti](unknown-user-types.md)
-   [Chiavi del registro di sistema COM](com-registry-keys.md)

 

 




