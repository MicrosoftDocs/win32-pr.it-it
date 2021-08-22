---
title: Handle di associazione
description: L'associazione è il processo di creazione di una connessione logica tra un programma client e un programma server. Le informazioni che costituiscono l'associazione tra client e server sono rappresentate da una struttura denominata handle di associazione.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09eae434fde790531a6f723cab6dc0b0613ee2fc99d680478d697cb550d6a18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932341"
---
# <a name="binding-handles"></a>Handle di associazione

L'associazione è il processo di creazione di una connessione logica tra un programma client e un programma server. Le informazioni che costituiscono l'associazione tra client e server sono rappresentate da una struttura denominata handle di associazione.

Un handle di associazione è analogo a un handle di file restituito dalla funzione fopen della libreria di runtime C o a un handle di finestra restituito [**dalla funzione CreateWindow.**](/windows/win32/api/winuser/nf-winuser-createwindowa)

Come per questi handle, l'applicazione non può accedere e modificare direttamente le informazioni nell'handle di associazione. Le informazioni in una struttura di dati dell'handle di associazione sono disponibili solo per le librerie di runtime RPC. L'handle viene fornito, le librerie di runtime accedono e modificano i dati appropriati.

Questa sezione presenta una discussione sugli handle di associazione negli argomenti seguenti:

-   [Tipi di handle di associazione](types-of-binding-handles.md)
-   [Associazione lato client](client-side-binding.md)
-   [Associazione lato server](server-side-binding.md)
-   [Handle completamente e parzialmente associati](fully-and-partially-bound-handles.md)
-   [Interpretazione delle informazioni di associazione](interpreting-binding-information.md)
-   [Estensioni Binding-Handle RPC Microsoft](microsoft-rpc-binding-handle-extensions.md)
-   [Funzioni di handle di associazione](binding-handle-functions.md)
-   [Database del servizio nomi RPC](the-rpc-name-service-database.md)

 

 