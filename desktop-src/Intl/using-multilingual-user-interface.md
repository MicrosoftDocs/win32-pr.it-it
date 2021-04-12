---
description: Uso dell'interfaccia utente multilingue
ms.assetid: caf167ad-f9a8-4093-9581-57bc507d1f6a
title: Uso dell'interfaccia utente multilingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287acc88d144c7775d2125cbb4a055784370d87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234192"
---
# <a name="using-multilingual-user-interface"></a><span data-ttu-id="b7995-103">Uso dell'interfaccia utente multilingue</span><span class="sxs-lookup"><span data-stu-id="b7995-103">Using Multilingual User Interface</span></span>

<span data-ttu-id="b7995-104">Questa sezione descrive come usare la funzionalità Multilingual User Interface (MUI) per progettare e implementare le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b7995-104">This section describes how to use Multilingual User Interface (MUI) functionality to design and implement your applications.</span></span> <span data-ttu-id="b7995-105">Di seguito sono riportati alcuni aspetti della tecnologia MUI che entrano in gioco alla maggior parte delle fasi del ciclo di vita dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7995-105">The following are aspects of MUI technology that will come into play at most stages of the application lifecycle.</span></span>

-   <span data-ttu-id="b7995-106">Sviluppo di applicazioni, tra cui la preparazione delle risorse, l'impostazione delle preferenze della lingua dell'applicazione, la ricerca e il caricamento delle risorse</span><span class="sxs-lookup"><span data-stu-id="b7995-106">Application development, including resource preparation, setting of application language preferences, finding and loading of resources</span></span>
-   <span data-ttu-id="b7995-107">Compilazione e localizzazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b7995-107">Building and localizing the application</span></span>
-   <span data-ttu-id="b7995-108">Distribuzione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b7995-108">Deploying the application</span></span>

<span data-ttu-id="b7995-109">Di seguito sono riportate alcune domande da considerare durante la progettazione e l'implementazione di un'applicazione MUI.</span><span class="sxs-lookup"><span data-stu-id="b7995-109">Here are some questions to consider when designing and implementing a MUI application.</span></span>

-   <span data-ttu-id="b7995-110">Quali sono le versioni di Windows supportate dall'applicazione?</span><span class="sxs-lookup"><span data-stu-id="b7995-110">What are the versions of Windows that the application will support?</span></span>
-   <span data-ttu-id="b7995-111">In quali lingue verrà localizzata l'applicazione?</span><span class="sxs-lookup"><span data-stu-id="b7995-111">In what languages will the application be localized?</span></span>
-   <span data-ttu-id="b7995-112">Se le impostazioni della lingua dell'applicazione seguono sempre le impostazioni della lingua per il sistema operativo o se l'utente dell'applicazione è in grado di impostare lingue specifiche?</span><span class="sxs-lookup"><span data-stu-id="b7995-112">Should the application language settings always follow language settings for the operating system, or should the application user be able to set specific languages?</span></span>
-   <span data-ttu-id="b7995-113">Quali tipi di risorse dell'interfaccia utente vengono utilizzate dall'applicazione e dove vengono archiviati?</span><span class="sxs-lookup"><span data-stu-id="b7995-113">What type of user interface resources does the application use and where are they stored?</span></span>

<span data-ttu-id="b7995-114">Questa sezione include gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="b7995-114">This section includes the following topics.</span></span> <span data-ttu-id="b7995-115">Le descrizioni presuppongono che un'applicazione MUI sia destinata a Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b7995-115">The descriptions assume a MUI application targeted at Windows Vista and later.</span></span> <span data-ttu-id="b7995-116">Le risorse per questa applicazione sono risorse Win32, con risorse specifiche del linguaggio e codice eseguibile che risiede in file PE Win32 distinti.</span><span class="sxs-lookup"><span data-stu-id="b7995-116">The resources for this application are Win32 resources, with language-specific resources and executable code residing in separate Win32 PE files.</span></span> <span data-ttu-id="b7995-117">Considerazioni speciali per il supporto dei sistemi operativi precedenti a Windows Vista o per i diversi tipi di risorse vengono aggiunti a seconda delle esigenze.</span><span class="sxs-lookup"><span data-stu-id="b7995-117">Special considerations for support of pre-Windows Vista operating systems or for different types of resources are added as appropriate.</span></span>

-   [<span data-ttu-id="b7995-118">Preparazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="b7995-118">Preparing Resources</span></span>](preparing-resources.md)
-   [<span data-ttu-id="b7995-119">Impostazione delle preferenze di lingua dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b7995-119">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
-   [<span data-ttu-id="b7995-120">Individuazione delle risorse PE Win32</span><span class="sxs-lookup"><span data-stu-id="b7995-120">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
-   [<span data-ttu-id="b7995-121">Individuazione di risorse PE non Win32</span><span class="sxs-lookup"><span data-stu-id="b7995-121">Locating Non-Win32 PE Resources</span></span>](locating-non-win32-pe-resources.md)
-   [<span data-ttu-id="b7995-122">Localizzazione delle risorse e compilazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b7995-122">Localizing Resources and Building the Application</span></span>](localizing-resources-and-building-the-application.md)
-   [<span data-ttu-id="b7995-123">Esempio di applicazione delle impostazioni di sistema MUI:</span><span class="sxs-lookup"><span data-stu-id="b7995-123">MUI: System Settings Application Sample</span></span>](mui-system-settings-application-sample.md)
-   [<span data-ttu-id="b7995-124">Esempio di impostazioni di MUI: Application-Specific (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="b7995-124">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
-   [<span data-ttu-id="b7995-125">Esempio di impostazioni di MUI: Application-Specific (precedente a Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="b7995-125">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)

 

 



