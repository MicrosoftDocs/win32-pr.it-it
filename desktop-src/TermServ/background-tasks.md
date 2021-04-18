---
title: Linee guida per le attività in background in Servizi Desktop remoto
description: Per ottimizzare la disponibilità della CPU per tutti gli utenti, disabilitare le attività in background durante l'esecuzione in un ambiente Servizi Desktop remoto o creare attività in background efficienti che non richiedono un uso intensivo delle risorse.
ms.assetid: c3688319-dbe7-4be5-8895-622a8f8797d2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b93169b248fb086b7ccad88aa57c0feae171f91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297989"
---
# <a name="guidelines-for-background-tasks-in-remote-desktop-services"></a>Linee guida per le attività in background in Servizi Desktop remoto

Attività in background: le attività eseguite quando il ciclo di messaggi di un'applicazione è inattivo, forniscono un meccanismo per gestire le attività con priorità bassa in un ambiente con un singolo utente. In un ambiente di Servizi Desktop remoto, tuttavia, un'attività in background di un utente compete per i cicli della CPU con le attività in primo piano di un altro utente. Quando più utenti eseguono attività in primo piano e in background, le richieste di CPU sono molto più elevate rispetto a quando tutti gli utenti eseguono solo attività in primo piano. Per ottimizzare la disponibilità della CPU per tutti gli utenti, disabilitare le attività in background durante l'esecuzione in un ambiente Servizi Desktop remoto o creare attività in background efficienti che non richiedono un uso intensivo delle risorse.

Per ulteriori informazioni, vedere [rilevamento dell'ambiente Servizi Desktop remoto](detecting-the-terminal-services-environment.md). Dopo aver rilevato l'ambiente di Servizi Desktop remoto, è possibile disabilitare o riconfigurare le attività in background per l'applicazione usando lo stesso set di API usato per gestire le attività.

 

 




