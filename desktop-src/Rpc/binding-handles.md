---
title: Handle di associazione
description: Il binding è il processo di creazione di una connessione logica tra un programma client e un programma server. Le informazioni che compongono l'associazione tra il client e il server sono rappresentate da una struttura denominata handle di associazione.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07973deb8319b44a82795a6402ef5e1a9310c2c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516846"
---
# <a name="binding-handles"></a>Handle di associazione

Il binding è il processo di creazione di una connessione logica tra un programma client e un programma server. Le informazioni che compongono l'associazione tra il client e il server sono rappresentate da una struttura denominata handle di associazione.

Un handle di associazione è analogo a un handle di file restituito dalla funzione della libreria di runtime C di FOPE o a un handle di finestra restituito dalla funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) .

Come con questi handle, l'applicazione non è in grado di accedere e modificare direttamente le informazioni nell'handle di binding. Le informazioni contenute in una struttura dei dati dell'handle di associazione sono disponibili solo per le librerie di runtime RPC. È possibile specificare l'handle, le librerie di runtime per accedere e modificare i dati appropriati.

Questa sezione presenta una discussione sugli handle di binding negli argomenti seguenti:

-   [Tipi di handle di associazione](types-of-binding-handles.md)
-   [Binding lato client](client-side-binding.md)
-   [Binding lato server](server-side-binding.md)
-   [Handle con binding completo e parziale](fully-and-partially-bound-handles.md)
-   [Interpretazione delle informazioni di binding](interpreting-binding-information.md)
-   [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md)
-   [Funzioni di binding-handle](binding-handle-functions.md)
-   [Il database del servizio nome RPC](the-rpc-name-service-database.md)

 

 