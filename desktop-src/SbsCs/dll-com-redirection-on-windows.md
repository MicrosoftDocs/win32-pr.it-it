---
description: Il reindirizzamento DLL/COM è una strategia di isolamento delle applicazioni utilizzata dagli amministratori aziendali in Windows XP.
ms.assetid: 5bbb0bee-d457-4dfa-93a0-82537fe11f2d
title: Reindirizzamento DLL/COM in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e356c7b4cc6e5616a03eba60439c7478d65e626a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883913"
---
# <a name="dllcom-redirection-on-windows"></a>Reindirizzamento DLL/COM in Windows

Il reindirizzamento DLL/COM è una strategia di isolamento delle applicazioni utilizzata dagli amministratori aziendali in Windows XP.

* * Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP con SP2: * * l'uso di strategie di reindirizzamento DLL/COM non è consigliato perché le applicazioni isolate che usano manifesti e [assembly affiancati](about-side-by-side-assemblies-.md) possono essere più facili da aggiornare e servire. La presenza di un file. local viene ignorata se è presente un manifesto. La strategia di reindirizzamento DLL/COM con i file. local funziona se l'applicazione non dispone di un manifesto.

Il reindirizzamento DLL/COM associa un'applicazione a una versione locale di un componente. I file del componente locale possono essere mantenuti separati dalla versione del sistema del componente in un percorso privato per l'applicazione. La versione del sistema del componente è registrata a livello globale e disponibile per tutte le altre applicazioni che vi associano. La versione locale del componente è riservata all'utilizzo esclusivo dell'applicazione. Se necessario, i file componente utilizzati dall'applicazione possono essere caricati in memoria contemporaneamente ai file componente del sistema.

Il reindirizzamento DLL/COM viene attivato installando un file speciale insieme a una copia del file del componente locale nella stessa directory del file eseguibile dell'applicazione. Il file speciale è un file vuoto denominato dopo il nome file dell'eseguibile dell'applicazione e aggiunto con. local. Ad esempio, per attivare il reindirizzamento DLL/COM per un'applicazione denominata MyApp, la versione locale del componente e un file vuoto denominato Myapp.exe. local devono essere copiati nella cartella contenente Myapp.exe. In questo modo l'applicazione viene associata alla versione locale del componente, anziché alla versione globalmente condivisa del componente.

Quando un'applicazione carica un file di componente, ad esempio un file DLL o ocx, Windows ne esegue prima la ricerca nella cartella in cui è installato il file eseguibile e locale dell'applicazione. Se trovato, l'applicazione usa il file del componente indipendentemente da qualsiasi percorso di ricerca della directory definito nell'applicazione o nel registro di sistema. Se non viene trovato, viene usato il file del componente nel percorso di ricerca definito.

Per installare l'applicazione con reindirizzamento DLL/COM, è necessario che l'utilità di installazione esegua le operazioni seguenti:

-   Un file locale vuoto deve essere copiato nella stessa cartella del file eseguibile dell'applicazione.
-   Tutti i componenti, i file DLL e ocx utilizzati dall'applicazione devono essere copiati nella stessa cartella del file eseguibile dell'applicazione.
-   I componenti COM isolati devono essere registrati con Windows in modo che diverse versioni dell'assembly non siano in conflitto tra loro durante il caricamento in memoria nello stesso momento. Per il processo di registrazione è necessario che, mentre l'implementazione del componente possa variare tra le versioni, alcuni metadati COM, ad esempio CLSID, ProgID, libreria dei tipi e modello di threading, non possono.
-   Se l'applicazione viene installata usando il Windows Installer, la directory dell'applicazione può essere protetta tramite la tabella LockPermissions. In genere, al sistema viene assegnato l'accesso in lettura, scrittura ed esecuzione; a tutti gli altri processi viene assegnato solo l'accesso in lettura e esecuzione.

 

 



