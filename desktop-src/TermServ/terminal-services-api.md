---
title: API Servizi Desktop remoto
description: L'API Servizi Desktop remoto è particolarmente utile per le applicazioni client/server e le applicazioni per Servizi Desktop remoto l'amministrazione.
ms.assetid: 4bd10a15-78d6-4754-9e17-f2576ee8b9d0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5aa187378625242463ea91151a6961b08d2a77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855901"
---
# <a name="remote-desktop-services-api"></a>API Servizi Desktop remoto

La maggior parte delle applicazioni viene eseguita senza modifiche in un ambiente di Servizi Desktop remoto (noto in precedenza come servizi Terminal) e non è necessario usare l'API Servizi Desktop remoto. L'API Servizi Desktop remoto è particolarmente utile per le applicazioni client/server e le applicazioni per Servizi Desktop remoto l'amministrazione.

L'API Servizi Desktop remoto è un set di chiamate di funzione in Wtsapi32.dll. Per progettare l'applicazione per l'esecuzione in ambienti Servizi Desktop remoto e non Servizi Desktop remoto, utilizzare il collegamento dinamico in fase di esecuzione per verificare la presenza di Wtsapi32.dll. Per ulteriori informazioni, vedere il [collegamento di run-time a Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

L'API Servizi Desktop remoto consente alle applicazioni di eseguire le attività seguenti in un ambiente Servizi Desktop remoto:

-   [Servizi Desktop remoto amministrazione](terminal-services-administration.md), ad esempio l'enumerazione e la gestione di server di host sessione Desktop remoto (host sessione Desktop remoto) (noti in precedenza come Terminal Server) in un dominio o l'enumerazione e la gestione di sessioni e processi in un server Host sessione Desktop remoto.
-   Miglioramento delle applicazioni client/server in un ambiente Servizi Desktop remoto.
-   Uso di [Servizi Desktop remoto canali virtuali](terminal-services-virtual-channels.md) per la comunicazione tra i moduli client e server di un'applicazione.
-   [Impostazione e recupero di Servizi Desktop remoto informazioni di configurazione utente specifiche](terminal-services-user-configuration.md).

 

 




