---
title: Esercitazione
description: Questa esercitazione illustra i passaggi necessari per creare una semplice applicazione distribuita a server singolo a singolo client da un'applicazione autonoma esistente.
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- RPC remote procedure call, esercitazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c19b0d8ec3b3eb55cf29ccfd87eca43775c2ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045079"
---
# <a name="tutorial"></a>Esercitazione

Questa esercitazione illustra i passaggi necessari per creare una semplice applicazione distribuita a server singolo a singolo client da un'applicazione autonoma esistente. Questi passaggi sono i seguenti:

-   Crea la definizione dell'interfaccia e i file di configurazione dell'applicazione.
-   Usare il compilatore MIDL per generare stub e intestazioni server e client in linguaggio C da tali file.
-   Scrivere un'applicazione client che gestisce la connessione al server.
-   Scrivere un'applicazione server contenente le procedure remote effettive.
-   Compilare e collegare questi file alla libreria di runtime RPC per produrre l'applicazione distribuita.

L'applicazione client passa una stringa di caratteri al server in una chiamata di procedura remota e il server stampa la stringa "Hello, World" nell'output standard.

I file di origine completi per questa applicazione di esempio, con codice aggiuntivo per la gestione dell'input della riga di comando e per l'output di diversi messaggi di stato all'utente, si trovano nella \\ directory Hello RPC di Platform Software Development Kit (SDK).

Questa sezione presenta le discussioni negli argomenti seguenti:

-   [Applicazione autonoma](the-standalone-application.md)
-   [Definizione dell'interfaccia](defining-the-interface.md)
-   [Generazione dell'UUID](generating-the-uuid.md)
-   [File IDL](the-idl-file.md)
-   [Il file ACF](the-acf-file.md)
-   [Generazione dei file stub](generating-the-stub-files.md)
-   [Applicazione client](the-client-application.md)
-   [Applicazione server](the-server-application.md)
-   [Arresto dell'applicazione server](stopping-the-server-application.md)
-   [Compilazione e collegamento](compiling-and-linking.md)
-   [Esecuzione dell'applicazione](running-the-application.md)

 

 




