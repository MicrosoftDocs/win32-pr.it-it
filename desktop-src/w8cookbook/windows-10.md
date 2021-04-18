---
title: Windows 10
description: Questa guida di riferimento fornisce informazioni per gli sviluppatori sulle modifiche apportate alla piattaforma per i sistemi operativi Windows 10.
ms.assetid: bf8d7d10-bab6-4711-b65f-5393d906e47b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03fce627969573deb395fda356564a85a3573682
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399566"
---
# <a name="windows-10"></a><span data-ttu-id="4c9a1-103">Windows 10</span><span class="sxs-lookup"><span data-stu-id="4c9a1-103">Windows 10</span></span>

<span data-ttu-id="4c9a1-104">Questa guida di riferimento fornisce informazioni per gli sviluppatori sulle modifiche apportate alla piattaforma per i sistemi operativi Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-104">This Cookbook provides info for developers about platform changes to the Windows 10 operating systems (OS).</span></span> <span data-ttu-id="4c9a1-105">Vengono inoltre fornite linee guida per verificare la compatibilità delle app esistenti e pianificate con la versione più recente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-105">We also provide guidelines for you to verify the compatibility of your existing and planned apps with the latest version of the OS.</span></span> <span data-ttu-id="4c9a1-106">Si presuppone che l'utente abbia familiarità con le versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-106">We assume that you are familiar with previous versions of Windows.</span></span>

<span data-ttu-id="4c9a1-107">Il contenuto si applica a: Windows 10</span><span class="sxs-lookup"><span data-stu-id="4c9a1-107">The content applies to: Windows 10</span></span>

<span data-ttu-id="4c9a1-108">Il Cookbook è destinato agli sviluppatori di terze parti di app e dispositivi progettati per l'uso nell'ambiente Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-108">The Cookbook is for third party developers of apps and devices that are designed to be used in the Microsoft Windows environment.</span></span>

## <a name="introduction"></a><span data-ttu-id="4c9a1-109">Introduzione</span><span class="sxs-lookup"><span data-stu-id="4c9a1-109">Introduction</span></span>

<span data-ttu-id="4c9a1-110">Windows 10 introduce le più recenti piattaforme di sviluppo software e tecnologia del sistema operativo per l'uso da parte di sviluppatori e aziende di app e driver a livello mondiale.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-110">Windows 10 introduces the latest OS technology and software development platforms for use by app and driver developers and enterprises worldwide.</span></span> <span data-ttu-id="4c9a1-111">Per migliorare ulteriormente la sicurezza, l'affidabilità, le prestazioni e l'esperienza utente di Windows, Microsoft ha introdotto numerose nuove funzionalità, ha migliorato le funzionalità esistenti e ne ha rimosse altre.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-111">To further enhance the security, reliability, performance, and user experience of Windows, Microsoft has introduced many new features, improved existing features, and removed others.</span></span>

<span data-ttu-id="4c9a1-112">Anche se l'obiettivo di Windows 10 è mantenere la compatibilità con le app scritte per le versioni rilasciate in precedenza del sistema operativo Windows, alcune interruzioni di compatibilità sono inevitabili a causa di innovazioni, protezione rafforzata e maggiore affidabilità.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-112">While the goal of Windows 10 is to maintain compatibility with apps written for previously released versions of the Windows OS, some compatibility breaks are inevitable due to innovations, tightened security, and increased reliability.</span></span> <span data-ttu-id="4c9a1-113">In generale, la compatibilità della versione più recente del sistema operativo Windows con le app e i dispositivi esistenti è elevata.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-113">Overall, the compatibility of the latest version of the Windows OS with existing apps and devices is high.</span></span>

<span data-ttu-id="4c9a1-114">Questo documento illustra come verificare che le app e i dispositivi siano compatibili con la versione più recente del sistema operativo e fornisce una panoramica dei problemi noti di incompatibilità delle app.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-114">This document shows you how to verify that your apps and devices are compatible with the latest version of the OS and provides an overview of known app incompatibility issues.</span></span>

<span data-ttu-id="4c9a1-115">Si consiglia di consultare questi argomenti per informazioni su come ottimizzare le app e sfruttare i vantaggi offerti da questa versione più recente di Windows.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-115">We invite you to check out these topics to learn how to optimize your apps and take advantage of what this newest release of Windows has to offer.</span></span>

## <a name="contents"></a><span data-ttu-id="4c9a1-116">Contenuto</span><span class="sxs-lookup"><span data-stu-id="4c9a1-116">Contents</span></span>

