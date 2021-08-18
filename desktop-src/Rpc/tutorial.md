---
title: Esercitazione
description: Questa esercitazione illustra i passaggi necessari per creare una semplice applicazione distribuita a client singolo e a server singolo da un'applicazione autonoma esistente.
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- Chiamata di procedura remota RPC , esercitazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd7259e5f5f0b9d0d273ff99a7cd5b42d15d57beaa60300fadecb7045a96876
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011179"
---
# <a name="tutorial"></a>Esercitazione

Questa esercitazione illustra i passaggi necessari per creare una semplice applicazione distribuita a client singolo e a server singolo da un'applicazione autonoma esistente. Questi passaggi sono:

-   Creare i file di definizione dell'interfaccia e di configurazione dell'applicazione.
-   Usare il compilatore MIDL per generare stub e intestazioni client e server in linguaggio C da tali file.
-   Scrivere un'applicazione client che gestirà la connessione al server.
-   Scrivere un'applicazione server contenente le procedure remote effettive.
-   Compilare e collegare questi file alla libreria di runtime RPC per produrre l'applicazione distribuita.

L'applicazione client passa una stringa di caratteri al server in una chiamata di procedura remota e il server stampa la stringa "Hello, World" nell'output standard.

I file di origine completi per questa applicazione di esempio, con codice aggiuntivo per gestire l'input della riga di comando e per l'output di vari messaggi di stato all'utente, sono nella directory RPC Hello di \\ Platform Software Development Kit (SDK).

Questa sezione presenta la discussione negli argomenti seguenti:

-   [Applicazione autonoma](the-standalone-application.md)
-   [Definizione dell'interfaccia](defining-the-interface.md)
-   [Generazione dell'UUID](generating-the-uuid.md)
-   [The IDL File](the-idl-file.md)
-   [The ACF File](the-acf-file.md)
-   [Generazione dei file stub](generating-the-stub-files.md)
-   [Applicazione client](the-client-application.md)
-   [Applicazione server](the-server-application.md)
-   [Arresto dell'applicazione server](stopping-the-server-application.md)
-   [Compilazione e collegamento](compiling-and-linking.md)
-   [Esecuzione dell'applicazione](running-the-application.md)

 

 




