---
title: Teoria del controllo delle versioni per RPC e COM
description: Teoria del controllo delle versioni per RPC (Remote Procedure Call) e COM.
ms.assetid: c4df0a7b-e1be-481d-9149-317ffc9179b9
keywords:
- RPC remote procedure call, procedure consigliate, controllo delle versioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3681ce1290b7653c28b12c09c93d21de3052e0e6137ed5c6f906afd42f8d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016381"
---
# <a name="the-versioning-theory-for-rpc-and-com"></a>Teoria del controllo delle versioni per RPC e COM

Solo due metodi completamente infallivi supportano nuove funzionalità senza il rischio di problemi di compatibilità dei cavi:

-   Modificare la versione dell'interfaccia in base alle regole. ciò impedisce ai nuovi client di comunicare con un server precedente e può o meno impedire a un client precedente di comunicare con il nuovo server. Questa operazione viene chiarita più avanti in questa sezione.
-   Introdurre un'interfaccia diversa che si occupa della nuova funzionalità.

Un'interfaccia RPC standard è identificata da una combinazione di GUID e numero di versione. un'interfaccia COM è identificata dal relativo GUID. La versione è costituita da parti principali e secondarie. Per le interfacce standard con lo stesso GUID e numeri di versione diversi, una connessione è possibile solo quando la versione principale è la stessa e il client non è superiore alla versione secondaria del server.

Una conseguenza è che la modifica del GUID dell'interfaccia RPC interrompe la compatibilità dei cavi, mentre la modifica del nome dell'interfaccia non lo fa.

In RPC standard, un percorso per gli aggiornamenti e le estensioni è ben definito e richiede fondamentalmente l'aggiunta di nuovi metodi solo alla fine dell'interfaccia e l'uso di nuovi tipi solo nei nuovi metodi. Se sono necessarie aggiunte di questo tipo, è necessario aumentare la versione secondaria. Qualsiasi altra modifica richiede una modifica nella versione principale, perché il software client e server sarebbe incompatibile in transito. L'aderenza a queste regole garantisce ogni volta che esiste una connessione tra un nuovo client e un server precedente o viceversa, entrambi i lati sono completamente compatibili.

Per un'interfaccia COM, non è possibile usare l'attributo version. La creazione di nuove interfacce e l'ereditarietà dalle interfacce vecchie equivale a modificare la versione in RPC. In genere, l'approccio migliore in COM consiste nel creare una nuova interfaccia per la funzionalità espansa. Un equivalente della versione secondaria è la nuova interfaccia che eredita da quella precedente. La modifica di metodi o tipi di dati vecchi richiede un'interfaccia COM completamente nuova, ovvero un'interfaccia che non eredita da quella precedente.

Per COM, la [**funzione QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) è un metodo stabilito per controllare se un server supporta un'interfaccia. Di conseguenza, è possibile risolvere facilmente le situazioni in cui un client può parlare con una versione precedente o una nuova di un'interfaccia.

 

 