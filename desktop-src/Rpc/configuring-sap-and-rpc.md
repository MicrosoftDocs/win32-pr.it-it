---
title: Configurazione di SAP e RPC
description: I server di rete Novell NetWare usano Service Advertising Protocol (SAP) per trasmettere informazioni sui servizi disponibili in rete ad altri dispositivi di rete.
ms.assetid: 6d6ef481-fc09-4795-8954-33329912ff4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf75a9ab45e97a66f1fc8d796b1d288367bb1c8d0e04b2ace4a90de7e21cbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931684"
---
# <a name="configuring-sap-and-rpc"></a>Configurazione di SAP e RPC

I server di rete Novell NetWare usano Service Advertising Protocol (SAP) per trasmettere informazioni sui servizi disponibili in rete ad altri dispositivi di rete. Un server può inviare una trasmissione SAP ogni 60 secondi per informare altri dispositivi di rete sui servizi che offre. Le workstation usano i criteri di accesso condiviso per trovare i servizi necessari nella rete.

Windows include un servizio SAP Agent per consentire Windows server basati su Windows interagire con i server NetWare. Il servizio SAP Agent sarà in ascolto delle richieste SAP dei client di rete per i servizi basati su IPX installati e in esecuzione nel server.

Il software progettato per essere annunciato come servizio in rete tramite una trasmissione SAP emettere gli annunci SAP ogni 60 secondi, senza installare l'agente SAP. Tuttavia, per consentire ai client di rete di individuare rapidamente un servizio di rete IPX, un server che gestisce un database del servizio deve essere disponibile in rete per rispondere alla richiesta di posizione del servizio. Questo database del servizio viene in genere gestito da un server Novell NetWare o compatibile con NetWare. Servizi file e stampa Microsoft per NetWare manterrà anche un database del servizio di rete IPX.

In un computer che esegue Windows Server, se è installato Gateway Services for NetWare (GSNW), un tipo SAP 640 verrà trasmesso ogni 60 secondi dal servizio RPC (Remote Procedure Call). Questa trasmissione SAP continuerà anche se l'utente disabilita GSNW e il servizio SAP Agent.

Il servizio RPC farà la trasmissione SAP se sono installati i servizi client per NetWare (CSNW) e il servizio AGENTE SAP. Questa trasmissione SAP continuerà anche se l'utente disabilita l'agente SAP.

Per impostazione predefinita, il servizio RPC verifica la presenza di Servizi gateway per NetWare e del servizio AGENTE SAP nel computer che esegue Windows Server. L'installazione di Servizi file e stampa per NetWare consente di installare un agente SAP.

Nel computer che esegue una versione client di Windows con CSNW, il servizio RPC controlla il servizio SAP Agent. Se i servizi sono presenti, RPC avvia il proprio thread che esegue il tipo di trasmissione SAP 640 ogni minuto.

> [!NOTE]
> Se non si vogliono trasmissioni SAP in rete ogni 60 secondi, è possibile disabilitare le trasmissioni SAP usando l'editor del Registro di sistema. Si noti che l'uso non corretto dell'editor del Registro di sistema può causare gravi problemi che potrebbero richiedere la reinstallazione del sistema operativo. Microsoft non garantisce che i problemi dovuti all'utilizzo errato dell'Editor del Registro di sistema possano essere risolti. L'uso dell'editor del Registro di sistema è a rischio e pericolo dell'utente. È necessario eseguire il backup del Registro di sistema prima di modificarlo.

 

**Per configurare per SAP**

1.  Eseguire l'editor del Registro di Regedt32.exe e passare alla chiave seguente nel Registro di sistema:

    **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ RPC**

2.  Scegliere **Aggiungi** valore **dal** menu Modifica e usare la voce seguente:
    1.  Nome valore: AdvertiseRpcService
    2.  Tipo di dati: REG \_ SZ
    3.  Stringa: No
3.  Se si usa No per la stringa, la trasmissione SAP RPC viene disattivata. L'uso di Sì per la stringa attiva la trasmissione SAP RPC.
4.  Riavviare il computer per l'applicazione della modifica al Registro di sistema.
    > [!NOTE]
    > Se le trasmissioni SAP continuano dopo aver seguito questa procedura, è possibile provare un passaggio per la risoluzione dei problemi. Eliminare il **valore della stringa \_ spx Ncacn** nella chiave del Registro di sistema seguente:
    >
    > **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Rpc \\ ServerProtocols\\**

     

> [!NOTE]  
> Deve essere usato solo come passaggio per la risoluzione dei problemi. L'eliminazione di questo valore stringa disabilita completamente le trasmissioni SAP che potrebbero essere necessarie per il corretto funzionamento di alcuni programmi.