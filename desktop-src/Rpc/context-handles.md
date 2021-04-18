---
title: Handle di contesto
description: In alcuni casi, le applicazioni distribuite richiedono che il programma server mantenga le informazioni sullo stato tra le chiamate del client.
ms.assetid: 91732a75-0a3a-44bd-9db9-c11be6fd2d70
keywords:
- RPC (Remote Procedure Call), descrizione, handle di contesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ff36ff8f1a36843293060e091b7eecee0d8666
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298229"
---
# <a name="context-handles"></a>Handle di contesto

In alcuni casi, le applicazioni distribuite richiedono che il programma server mantenga le informazioni sullo stato tra le chiamate del client. I programmi server che consentono di gestire più di un client alla volta devono contenere le informazioni sullo stato per ogni client. Poiché il client e il server utilizzano spazi di indirizzi diversi in computer diversi e non considerano necessariamente attendibili reciprocamente, gli approcci comuni alla condivisione dei dati spesso non funzionano. Ad esempio, il client e il server non sono in grado di mantenere le informazioni sullo stato della sessione remota nelle variabili globali perché non condividono lo stesso spazio di indirizzi globale. È difficile salvare le informazioni in un file condiviso perché vengono eseguite in computer diversi. Un approccio semplicistico potrebbe consistere nel fornire tutto lo stato al client e fare in modo che il client lo restituisca alla chiamata successiva, ma questo approccio presenta difetti: il server non considera necessariamente attendibile il client per restituire lo stato corretto e lo stato può essere associato in modo implicito a un altro stato sul server, ad esempio handle di file o socket aperti.

Microsoft RPC fornisce un meccanismo potente e sicuro chiamato handle di contesto per mantenere lo stato associato a un determinato client in un server. Le informazioni sullo stato sono denominate contesto del server. I client possono ottenere un handle di contesto per identificare il contesto del server per le singole sessioni RPC.

Per ogni client in un'applicazione distribuita, ad esempio, il programma server può creare e aggiornare un file di dati per la sessione RPC. Il server può utilizzare il relativo handle di file per ogni file di dati del client come handle di contesto. Ogni volta che un client richiede operazioni sul file di dati creato dal server, il client passa l'handle di contesto al server. Il client non ottiene effettivamente l'handle di file. Ottiene un token opaco che il tempo di esecuzione RPC del server può associare in modo univoco all'handle di file. Poiché l'handle del contesto è effettivamente un handle di file, il punto di controllo del contesto ha senso solo nello spazio degli indirizzi del server. Tuttavia, il programma client può utilizzare l'handle di contesto per indicare al server in quale file eseguire gli aggiornamenti.

Altri dati possono anche essere handle di contesto. Un client e un server possono ad esempio usare un numero di record di un record di database come handle di file. Se il client deve eseguire una serie di aggiornamenti su un record specifico, può ottenere il numero di record come handle di contesto. Passa il numero di record al server ogni volta che viene richiamata una procedura remota per aggiornare il record del database.

Spesso un handle di contesto punta a un blocco di memoria nel server in cui il server mantiene le varie informazioni di gestione.

In questa sezione vengono fornite informazioni sulla definizione e sull'utilizzo degli handle di contesto. La discussione viene presentata negli argomenti seguenti:

-   [Sviluppo di interfacce con handle di contesto](interface-development-using-context-handles.md)
-   [Sviluppo di server con handle di contesto](server-development-using-context-handles.md)
-   [Sviluppo di client con handle di contesto](client-development-using-context-handles.md)
-   [Routine di esecuzione del contesto del server](server-context-run-down-routine.md)
-   [Ripristino del contesto client](client-context-reset.md)
-   [Client multithreading e handle di contesto](multithreaded-clients-and-context-handles.md)

 

 




