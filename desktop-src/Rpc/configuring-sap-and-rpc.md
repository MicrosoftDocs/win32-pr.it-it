---
title: Configurazione di SAP e RPC
description: I server di rete Novell NetWare utilizzano il Service Advertising Protocol (SAP) per trasmettere informazioni sui servizi disponibili sulla rete ad altri dispositivi di rete.
ms.assetid: 6d6ef481-fc09-4795-8954-33329912ff4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385d60168a52cbe5d31368959ec4f21d52f9ad80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/15/2019
ms.locfileid: "104397038"
---
# <a name="configuring-sap-and-rpc"></a>Configurazione di SAP e RPC

I server di rete Novell NetWare utilizzano il Service Advertising Protocol (SAP) per trasmettere informazioni sui servizi disponibili sulla rete ad altri dispositivi di rete. Un server può inviare una trasmissione SAP ogni 60 secondi per informare altri dispositivi di rete sui servizi offerti. Le workstation utilizzano i succhi per trovare i servizi necessari sulla rete.

Windows include un servizio agente SAP per consentire ai server basati su Windows di interagire con i server NetWare. Il servizio agente SAP resterà in ascolto delle richieste SAP dei client di rete per i servizi basati su IPX installati e in esecuzione nel server.

Il software progettato per essere annunciato come servizio in rete tramite una trasmissione SAP emetterà gli annunci SAP ogni 60 secondi, senza che sia installato l'agente SAP. Tuttavia, per consentire ai client di rete di individuare rapidamente un servizio di rete IPX, un server che gestisce un database del servizio deve essere disponibile in rete per rispondere alla richiesta di individuazione del servizio. Questo database del servizio viene in genere gestito da un server Novell NetWare o compatibile con NetWare. I servizi file e stampa Microsoft per NetWare gestiranno anche un database del servizio di rete IPX.

In un computer che esegue Windows Server, se è installato Gateway Services for NetWare (GSNW), un tipo SAP 640 verrà trasmesso ogni 60 secondi dal servizio RPC (Remote Procedure Call). Questa trasmissione SAP continuerà anche se l'utente disabilita il GSNW e il servizio SAP Agent.

Il servizio RPC eseguirà la trasmissione SAP se i servizi client per NetWare (CSNW) e il servizio SAP Agent sono installati. Questa trasmissione SAP continuerà anche se l'utente disabilita l'agente SAP.

Per impostazione predefinita, il servizio RPC verificherà la presenza di servizi gateway per NetWare e del servizio agente SAP nel computer che esegue Windows Server. Con l'installazione di servizi file e stampa per NetWare viene installato un agente SAP.

Nel computer in cui è in esecuzione una versione client di Windows con CSNW, il servizio RPC controlla il servizio agente SAP. Se i servizi sono presenti, RPC avvierà il proprio thread che eseguirà il tipo di trasmissione SAP 640 ogni minuto.

> [!NOTE]
> Se non si vuole trasmettere le trasmissioni SAP sulla rete ogni 60 secondi, è possibile disabilitare le trasmissioni SAP usando l'editor del registro di sistema. Tenere presente che l'utilizzo errato dell'editor del registro di sistema può causare gravi problemi che potrebbero richiedere la reinstallazione del sistema operativo. Microsoft non garantisce che i problemi dovuti all'utilizzo errato dell'Editor del Registro di sistema possano essere risolti. L'uso dell'editor del Registro di sistema è a rischio e pericolo dell'utente. È consigliabile eseguire il backup del registro di sistema prima di modificarlo.

 

**Per configurare per SAP**

1.  Eseguire l'editor del registro di sistema (Regedt32.exe) e passare alla chiave seguente nel registro di sistema:

    **HKEY \_ \_ computer locale \\ software \\ Microsoft \\ RPC**

2.  Scegliere **Aggiungi valore** dal menu **modifica** e utilizzare la voce seguente:
    1.  Nome valore: AdvertiseRpcService
    2.  Tipo di dati: REG \_ SZ
    3.  Stringa: No
3.  L'uso di no per la stringa Disattiva la trasmissione di SAP RPC. Se si usa Sì per la stringa, viene attivata la trasmissione di SAP RPC.
4.  Riavviare il computer per rendere effettive le modifiche del registro di sistema.
    > [!NOTE]
    > Se le trasmissioni SAP continuano dopo aver seguito questa procedura, è possibile provare a eseguire un passaggio di risoluzione dei problemi. Eliminare il valore stringa **ncacn \_ SPX** nella seguente chiave del registro di sistema:
    >
    > **HKEY \_ \_ computer locale \\ software \\ Microsoft \\ RPC \\ ServerProtocols\\**

     

> [!NOTE]  
> Questa operazione deve essere usata solo come passaggio per la risoluzione dei problemi. L'eliminazione di questo valore stringa Disabilita completamente le trasmissioni SAP che potrebbero essere necessarie per alcuni programmi per funzionare correttamente.