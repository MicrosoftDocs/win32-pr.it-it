---
title: Installazione e configurazione di applicazioni RPC
description: Quando il sistema operativo Microsoft Windows è installato in un server o in un client, il programma di installazione installa automaticamente i file di runtime RPC.
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- Remote Procedure Call RPC, attività, installazione e configurazione di applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90837261c571276a74bb3a5354c7b9a5db2da6cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471758"
---
# <a name="installing-and-configuring-rpc-applications"></a>Installazione e configurazione di applicazioni RPC

Quando il sistema operativo Microsoft Windows è installato in un server o in un client, il programma di installazione installa automaticamente i file di runtime RPC. Non è richiesta alcuna ulteriore installazione RPC. È tuttavia necessario assicurarsi che la versione di Windows installata supporti tutte le funzionalità utilizzate nell'applicazione distribuita.

Quando si utilizza un'applicazione RPC in un sistema operativo Windows 3. x o Microsoft MS-DOS, è necessario copiare i file eseguibili della fase di esecuzione RPC nei computer Windows 3. x o MS-DOS che utilizzeranno l'applicazione. La directory \\ mstools \\ RPC \_ RT16 nel CD di Platform Software Development Kit (SDK) contiene un'immagine del disco di questi file insieme a un programma di installazione per installare i file. Usare questa immagine del disco per creare un disco di installazione per la distribuzione con l'applicazione RPC. È anche possibile usare applicazioni client a 16 bit destinate a MS-DOS o Windows in un sistema operativo Windows a 32 bit o a 64 bit. Tuttavia, il programma di installazione dell'applicazione deve installare i file eseguibili contenuti in questa immagine del disco.

Quando si compila un'applicazione RPC per un client Macintosh, è necessario collegare i file necessari all'applicazione in fase di compilazione. Non è necessaria alcuna installazione RPC aggiuntiva.

Per ulteriori informazioni sui file ridistribuibili e sui contratti di licenza, vedere \\ licenza \\Redist.txt e \\ \\License.txt di licenza nel CD di Platform SDK.

In questa sezione vengono fornite informazioni sulla configurazione di applicazioni RPC in un'ampia gamma di piattaforme hardware e software. Viene presentata la discussione nelle seguenti sezioni:

-   [Configurazione del provider di servizi dei nomi](configuring-the-name-service-provider.md)
-   [Informazioni registro di sistema](registry-information.md)
-   [Uso di RPC con proxy Winsock](using-rpc-with-winsock-proxy.md)
-   [Installazione di SPX/IPX](spx-ipx-installation.md)
-   [Configurazione del server di sicurezza](configuring-the-security-server.md)

 

 




