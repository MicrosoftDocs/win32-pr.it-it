---
title: Informazioni sulle interfacce del servizio Active Directory
description: Le interfacce ADSI (Active Directory Service Interfaces) astraggono le funzionalità dei servizi directory da provider di rete diversi in un ambiente di elaborazione distribuita per presentare un unico set di interfacce del servizio directory per la gestione delle risorse di rete.
ms.assetid: 6d601af5-7470-42c2-b99e-21174ea008b1
ms.tgt_platform: multiple
keywords:
- Informazioni su Active Directory interfacce di servizio ADSI
- ADSI ADSI, informazioni
- Interfacce di servizio Active Directory ADSI, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc083b33a633335da12915257fcddff1174a6858
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116701"
---
# <a name="about-active-directory-service-interfaces"></a><span data-ttu-id="fd620-106">Informazioni sulle interfacce del servizio Active Directory</span><span class="sxs-lookup"><span data-stu-id="fd620-106">About Active Directory Service Interfaces</span></span>

<span data-ttu-id="fd620-107">Le interfacce ADSI (Active Directory Service Interfaces) astraggono le funzionalità dei servizi directory da provider di rete diversi in un ambiente di elaborazione distribuita per presentare un unico set di interfacce del servizio directory per la gestione delle risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="fd620-107">Active Directory Service Interfaces (ADSI) abstracts the capabilities of directory services from different network providers in a distributed computing environment to present a single set of directory service interfaces for managing network resources.</span></span> <span data-ttu-id="fd620-108">Gli amministratori e gli sviluppatori possono utilizzare i servizi ADSI per enumerare e gestire le risorse in un servizio directory, indipendentemente dall'ambiente di rete che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="fd620-108">Administrators and developers can use ADSI services to enumerate and manage the resources in a directory service, no matter which network environment contains the resource.</span></span>

<span data-ttu-id="fd620-109">ADSI semplifica l'esecuzione di attività amministrative comuni, ad esempio l'aggiunta di nuovi utenti, la gestione delle stampanti e l'individuazione delle risorse nell'ambiente di calcolo distribuito.</span><span class="sxs-lookup"><span data-stu-id="fd620-109">ADSI makes it easier to perform common administrative tasks, such as adding new users, managing printers, and locating resources throughout the distributed computing environment.</span></span>

<span data-ttu-id="fd620-110">ADSI consente agli sviluppatori di "abilitare le directory" in modo semplice.</span><span class="sxs-lookup"><span data-stu-id="fd620-110">ADSI makes it easy for developers to "directory enable" their applications.</span></span> <span data-ttu-id="fd620-111">Gli amministratori e gli sviluppatori gestiscono un singolo set di interfacce del servizio directory, indipendentemente dai servizi directory installati.</span><span class="sxs-lookup"><span data-stu-id="fd620-111">Administrators and developers handle a single set of directory service interfaces, regardless of which directory services are installed.</span></span>

<span data-ttu-id="fd620-112">Gli argomenti seguenti sono descritti in questa introduzione:</span><span class="sxs-lookup"><span data-stu-id="fd620-112">The following topics are discussed in this introduction:</span></span>

