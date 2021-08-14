---
description: Gestione sincronizzazione include componenti dell'interfaccia utente, ad esempio le finestre di dialogo a schede nel servizio SyncMgr, le finestre di dialogo di errore e le finestre di dialogo di stato.
title: Architettura di Gestione sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.assetid: db338835-ca8d-4e9f-973a-8eb081feda2b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 584329a06ee9df80558d9961b734b62a57d5ebccd83f200690812fa99132b06d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451867"
---
# <a name="synchronization-manager-architecture"></a>Architettura di Gestione sincronizzazione

Gestione sincronizzazione include componenti dell'interfaccia utente, ad esempio le finestre di dialogo a schede nel servizio SyncMgr, le finestre di dialogo di errore e le finestre di dialogo di stato. Con i componenti dell'interfaccia utente l'utente finale può pianificare le applicazioni per la sincronizzazione e configurare la sincronizzazione automatica in modo che si verifichi insieme agli eventi di sistema specificati. Ad esempio, SyncMgr può essere richiamato all'accesso utente o all'arresto del sistema. L'utente può anche richiamare una sincronizzazione manuale.

L'utente seleziona un'applicazione e specifica gli elementi all'interno dell'applicazione da sincronizzare e imposta un evento trigger. Ad esempio, all'interno di un'applicazione di posta elettronica, la posta in arrivo, la posta in uscita o un'altra cartella contenente messaggi può essere un elemento separato per l'applicazione.

SyncMgr include anche un'interfaccia di programmazione in modo che le applicazioni possano registrarsi per usare le funzionalità di sincronizzazione, elaborare gli errori e ricevere informazioni sullo stato e notifiche durante il processo di sincronizzazione.

 

 



