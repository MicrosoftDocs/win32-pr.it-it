---
title: Teoria del controllo delle versioni per RPC e COM
description: Teoria del controllo delle versioni per RPC (Remote Procedure Call) e COM.
ms.assetid: c4df0a7b-e1be-481d-9149-317ffc9179b9
keywords:
- RPC, procedure consigliate, controllo delle versioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e03b23c91bf69fbc3c4f72366b80812fd54330d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118227"
---
# <a name="the-versioning-theory-for-rpc-and-com"></a>Teoria del controllo delle versioni per RPC e COM

Solo due metodi completamente infallibili supportano nuove funzionalità senza rischiare problemi di compatibilità con i fili:

-   Modificare la versione dell'interfaccia in base alle regole; in questo modo si impedisce che i nuovi client comunicano con un server precedente e possano o meno impedire a un vecchio client di comunicare con il nuovo server. Questa operazione viene chiarita più avanti in questa sezione.
-   Introduce un'interfaccia diversa che riguarda la nuova funzionalità.

Un'interfaccia RPC standard è identificata da una combinazione di numero di versione e GUID; un'interfaccia COM è identificata dal relativo GUID. La versione è costituita dalle parti principali e secondarie. Per le interfacce standard con lo stesso GUID e numeri di versione diversi, una connessione è possibile solo quando la versione principale è la stessa e il client non è superiore alla versione secondaria del server.

Una conseguenza è che la modifica del GUID dell'interfaccia RPC interrompe la compatibilità di rete, mentre la modifica del nome dell'interfaccia non lo è.

In RPC standard, un percorso per gli aggiornamenti e le estensioni è ben definito e richiede fondamentalmente che i nuovi metodi vengano aggiunti alla fine dell'interfaccia e i nuovi tipi vengano utilizzati solo nei nuovi metodi. Se tali aggiunte sono necessarie, è necessario aumentare la versione secondaria. Eventuali altre modifiche richiedono una modifica nella versione principale, poiché il software client e server non sarebbero compatibili in rete. L'adesione a queste regole garantisce che ogni volta che si verifica una connessione tra un nuovo client e un server precedente o viceversa, entrambi i lati sono completamente compatibili.

Per un'interfaccia COM, non è possibile usare l'attributo Version. La creazione di nuove interfacce e l'ereditarietà delle interfacce precedenti è un equivalente della modifica della versione in RPC. In genere, l'approccio migliore in COM consiste nel creare una nuova interfaccia per la funzionalità espansa. Un equivalente della versione secondaria è la nuova interfaccia che eredita da quella precedente. Per modificare metodi obsoleti o tipi di dati obsoleti è necessaria un'interfaccia COM completamente nuova, ovvero un'interfaccia che non eredita da quella precedente.

Per COM, la funzione [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) è un metodo stabilito per verificare se un server supporta un'interfaccia; di conseguenza, le situazioni in cui un client può comunicare con una versione precedente o una nuova di un'interfaccia può essere risolta facilmente.

 

 