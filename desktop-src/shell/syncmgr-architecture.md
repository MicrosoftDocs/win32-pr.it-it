---
description: Gestione sincronizzazione include i componenti dell'interfaccia utente, ad esempio le finestre di dialogo a schede nel servizio SyncMgr, le finestre di dialogo di errore e le finestre di dialogo di stato.
title: Architettura di gestione sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.assetid: db338835-ca8d-4e9f-973a-8eb081feda2b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f178b407c1f7d568c9de2ce7c81d937e7d1cdef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760508"
---
# <a name="synchronization-manager-architecture"></a>Architettura di gestione sincronizzazione

Gestione sincronizzazione include i componenti dell'interfaccia utente, ad esempio le finestre di dialogo a schede nel servizio SyncMgr, le finestre di dialogo di errore e le finestre di dialogo di stato. Con i componenti dell'interfaccia utente, l'utente finale può pianificare le applicazioni per la sincronizzazione e impostare la sincronizzazione automatica affinché venga eseguita insieme a eventi di sistema specificati. Ad esempio, SyncMgr può essere richiamato all'accesso dell'utente o all'arresto del sistema. L'utente può anche richiamare una sincronizzazione manuale.

L'utente seleziona un'applicazione e specifica gli elementi all'interno dell'applicazione da sincronizzare e imposta un evento trigger. Ad esempio, all'interno di un'applicazione di posta elettronica, la posta in arrivo, la posta in uscita o altre cartelle contenenti messaggi possono essere un elemento separato per l'applicazione.

SyncMgr include inoltre un'interfaccia di programmazione che consente alle applicazioni di registrarsi per l'utilizzo delle funzionalità di sincronizzazione, può elaborare errori e ricevere informazioni sullo stato di avanzamento e notifiche durante il processo di sincronizzazione.

 

 



