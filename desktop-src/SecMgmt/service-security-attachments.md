---
description: Microsoft Security Configuration Tool set è un set di strumenti di Microsoft Management Console (MMC) che semplificano la configurazione e l'analisi della sicurezza del sistema.
ms.assetid: c6558789-84eb-4998-a2c1-725d8a64d255
title: Allegati di sicurezza del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47cdd0ca3799615125900a3ae6b0b78c26f4abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343091"
---
# <a name="service-security-attachments"></a><span data-ttu-id="271c9-103">Allegati di sicurezza del servizio</span><span class="sxs-lookup"><span data-stu-id="271c9-103">Service Security Attachments</span></span>

<span data-ttu-id="271c9-104">Microsoft Security Configuration Tool set è un set di strumenti di Microsoft Management Console (MMC) che semplificano la configurazione e l'analisi della sicurezza del sistema.</span><span class="sxs-lookup"><span data-stu-id="271c9-104">The Microsoft Security Configuration tool set is a set of Microsoft Management Console (MMC) tools that simplify configuration and analysis of system security.</span></span> <span data-ttu-id="271c9-105">Alcuni servizi, tuttavia, hanno esigenze di configurazione specializzate che vanno oltre le impostazioni di sicurezza fornite dal set di strumenti standard.</span><span class="sxs-lookup"><span data-stu-id="271c9-105">Some services, however, have specialized configuration needs that go beyond the security settings provided by the standard tool set.</span></span> <span data-ttu-id="271c9-106">Per gestire tali esigenze, è possibile estendere la funzionalità del set di strumenti scrivendo un allegato che gestisce le attività di sicurezza specifiche del servizio.</span><span class="sxs-lookup"><span data-stu-id="271c9-106">To handle those needs, you can extend the functionality of the tool set by writing an attachment that handles the service-specific security tasks.</span></span>

<span data-ttu-id="271c9-107">Lo spooler, ad esempio, è un servizio di Windows NT che definisce oggetti privati, che devono essere protetti, ad esempio stampanti.</span><span class="sxs-lookup"><span data-stu-id="271c9-107">For example, Spooler is a Windows NT service that defines private objects, which need to be secured, for example, printers.</span></span> <span data-ttu-id="271c9-108">Questa funzionalità non viene gestita dal set di strumenti standard e pertanto richiede un allegato per gestire la configurazione e l'analisi degli oggetti stampante.</span><span class="sxs-lookup"><span data-stu-id="271c9-108">This functionality is not handled by the standard tool set and thus requires an attachment to handle configuration and analysis of printer objects.</span></span> <span data-ttu-id="271c9-109">La configurazione dei parametri di sicurezza generale, ad esempio i criteri di chiamata del servizio, è ancora gestita dal set di strumenti di configurazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="271c9-109">Configuration of general security parameters, such as the service invocation policy, is still handled by the Security Configuration tool set.</span></span>

<span data-ttu-id="271c9-110">Gli allegati dei servizi di sicurezza estendono le funzionalità dello strumento di configurazione della sicurezza impostato per supportare configurazioni specifiche del servizio.</span><span class="sxs-lookup"><span data-stu-id="271c9-110">Security service attachments extend the functionality of the Security Configuration tool set to support service-specific configurations.</span></span>

<span data-ttu-id="271c9-111">Un allegato è costituito da due componenti:</span><span class="sxs-lookup"><span data-stu-id="271c9-111">An attachment has two components:</span></span>

-   <span data-ttu-id="271c9-112">Estensione di snap-in di MMC che implementa l'interfaccia utente dell'allegato.</span><span class="sxs-lookup"><span data-stu-id="271c9-112">An MMC snap-in extension that implements the attachment user interface.</span></span>
-   <span data-ttu-id="271c9-113">Motore di allegati che elabora le attività di analisi e configurazione della sicurezza specifiche del servizio.</span><span class="sxs-lookup"><span data-stu-id="271c9-113">An attachment engine that processes service-specific security configuration and analysis tasks.</span></span>

<span data-ttu-id="271c9-114">L'estensione dello snap-in allegato è ospitata dagli snap-in Configurazione sicurezza. Si tratta di snap-in di MMC che forniscono all'utente le interfacce per configurare e analizzare le impostazioni di sicurezza generali per un servizio.</span><span class="sxs-lookup"><span data-stu-id="271c9-114">The attachment snap-in extension is hosted by the Security Configuration snap-ins. These are MMC snap-ins that provide the user with interfaces to configure and analyze the general security settings for a service.</span></span> <span data-ttu-id="271c9-115">Le impostazioni specifiche del servizio vengono configurate utilizzando l'estensione dello snap-in allegato.</span><span class="sxs-lookup"><span data-stu-id="271c9-115">Service-specific settings are configured using the attachment snap-in extension.</span></span>

<span data-ttu-id="271c9-116">Quando l'utente modifica un'impostazione di configurazione, gli snap-in configurazione di sicurezza archiviano le nuove informazioni e quindi passano la richiesta al motore di configurazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="271c9-116">When the user changes a configuration setting, the Security Configuration snap-ins store the new information and then pass the request to the Security Configuration Engine.</span></span> <span data-ttu-id="271c9-117">Il motore elabora la richiesta e imposta il servizio sulla nuova configurazione.</span><span class="sxs-lookup"><span data-stu-id="271c9-117">The Engine processes the request and sets the service to the new configuration.</span></span> <span data-ttu-id="271c9-118">Se la richiesta ha effetto su un'impostazione di sicurezza standard, viene gestita dal motore.</span><span class="sxs-lookup"><span data-stu-id="271c9-118">If the request affects a standard security setting, it is handled by the Engine.</span></span> <span data-ttu-id="271c9-119">Se la richiesta è specifica del servizio, il motore chiama il motore degli allegati appropriato per gestire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="271c9-119">If the request is service-specific, the Engine calls the appropriate attachment engine to handle the request.</span></span>

<span data-ttu-id="271c9-120">Nella figura seguente viene illustrato il funzionamento del motore di allegati e dell'estensione dello snap-in nel Framework del set di strumenti di configurazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="271c9-120">The following illustration shows how the attachment engine and snap-in extension work within the framework of the Security Configuration tool set.</span></span>

![motore allegati e snap-in](images/model1a.png)

<span data-ttu-id="271c9-122">Per ulteriori informazioni sull'utilizzo del set di strumenti di configurazione della sicurezza Microsoft, cercare configurazione di sicurezza utilizzando il motore di ricerca preferito.</span><span class="sxs-lookup"><span data-stu-id="271c9-122">For more information about using the Microsoft Security Configuration tool set, search for Security Configuration using your preferred search engine.</span></span>

 

 



