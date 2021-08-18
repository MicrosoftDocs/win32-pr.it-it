---
title: API Servizi Desktop remoto
description: L Servizi Desktop remoto aPI è particolarmente utile per le applicazioni client/server e le applicazioni per Servizi Desktop remoto amministrazione.
ms.assetid: 4bd10a15-78d6-4754-9e17-f2576ee8b9d0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbdaff1f09a0de3fad20f4de334af1030c52e16ef795b1ece51cdaead639825a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000111"
---
# <a name="remote-desktop-services-api"></a>API Servizi Desktop remoto

La maggior parte delle applicazioni viene eseguita senza modifiche in un ambiente Servizi Desktop remoto (noto in precedenza come Servizi terminal) e non è necessario usare l'API Servizi Desktop remoto. L Servizi Desktop remoto aPI è particolarmente utile per le applicazioni client/server e le applicazioni per Servizi Desktop remoto amministrazione.

L Servizi Desktop remoto API è un set di chiamate di funzione Wtsapi32.dll. Per progettare l'applicazione per l'esecuzione in ambienti Servizi Desktop remoto e non Servizi Desktop remoto, usare il collegamento dinamico in fase di esecuzione per verificare la presenza di Wtsapi32.dll. Per altre informazioni, vedere [Collegamento in fase di esecuzione Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

L Servizi Desktop remoto API consente alle applicazioni di eseguire le attività seguenti in un Servizi Desktop remoto ambiente:

-   [Servizi Desktop remoto,](terminal-services-administration.md)ad esempio l'enumerazione e la gestione di server Host sessione Desktop remoto (precedentemente noti come server terminal) in un dominio o l'enumerazione e la gestione di sessioni e processi in un server Host sessione Desktop remoto.
-   Miglioramento delle applicazioni client/server in un Servizi Desktop remoto locale.
-   Uso [Servizi Desktop remoto canali virtuali per](terminal-services-virtual-channels.md) comunicare tra i moduli client e server di un'applicazione.
-   [Impostazione e recupero di Servizi Desktop remoto di configurazione utente specifiche](terminal-services-user-configuration.md).

 

 




