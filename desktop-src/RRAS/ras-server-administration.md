---
title: Amministrazione del server RAS
description: Windows NT Server 4,0 fornisce un set di funzioni per l'amministrazione delle autorizzazioni e delle porte utente nei server RAS Windows NT/Windows 2000.
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- Amministrazione del server, RAS
- Amministrazione, server RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e096610e1cfe986c504a017f4d2b0d1033a6e6d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221880"
---
# <a name="ras-server-administration"></a>Amministrazione del server RAS

Windows NT Server 4,0 fornisce un set di funzioni per l'amministrazione delle autorizzazioni e delle porte utente nei server RAS Windows NT/Windows 2000. Windows 95 non supporta queste funzioni. Utilizzando queste funzioni, è possibile sviluppare un'applicazione di amministrazione del server RAS per eseguire le attività seguenti:

-   Enumerare gli utenti che dispongono di un set specificato di autorizzazioni RAS
-   Assegnare o revocare le autorizzazioni RAS per un utente specificato
-   Enumerare le porte configurate in un server RAS
-   Ottenere informazioni e statistiche su una porta specificata in un server RAS
-   Reimposta i contatori delle statistiche per una porta specificata
-   Disconnettere una porta specificata

È inoltre possibile installare una DLL di amministrazione del server RAS per il controllo delle connessioni utente e l'assegnazione di indirizzi IP agli utenti con connessione remota. La DLL esporta un set di funzioni che il server RAS chiama ogni volta che un utente tenta di connettersi o disconnettersi.

 

 




