---
title: Linee guida per le attività in background in Servizi Desktop remoto
description: Per ottimizzare la disponibilità della CPU per tutti gli utenti, disabilitare le attività in background durante l'esecuzione in un ambiente Servizi Desktop remoto o creare attività in background efficienti che non richiedono un uso intensivo delle risorse.
ms.assetid: c3688319-dbe7-4be5-8895-622a8f8797d2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c19590d32db21ad08e1d31cbe02e0850bd0964282c8f709207837c3c2a638a12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131290"
---
# <a name="guidelines-for-background-tasks-in-remote-desktop-services"></a>Linee guida per le attività in background in Servizi Desktop remoto

Le attività in background, ovvero le attività eseguite quando il ciclo di messaggi di un'applicazione è inattivo, forniscono un meccanismo per la gestione delle attività con priorità bassa in un ambiente a utente singolo. In un Servizi Desktop remoto, tuttavia, un'attività in background di un utente compete per i cicli della CPU con le attività in primo piano di un altro utente. Quando più utenti eseguono attività in primo piano e in background, le richieste di CPU sono molto più elevate rispetto a quando tutti gli utenti eseguono solo attività in primo piano. Per ottimizzare la disponibilità della CPU per tutti gli utenti, disabilitare le attività in background durante l'esecuzione in un ambiente Servizi Desktop remoto o creare attività in background efficienti che non richiedono un uso intensivo delle risorse.

Per altre informazioni, vedere [Detecting the Servizi Desktop remoto environment](detecting-the-terminal-services-environment.md). Dopo aver rilevato l'ambiente Servizi Desktop remoto, è possibile disabilitare o riconfigurare le attività in background per l'applicazione usando lo stesso set di API usato per gestire le attività.

 

 




