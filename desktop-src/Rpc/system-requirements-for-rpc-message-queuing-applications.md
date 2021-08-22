---
title: Requisiti di sistema per RPC-Message applicazioni di accodamento
description: Per utilizzare il trasporto di accodamento messaggi in un'applicazione client/server RPC, nei computer server e client devono essere installati la piattaforma del sistema operativo e il software di accodamento messaggi appropriati.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46d9775e720c725ad3b0d06a0be0cf67aa438f739c6a0d1162f4940ac59e561e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924648"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a>Requisiti di sistema per RPC-Message applicazioni di accodamento

Per utilizzare il trasporto di accodamento messaggi in un'applicazione client/server RPC, nei computer server e client devono essere installati la piattaforma del sistema operativo e il software di accodamento messaggi appropriati.

I requisiti per i computer server sono:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o versione successiva.
-   SQL Server versione 6.5 o successiva.
-   Controller del sito primario Enterprise accodamento messaggi o controller del sito primario.
-   DLL di trasporto lato server RPC (RpcMqSvr.dll).

I requisiti per i computer client sono:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o versione successiva.
-   Microsoft Message Queuing Client.
-   DLL di trasporto lato client RPC (RpcMqCl.dll).

Quando i componenti MSMQ vengono installati nei computer client e server, i registri di sistema vengono configurati automaticamente per includere il protocollo di trasporto [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq) message-queuing per le chiamate di procedura remota.

Per compilare l'applicazione RPC-MSMQ, sono necessari gli elementi seguenti:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o versione successiva
-   MIDL versione 3.1.76 o successiva.

 

 