---
title: Installazione e configurazione di applicazioni RPC
description: Quando microsoft Windows sistema operativo è installato in un server o client, il programma di installazione installa automaticamente i file di run-time RPC.
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- RPC Remote Procedure Call , attività, installazione e configurazione di applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5cf5d408e2b23042074031ce0307b3a13cf3461df31cc39899b0315f99e8c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020441"
---
# <a name="installing-and-configuring-rpc-applications"></a>Installazione e configurazione di applicazioni RPC

Quando microsoft Windows sistema operativo è installato in un server o client, il programma di installazione installa automaticamente i file di run-time RPC. Non sono necessarie altre installazioni RPC. È tuttavia necessario assicurarsi che la versione di Windows installata supporti tutte le funzionalità usate nell'applicazione distribuita.

Quando si usa un'applicazione RPC in un sistema operativo Windows 3.x o Microsoft MS-DOS, è necessario copiare i file eseguibili di run-time RPC nei computer Windows 3.x o MS-DOS che useranno l'applicazione. La directory mstools rpc rt16 nel CD di \\ Platform Software Development Kit \\ (SDK) contiene un'immagine disco di questi file insieme a un programma di installazione per \_ installare i file. Usare questa immagine disco per creare un disco di installazione per la distribuzione con l'applicazione RPC. È anche possibile usare applicazioni client a 16 bit destinate a MS-DOS o Windows in un sistema operativo Windows a 32 bit/64 bit. Tuttavia, il programma di installazione dell'applicazione deve installare i file eseguibili contenuti in questa immagine disco.

Quando si compila un'applicazione RPC per un client Macintosh, è necessario collegare i file necessari all'applicazione in fase di compilazione. Non è necessaria alcuna installazione RPC aggiuntiva.

Per altre informazioni sui file ridistribuibili e sui contratti di licenza, vedere LICENSERedist.txt e LICENSELicense.txt nel CD \\ \\ di Platform \\ \\ SDK.

Questa sezione contiene informazioni sulla configurazione di applicazioni RPC in un'ampia gamma di piattaforme hardware e software. Presenta la discussione nelle sezioni seguenti:

-   [Configurazione del provider di servizi dei nomi](configuring-the-name-service-provider.md)
-   [Informazioni del Registro di sistema](registry-information.md)
-   [Uso di RPC con il proxy Winsock](using-rpc-with-winsock-proxy.md)
-   [Installazione di SPX/IPX](spx-ipx-installation.md)
-   [Configurazione del server di sicurezza](configuring-the-security-server.md)

 

 