-   [<span data-ttu-id="4c9a1-117">Modifiche principali apportate da Windows 7 per garantire la compatibilità</span><span class="sxs-lookup"><span data-stu-id="4c9a1-117">Key changes since Windows 7 to ensure compatibility</span></span>](key-changes-since-windows-7-to-ensure-compatibility.md)
-   [<span data-ttu-id="4c9a1-118">Come è possibile garantire la compatibilità dell'ecosistema combinato</span><span class="sxs-lookup"><span data-stu-id="4c9a1-118">How we can ensure compatibility of the combined ecosystem</span></span>](how-we-can-ensure-compatibility-of-the-combined-ecosystem.md)
    -   [<span data-ttu-id="4c9a1-119">Controllo della versione di Windows</span><span class="sxs-lookup"><span data-stu-id="4c9a1-119">Windows version check</span></span>](windows-version-check.md)
    -   [<span data-ttu-id="4c9a1-120">API non documentate</span><span class="sxs-lookup"><span data-stu-id="4c9a1-120">Undocumented APIs</span></span>](undocumented-apis.md)
    -   [<span data-ttu-id="4c9a1-121">Sviluppare app UWP e desktop Bridge</span><span class="sxs-lookup"><span data-stu-id="4c9a1-121">Develop UWP and Desktop Bridge apps</span></span>](/windows/desktop/w8cookbook/develop-universal-windows-platform-apps)
    -   [<span data-ttu-id="4c9a1-122">Le funzionalità moderne dell'app desktop sono interessate se non vengono eseguite in modalità finestra</span><span class="sxs-lookup"><span data-stu-id="4c9a1-122">Modern Desktop App functionality is impacted if not run in Windowed Mode</span></span>](modern-desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode.md)
    -   [<span data-ttu-id="4c9a1-123">Disponibilità dei driver grafici applicabili in Windows Update</span><span class="sxs-lookup"><span data-stu-id="4c9a1-123">Availability of applicable graphics drivers on Windows Update</span></span>](availability-of-applicable-graphics-drivers-on-windows-update.md)
    -   [<span data-ttu-id="4c9a1-124">Migrazione di driver grafici a Windows 10</span><span class="sxs-lookup"><span data-stu-id="4c9a1-124">Graphics driver migration to Windows 10</span></span>](graphics-driver-migration-to-windows-10.md)
    -   [<span data-ttu-id="4c9a1-125">Driver Bluetooth</span><span class="sxs-lookup"><span data-stu-id="4c9a1-125">Bluetooth drivers</span></span>](bluetooth-drivers.md)

## <a name="download-the-cookbook"></a><span data-ttu-id="4c9a1-126">Scarica il Cookbook</span><span class="sxs-lookup"><span data-stu-id="4c9a1-126">Download the cookbook</span></span>

<span data-ttu-id="4c9a1-127">Per un riferimento rapido a tutte queste informazioni e per informazioni su Windows As a Service, su come supportare le app in Windows e sulle strategie ottimizzate per il test dell'app, [scaricare il Cookbook per la compatibilità con Windows 10](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx).</span><span class="sxs-lookup"><span data-stu-id="4c9a1-127">For a quick reference to all this information, as well as information on Windows as a service, supporting apps in Windows, and optimized strategies for testing your app, [download the Windows 10 Compatibility Cookbook](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx).</span></span>

## <a name="see-also"></a><span data-ttu-id="4c9a1-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4c9a1-128">See Also</span></span>

-   <span data-ttu-id="4c9a1-129">[Windows As a Service](/windows/deployment/update/), per informazioni sui tipi di versione di Windows 10 e sul supporto delle app.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-129">[Windows as a service](/windows/deployment/update/), for information about Windows 10 release types and app support.</span></span>
-   <span data-ttu-id="4c9a1-130">[Windows Insider](https://insider.windows.com/), per accedere alle build di anteprima, testare e fornire commenti e suggerimenti.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-130">[Windows Insider](https://insider.windows.com/), to access preview builds, test, and provide feedback.</span></span>
-   <span data-ttu-id="4c9a1-131">[Pronto per Windows 10](https://www.readyfor10.com/), per inviare le informazioni aziendali a una risorsa per i responsabili IT.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-131">[Ready for Windows 10](https://www.readyfor10.com/), to submit your company's information to a resource for IT managers.</span></span>

 

 