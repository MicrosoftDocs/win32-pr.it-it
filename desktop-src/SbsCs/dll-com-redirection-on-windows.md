---
description: Il reindirizzamento DLL/COM è una strategia di isolamento delle applicazioni utilizzata dagli amministratori aziendali in Windows XP.
ms.assetid: 5bbb0bee-d457-4dfa-93a0-82537fe11f2d
title: Reindirizzamento DLL/COM in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ce6b55c2a66d298b7b80248613eab7cefe96c25f8f53dd9218966e235ea267f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142264"
---
# <a name="dllcom-redirection-on-windows"></a>Reindirizzamento DLL/COM in Windows

Il reindirizzamento DLL/COM è una strategia di isolamento delle applicazioni utilizzata dagli amministratori aziendali in Windows XP.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP con SP2: ** L'uso di strategie di reindirizzamento DLL/COM non è consigliato perché le applicazioni isolate che usano manifesti e assembly [side-by-side](about-side-by-side-assemblies-.md) possono essere più facili da aggiornare e da usare. La presenza di un file con estensione local viene ignorata se è presente un manifesto. La strategia di reindirizzamento DLL/COM che usa file locali funziona se l'applicazione non dispone di un manifesto.

Il reindirizzamento DLL/COM associa un'applicazione a una versione locale di un componente. I file del componente locale possono essere mantenuti separati dalla versione del sistema del componente in un percorso privato per l'applicazione. La versione del sistema del componente è registrata a livello globale e disponibile per qualsiasi altra applicazione associata. La versione locale del componente è riservata per l'uso esclusivo dell'applicazione. Se necessario, i file dei componenti usati dall'applicazione possono essere caricati in memoria contemporaneamente ai file dei componenti del sistema.

Il reindirizzamento DLL/COM viene attivato installando un file speciale insieme a una copia del file del componente locale nella stessa directory del file eseguibile dell'applicazione. Il file speciale è un file vuoto denominato dopo il nome del file eseguibile dell'applicazione e aggiunto con .local. Ad esempio, per attivare il reindirizzamento DLL/COM per un'applicazione denominata Myapp, la versione locale del componente e un file vuoto denominato Myapp.exe.local devono essere copiati nella cartella contenente Myapp.exe. In questo modo l'applicazione viene associata alla versione locale del componente anziché alla versione condivisa a livello globale del componente.

Quando un'applicazione carica un file di componente, ad esempio un file DLL o ocx, Windows cerca prima di tutto il file nella cartella in cui è installato il file locale e il file eseguibile dell'applicazione. Se viene trovato, l'applicazione usa il file del componente indipendentemente dal percorso di ricerca di directory definito nell'applicazione o nel Registro di sistema. Se non viene trovato, viene usato il file del componente nel percorso di ricerca definito.

L'utilità di installazione deve eseguire le operazioni seguenti per installare l'applicazione con il reindirizzamento DLL/COM:

-   Un file .local vuoto deve essere copiato nella stessa cartella del file eseguibile dell'applicazione.
-   Tutti i componenti, i file DLL e ocx usati dall'applicazione devono essere copiati nella stessa cartella del file eseguibile dell'applicazione.
-   I componenti COM isolati devono essere registrati con Windows in modo che versioni diverse dell'assembly non siano in conflitto tra loro quando vengono caricate in memoria contemporaneamente. Il processo di registrazione richiede che, anche se l'implementazione del componente può cambiare tra le versioni, alcuni metadati COM come CLSID, ProgID, libreria dei tipi e modello di threading non possono essere.
-   Se l'applicazione viene installata usando il programma Windows, la directory dell'applicazione può essere protetta tramite la tabella LockPermissions. In genere, al sistema viene assegnato l'accesso in lettura, scrittura ed esecuzione. a tutti gli altri processi viene assegnato solo l'accesso in lettura e di esecuzione.

 

 