-   [<span data-ttu-id="fd620-113">Più servizi directory</span><span class="sxs-lookup"><span data-stu-id="fd620-113">Multiple Directory Services</span></span>](multiple-directory-services.md)
-   [<span data-ttu-id="fd620-114">Chi utilizzerà Active Directory interfacce del servizio?</span><span class="sxs-lookup"><span data-stu-id="fd620-114">Who Will Use Active Directory Service Interfaces?</span></span>](who-will-use-active-directory-service-interfaces.md)
-   [<span data-ttu-id="fd620-115">Servizi directory attualmente</span><span class="sxs-lookup"><span data-stu-id="fd620-115">Directory Services Today</span></span>](directory-services-today.md)
-   [<span data-ttu-id="fd620-116">Vantaggi dell'utilizzo delle interfacce di servizio Active Directory</span><span class="sxs-lookup"><span data-stu-id="fd620-116">Benefits of Using Active Directory Service Interfaces</span></span>](benefits-of-using-active-directory-service-interfaces.md)
-   [<span data-ttu-id="fd620-117">Architettura delle interfacce del servizio Active Directory</span><span class="sxs-lookup"><span data-stu-id="fd620-117">Active Directory Service Interfaces Architecture</span></span>](active-directory-service-interfaces-architecture.md)
-   [<span data-ttu-id="fd620-118">Supporto del linguaggio di programmazione</span><span class="sxs-lookup"><span data-stu-id="fd620-118">Programming Language Support</span></span>](programming-language-support.md)
-   [<span data-ttu-id="fd620-119">Proprietà e attributi ADSI</span><span class="sxs-lookup"><span data-stu-id="fd620-119">ADSI Properties and Attributes</span></span>](adsi-properties-and-attributes.md)

## <a name="what-you-should-know-before-reading-this-guide"></a><span data-ttu-id="fd620-120">Informazioni preliminari per la lettura di questa guida</span><span class="sxs-lookup"><span data-stu-id="fd620-120">What You Should Know Before Reading This Guide</span></span>

<span data-ttu-id="fd620-121">In questa guida si presuppone che l'utente abbia familiarità con il Component Object Model (COM) e l'automazione e che sia possibile programmare in Visual Basic o C/C++.</span><span class="sxs-lookup"><span data-stu-id="fd620-121">This guide assumes that you are familiar with the Component Object Model (COM) and Automation, and that you know how to program in either Visual Basic or C/C++.</span></span>

<span data-ttu-id="fd620-122">Alcuni dei termini usati in questa guida sono univoci per ADSI o per l'ambiente dei servizi directory.</span><span class="sxs-lookup"><span data-stu-id="fd620-122">Some of the terms used in this guide are unique to either ADSI or the directory services environment.</span></span> <span data-ttu-id="fd620-123">Altri termini saranno noti ma potrebbero avere significati leggermente diversi in questi ambienti.</span><span class="sxs-lookup"><span data-stu-id="fd620-123">Other terms will be familiar but may have slightly different meanings in these environments.</span></span>

## <a name="further-reading-about-adsi-and-related-topics"></a><span data-ttu-id="fd620-124">Ulteriori informazioni su ADSI e argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fd620-124">Further Reading about ADSI and Related Topics</span></span>

<span data-ttu-id="fd620-125">Per ulteriori informazioni sulle interfacce del servizio Active Directory e sulle tecnologie su cui si basano, è possibile che siano disponibili le origini seguenti.</span><span class="sxs-lookup"><span data-stu-id="fd620-125">For more information about Active Directory Service Interfaces and the technologies on which they are based, you may find the following sources helpful.</span></span>

<span data-ttu-id="fd620-126">Brockschmidt, Kraig.</span><span class="sxs-lookup"><span data-stu-id="fd620-126">Brockschmidt, Kraig.</span></span> <span data-ttu-id="fd620-127">*All'interno di OLE*, 2a edizione.</span><span class="sxs-lookup"><span data-stu-id="fd620-127">*Inside OLE*, 2nd edition.</span></span> <span data-ttu-id="fd620-128">Redmond, WA: Microsoft Press, 1995.</span><span class="sxs-lookup"><span data-stu-id="fd620-128">Redmond, WA: Microsoft Press, 1995.</span></span>

<span data-ttu-id="fd620-129">Cuccu, David.</span><span class="sxs-lookup"><span data-stu-id="fd620-129">Chappell, David.</span></span> <span data-ttu-id="fd620-130">*Informazioni su ActiveX e OLE*.</span><span class="sxs-lookup"><span data-stu-id="fd620-130">*Understanding ActiveX and OLE*.</span></span> <span data-ttu-id="fd620-131">Redmond, WA: Microsoft Press, 1996.</span><span class="sxs-lookup"><span data-stu-id="fd620-131">Redmond, WA: Microsoft Press, 1996.</span></span>

<span data-ttu-id="fd620-132">Hahn, Steven.</span><span class="sxs-lookup"><span data-stu-id="fd620-132">Hahn, Steven.</span></span> <span data-ttu-id="fd620-133">Guida *di riferimento per programmatori ADSI ASP*.</span><span class="sxs-lookup"><span data-stu-id="fd620-133">*ADSI ASP Programmer's Reference*.</span></span> <span data-ttu-id="fd620-134">Wrox premere Ltd., 1998.</span><span class="sxs-lookup"><span data-stu-id="fd620-134">Wrox Press Ltd., 1998.</span></span>

<span data-ttu-id="fd620-135">Harrison, Richard.</span><span class="sxs-lookup"><span data-stu-id="fd620-135">Harrison, Richard.</span></span> <span data-ttu-id="fd620-136">*Sicurezza Web ASP/MTS/ADSI*.</span><span class="sxs-lookup"><span data-stu-id="fd620-136">*ASP/MTS/ADSI Web Security*.</span></span> <span data-ttu-id="fd620-137">Prentice Hall, 1999.</span><span class="sxs-lookup"><span data-stu-id="fd620-137">Prentice Hall, 1999.</span></span>

<span data-ttu-id="fd620-138">Microsoft OLE DB Programmer ' s Reference versione 1,0, 1996.</span><span class="sxs-lookup"><span data-stu-id="fd620-138">Microsoft's OLE DB Programmer's Reference Version 1.0, 1996.</span></span>

<span data-ttu-id="fd620-139">*Riferimento per programmatori OLE 2, Volume Two*.</span><span class="sxs-lookup"><span data-stu-id="fd620-139">*OLE 2 Programmer's Reference, Volume Two*.</span></span> <span data-ttu-id="fd620-140">Redmond, WA: Microsoft Press, 1994.</span><span class="sxs-lookup"><span data-stu-id="fd620-140">Redmond, WA: Microsoft Press, 1994.</span></span>

<span data-ttu-id="fd620-141">Rogerson, Dale.</span><span class="sxs-lookup"><span data-stu-id="fd620-141">Rogerson, Dale.</span></span> <span data-ttu-id="fd620-142">*All'interno di com*.</span><span class="sxs-lookup"><span data-stu-id="fd620-142">*Inside COM*.</span></span> <span data-ttu-id="fd620-143">Redmond, WA: Microsoft Press, 1997.</span><span class="sxs-lookup"><span data-stu-id="fd620-143">Redmond, WA: Microsoft Press, 1997.</span></span>

<span data-ttu-id="fd620-144">*La specifica di progettazione del servizio Active Directory versione 2,0*.</span><span class="sxs-lookup"><span data-stu-id="fd620-144">*The Active Directory Service Design Specification Version 2.0*.</span></span>

<span data-ttu-id="fd620-145">*Specifica Component Object Model*.</span><span class="sxs-lookup"><span data-stu-id="fd620-145">*The Component Object Model Specification*.</span></span>

<span data-ttu-id="fd620-146">Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="fd620-146">(These resources may not be available in some languages and countries/regions.)</span></span>

 

 




