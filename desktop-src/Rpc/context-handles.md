---
title: Handle di contesto
description: In alcuni casi, le applicazioni distribuite richiedono al programma server di mantenere le informazioni sullo stato tra le chiamate client.
ms.assetid: 91732a75-0a3a-44bd-9db9-c11be6fd2d70
keywords:
- RPC remote procedure call , descritto, handle di contesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73fb49a2e4c09ec818777389194df98e0d7b8bcac618d05ff7b519aefe5eb28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073421"
---
# <a name="context-handles"></a>Handle di contesto

In alcuni casi, le applicazioni distribuite richiedono al programma server di mantenere le informazioni sullo stato tra le chiamate client. I programmi server che esercitono più client alla volta devono mantenere le informazioni sullo stato per ogni client. Poiché il client e il server usano spazi di indirizzi diversi in computer diversi e non si fidano necessariamente l'uno dell'altro, gli approcci comuni alla condivisione dei dati spesso non funzionano. Ad esempio, il client e il server non sono in grado di mantenere le informazioni sullo stato nella sessione remota nelle variabili globali perché non condividono lo stesso spazio indirizzi globale. È difficile mantenere le informazioni in un file condiviso perché vengono eseguite in computer diversi. Un approccio semplicistico può essere quello di spedire tutto lo stato al client e fare in modo che il client lo restituisca alla chiamata successiva, ma questo approccio presenta difetti: il server non considera necessariamente attendibile il client per restituire lo stato giusto e lo stato può essere implicitamente associato a un altro stato nel server, ad esempio handle di file o socket aperti.

Microsoft RPC offre un meccanismo potente e sicuro denominato handle di contesto per mantenere lo stato associato a un determinato client in un server. Le informazioni sullo stato sono denominate contesto del server. I client possono ottenere un handle di contesto per identificare il contesto del server per le singole sessioni RPC.

Ad esempio, ogni client in un'applicazione distribuita può fare in modo che il programma server crei e aggiorne un file di dati per la sessione RPC. Il server può usare il relativo handle di file per il file di dati di ogni client come handle di contesto. Ogni volta che un client richiede operazioni sul file di dati creato dal server, il client passa l'handle di contesto al server. Il client non ottiene effettivamente l'handle di file stesso. ottiene un token opaco che il tempo di esecuzione RPC del server può associare in modo univoco all'handle di file. Poiché l'handle di contesto è effettivamente un handle di file, l'handle di contesto ha senso solo nello spazio degli indirizzi del server. Tuttavia, il programma client può usare l'handle di contesto per indicare al server in quale file eseguire gli aggiornamenti.

Altri dati possono anche essere handle di contesto. Ad esempio, un client e un server possono usare un numero record di un record di database come handle di file. Se il client deve eseguire una serie di aggiornamenti su un record specifico, può ottenere il numero di record come handle di contesto. Passerebbe il numero di record al server ogni volta che richiamava una procedura remota per aggiornare il record del database.

Molto spesso un handle di contesto punta a un blocco di memoria nel server in cui il server conserva varie informazioni di gestione.

Questa sezione presenta informazioni sulla definizione e sull'uso degli handle di contesto. La discussione è presentata negli argomenti seguenti:

-   [Sviluppo di interfacce tramite handle di contesto](interface-development-using-context-handles.md)
-   [Sviluppo di server tramite handle di contesto](server-development-using-context-handles.md)
-   [Sviluppo client tramite handle di contesto](client-development-using-context-handles.md)
-   [Routine di esecuzione del contesto del server](server-context-run-down-routine.md)
-   [Reimpostazione del contesto client](client-context-reset.md)
-   [Client multithreading e handle di contesto](multithreaded-clients-and-context-handles.md)

 

 




