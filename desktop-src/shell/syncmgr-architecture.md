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
# <a name="synchronization-manager-architecture"></a><span data-ttu-id="29284-103">Architettura di gestione sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="29284-103">Synchronization Manager Architecture</span></span>

<span data-ttu-id="29284-104">Gestione sincronizzazione include i componenti dell'interfaccia utente, ad esempio le finestre di dialogo a schede nel servizio SyncMgr, le finestre di dialogo di errore e le finestre di dialogo di stato.</span><span class="sxs-lookup"><span data-stu-id="29284-104">The Synchronization Manager includes user interface components, such as the tabbed dialog boxes in the SyncMgr service, error dialogs, and progress dialogs.</span></span> <span data-ttu-id="29284-105">Con i componenti dell'interfaccia utente, l'utente finale può pianificare le applicazioni per la sincronizzazione e impostare la sincronizzazione automatica affinché venga eseguita insieme a eventi di sistema specificati.</span><span class="sxs-lookup"><span data-stu-id="29284-105">With the user interface components the end user can schedule applications for synchronization and set up automatic synchronization to occur in conjunction with specified system events.</span></span> <span data-ttu-id="29284-106">Ad esempio, SyncMgr può essere richiamato all'accesso dell'utente o all'arresto del sistema.</span><span class="sxs-lookup"><span data-stu-id="29284-106">For example, the SyncMgr can be invoked at user logon or system shutdown.</span></span> <span data-ttu-id="29284-107">L'utente può anche richiamare una sincronizzazione manuale.</span><span class="sxs-lookup"><span data-stu-id="29284-107">The user can also invoke a manual synchronization.</span></span>

<span data-ttu-id="29284-108">L'utente seleziona un'applicazione e specifica gli elementi all'interno dell'applicazione da sincronizzare e imposta un evento trigger.</span><span class="sxs-lookup"><span data-stu-id="29284-108">The user selects an application and specifies the items within the application to be synchronized and sets a trigger event.</span></span> <span data-ttu-id="29284-109">Ad esempio, all'interno di un'applicazione di posta elettronica, la posta in arrivo, la posta in uscita o altre cartelle contenenti messaggi possono essere un elemento separato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="29284-109">For example, within an email application, the Inbox, the Outbox, or some other folder containing messages can be a separate item for the application.</span></span>

<span data-ttu-id="29284-110">SyncMgr include inoltre un'interfaccia di programmazione che consente alle applicazioni di registrarsi per l'utilizzo delle funzionalità di sincronizzazione, può elaborare errori e ricevere informazioni sullo stato di avanzamento e notifiche durante il processo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="29284-110">SyncMgr also includes a programming interface so that applications can register to use synchronization features, can process errors, and can receive progress information and notifications during the synchronization process.</span></span>

 

 



