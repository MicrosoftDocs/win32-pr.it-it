---
description: Un motore di allegati è una DLL che gestisce le richieste di configurazione e analisi specifiche del servizio.
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: Motori allegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af0711caa5ceada7c16ae11b6470568a76d16ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883606"
---
# <a name="attachment-engines"></a><span data-ttu-id="1a31f-103">Motori allegati</span><span class="sxs-lookup"><span data-stu-id="1a31f-103">Attachment Engines</span></span>

<span data-ttu-id="1a31f-104">Un motore di allegati è una DLL che gestisce le richieste di configurazione e analisi specifiche del servizio.</span><span class="sxs-lookup"><span data-stu-id="1a31f-104">An attachment engine is a DLL that handles service-specific configuration and analysis requests.</span></span>

<span data-ttu-id="1a31f-105">L'utente esegue una configurazione e una richiesta di analisi specifiche del servizio usando l'estensione dello snap-in allegato.</span><span class="sxs-lookup"><span data-stu-id="1a31f-105">The user makes a service-specific configuration and analysis request using the attachment snap-in extension.</span></span> <span data-ttu-id="1a31f-106">Questa richiesta viene quindi passata tramite gli snap-in configurazione di sicurezza al motore di configurazione della sicurezza generale, che a sua volta passa l'elaborazione specifica del servizio al motore di allegati appropriato.</span><span class="sxs-lookup"><span data-stu-id="1a31f-106">This request is then passed through the Security Configuration snap-ins to the general Security Configuration Engine, which in turn passes the service-specific processing to the appropriate attachment engine.</span></span> <span data-ttu-id="1a31f-107">Il motore dell'allegato si connette quindi al servizio e ne modifica la configurazione.</span><span class="sxs-lookup"><span data-stu-id="1a31f-107">The attachment engine then connects to the service and changes its configuration.</span></span> <span data-ttu-id="1a31f-108">In altre parole, il motore di allegati fornisce l'elaborazione back-end che supporta l'estensione dello snap-in allegato.</span><span class="sxs-lookup"><span data-stu-id="1a31f-108">In other words, the attachment engine provides the back-end processing that supports the attachment snap-in extension.</span></span>

<span data-ttu-id="1a31f-109">Un motore di allegati deve implementare le tre funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1a31f-109">An attachment engine must implement the following three functions:</span></span>

-   <span data-ttu-id="1a31f-110">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), che calcola la differenza tra la configurazione del servizio e la configurazione archiviata nel database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1a31f-110">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), which computes the difference between the service's configuration and the configuration stored in the security database.</span></span> <span data-ttu-id="1a31f-111">Le differenze vengono scritte nel database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1a31f-111">The differences are written to the security database.</span></span>
-   <span data-ttu-id="1a31f-112">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), che configura il servizio come specificato nell'interfaccia utente dello snap-in.</span><span class="sxs-lookup"><span data-stu-id="1a31f-112">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), which configures the service as specified in the snap-in user interface.</span></span>
-   <span data-ttu-id="1a31f-113">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), che aggiorna la configurazione di base e l'analisi della configurazione per il servizio nel database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1a31f-113">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), which updates the base configuration and configuration analysis for the service in the security database.</span></span>

<span data-ttu-id="1a31f-114">Per semplificare l'implementazione delle funzioni precedenti, il set di strumenti di configurazione della sicurezza fornisce le funzioni e le strutture di supporto che l'applicazione può utilizzare per eseguire query e impostare le informazioni nel database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1a31f-114">To simplify implementation of the preceding functions, the Security Configuration tool set provides support functions and structures that your application can use to query and set information in the security database.</span></span> <span data-ttu-id="1a31f-115">Per altre informazioni, vedere [funzioni di callback degli allegati](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="1a31f-115">For more information, see [Attachment Callback Functions](management-functions.md).</span></span>

<span data-ttu-id="1a31f-116">Quando si crea una DLL del motore di allegati, è necessario installarla e quindi registrarla con il motore di configurazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1a31f-116">When you create an attachment engine DLL, you must install it and then register it with the Security Configuration Engine.</span></span> <span data-ttu-id="1a31f-117">Per registrare la DLL, aggiungere una chiave specifica al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1a31f-117">To register the DLL, you add a specific key to the registry.</span></span> <span data-ttu-id="1a31f-118">Quando viene avviato, il motore di configurazione della sicurezza controlla il registro di sistema e carica tutte le dll del motore allegati registrato.</span><span class="sxs-lookup"><span data-stu-id="1a31f-118">When the Security Configuration Engine starts, it checks the registry and loads all registered attachment engine DLLs.</span></span> <span data-ttu-id="1a31f-119">Passa quindi le richieste di configurazione e analisi specifiche del servizio al motore di allegati appropriato.</span><span class="sxs-lookup"><span data-stu-id="1a31f-119">It then passes service-specific configuration and analysis requests to the appropriate attachment engine.</span></span> <span data-ttu-id="1a31f-120">Le richieste di configurazione e analisi standard, che non sono specifiche del servizio, vengono gestite dal motore di configurazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1a31f-120">Standard configuration and analysis requests, those that are not service-specific, are handled by the Security Configuration Engine.</span></span>

 

 



