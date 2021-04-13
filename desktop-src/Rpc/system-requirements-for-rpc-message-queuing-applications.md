---
title: Requisiti di sistema per le applicazioni di Accodamento RPC-Message
description: Per utilizzare il trasporto di Accodamento messaggi in un'applicazione client/server RPC, è necessario che nei computer server e client siano installate la piattaforma del sistema operativo e il software di Accodamento messaggi appropriati.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1274c888506a6868eb7ded5ba96c5f1ea8dc8b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399538"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a>Requisiti di sistema per le applicazioni di Accodamento RPC-Message

Per utilizzare il trasporto di Accodamento messaggi in un'applicazione client/server RPC, è necessario che nei computer server e client siano installate la piattaforma del sistema operativo e il software di Accodamento messaggi appropriati.

I requisiti per i computer server sono:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o versione successiva.
-   SQL Server versione 6,5 o successiva.
-   Controller aziendale primario di Accodamento messaggi o controller del sito primario.
-   DLL di trasporto lato server RPC (RpcMqSvr.dll).

I requisiti per i computer client sono:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o versione successiva.
-   Microsoft Message Queuing client.
-   DLL di trasporto lato client RPC (RpcMqCl.dll).

Quando i componenti MSMQ sono installati nei computer client e server, i registri di sistema vengono automaticamente configurati per includere il protocollo di trasporto di Accodamento messaggi di [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq) per le chiamate di procedure remote.

Per compilare l'applicazione RPC-MSMQ, è necessario quanto segue:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o versione successiva
-   MIDL versione 3.1.76 o successiva.

 

 