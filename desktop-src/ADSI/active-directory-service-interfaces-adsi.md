---
title: Interfacce di servizio Active Directory
description: Introduzione alle interfacce di Active Directory Services, con collegamenti a diverse guide.
ms.assetid: b24f9789-b9f5-49c4-9812-298bae8b28a9
ms.tgt_platform: multiple
keywords:
- ADSI ADSI
- Interfacce del servizio Active Directory (vedere ADSI)
- ADSI ADSI, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cc702fec86f1202f1fbd00ba575fd848e4ab74
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047359"
---
# <a name="active-directory-service-interfaces"></a><span data-ttu-id="a27c4-106">Interfacce di servizio Active Directory</span><span class="sxs-lookup"><span data-stu-id="a27c4-106">Active Directory Service Interfaces</span></span>

## <a name="purpose"></a><span data-ttu-id="a27c4-107">Scopo</span><span class="sxs-lookup"><span data-stu-id="a27c4-107">Purpose</span></span>

<span data-ttu-id="a27c4-108">Active Directory Service Interfaces (ADSI) è un set di interfacce COM utilizzate per accedere alle funzionalità dei servizi directory da provider di rete diversi.</span><span class="sxs-lookup"><span data-stu-id="a27c4-108">Active Directory Service Interfaces (ADSI) is a set of COM interfaces used to access the features of directory services from different network providers.</span></span> <span data-ttu-id="a27c4-109">ADSI viene utilizzato in un ambiente di elaborazione distribuita per presentare un unico set di interfacce del servizio directory per la gestione delle risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="a27c4-109">ADSI is used in a distributed computing environment to present a single set of directory service interfaces for managing network resources.</span></span> <span data-ttu-id="a27c4-110">Gli amministratori e gli sviluppatori possono utilizzare i servizi ADSI per enumerare e gestire le risorse in un servizio directory, indipendentemente dall'ambiente di rete che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a27c4-110">Administrators and developers can use ADSI services to enumerate and manage the resources in a directory service, no matter which network environment contains the resource.</span></span>

<span data-ttu-id="a27c4-111">ADSI consente attività amministrative comuni, ad esempio l'aggiunta di nuovi utenti, la gestione delle stampanti e l'individuazione delle risorse in un ambiente di elaborazione distribuito.</span><span class="sxs-lookup"><span data-stu-id="a27c4-111">ADSI enables common administrative tasks, such as adding new users, managing printers, and locating resources in a distributed computing environment.</span></span>

> [!Note]  
> <span data-ttu-id="a27c4-112">La documentazione seguente è destinata ai programmatori di computer.</span><span class="sxs-lookup"><span data-stu-id="a27c4-112">The following documentation is for computer programmers.</span></span> <span data-ttu-id="a27c4-113">Se si è un utente finale che tenta di eseguire il debug di un errore di stampa o di una rete domestica, vedere i [Forum della community Microsoft](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="a27c4-113">If you are an end-user trying to debug a printing error or home network issue, see the [Microsoft community forums](https://answers.microsoft.com).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="a27c4-114">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="a27c4-114">Where applicable</span></span>

<span data-ttu-id="a27c4-115">Gli amministratori di rete possono utilizzare ADSI per automatizzare le attività comuni, ad esempio l'aggiunta di utenti e gruppi, la gestione delle stampanti e l'impostazione delle autorizzazioni per le risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="a27c4-115">Network Administrators can use ADSI to automate common tasks, such as adding users and groups, managing printers, and setting permissions on network resources.</span></span>

<span data-ttu-id="a27c4-116">I fornitori di software indipendenti e gli sviluppatori di utenti finali possono utilizzare ADSI per "abilitare la directory" dei propri prodotti e applicazioni.</span><span class="sxs-lookup"><span data-stu-id="a27c4-116">Independent Software Vendors and end-user developers can use ADSI to "directory enable" their products and applications.</span></span> <span data-ttu-id="a27c4-117">I servizi possono essere pubblicati in una directory, i client possono utilizzare la directory per trovare i servizi ed entrambi possono utilizzare la directory per individuare e modificare altri oggetti di interesse.</span><span class="sxs-lookup"><span data-stu-id="a27c4-117">Services can publish themselves in a directory, clients can use the directory to find the services, and both can use the directory to find and manipulate other objects of interest.</span></span> <span data-ttu-id="a27c4-118">Poiché le interfacce del servizio Active Directory sono indipendenti dai servizi directory sottostanti, i prodotti e le applicazioni abilitati alla directory possono funzionare correttamente in più ambienti di rete e di directory.</span><span class="sxs-lookup"><span data-stu-id="a27c4-118">Because Active Directory Service Interfaces are independent of the underlying directory service(s), directory-enabled products and applications can operate successfully in multiple network and directory environments.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a27c4-119">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="a27c4-119">Developer audience</span></span>

<span data-ttu-id="a27c4-120">È possibile scrivere applicazioni client ADSI in molte lingue.</span><span class="sxs-lookup"><span data-stu-id="a27c4-120">You can write ADSI client applications in many languages.</span></span> <span data-ttu-id="a27c4-121">Per la maggior parte delle attività amministrative, ADSI definisce le interfacce e gli oggetti accessibili da linguaggi conformi all'automazione come Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript) e Java ai linguaggi più performanti e in efficienza, ad esempio C e C++.</span><span class="sxs-lookup"><span data-stu-id="a27c4-121">For most administrative tasks, ADSI defines interfaces and objects accessible from Automation-compliant languages like Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript), and Java to the more performance and efficiency-conscious languages such as C and C++.</span></span> <span data-ttu-id="a27c4-122">Una valida base nella programmazione COM è utile per il programmatore ADSI.</span><span class="sxs-lookup"><span data-stu-id="a27c4-122">A good foundation in COM programming is useful to the ADSI programmer.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a27c4-123">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="a27c4-123">Run-time requirements</span></span>

<span data-ttu-id="a27c4-124">Active Directory viene eseguito nei controller di dominio di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="a27c4-124">Active Directory runs on Windows Server domain controllers.</span></span> <span data-ttu-id="a27c4-125">Tuttavia, le applicazioni client che utilizzano ADSI possono essere scritte ed eseguite in Windows.</span><span class="sxs-lookup"><span data-stu-id="a27c4-125">However, client applications using ADSI may be written and run on Windows.</span></span> <span data-ttu-id="a27c4-126">Inoltre, gli sviluppatori vorranno la piattaforma Software Development Kit (SDK), disponibile anche nel sito Web MSDN.</span><span class="sxs-lookup"><span data-stu-id="a27c4-126">In addition, developers will want the Platform Software Development Kit (SDK), also available on the MSDN website.</span></span> <span data-ttu-id="a27c4-127">Per esaminare il contenuto di Active Directory, utilizzare lo snap-in MMC utenti e computer Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a27c4-127">To investigate the contents of Active Directory, use the Active Directory Users and Computers MMC snap-in.</span></span> <span data-ttu-id="a27c4-128">Questo snap-in sostituisce lo strumento ADSVW disponibile per le versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="a27c4-128">This snap-in replaces the Adsvw tool that was available for previous versions of Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a27c4-129">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a27c4-129">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a27c4-130">Informazioni su ADSI</span><span class="sxs-lookup"><span data-stu-id="a27c4-130">About ADSI</span></span>](about-adsi.md)
</dt> <dd>

<span data-ttu-id="a27c4-131">Informazioni generali su ADSI.</span><span class="sxs-lookup"><span data-stu-id="a27c4-131">General information about ADSI.</span></span>

</dd> <dt>

[<span data-ttu-id="a27c4-132">Uso di ADSI</span><span class="sxs-lookup"><span data-stu-id="a27c4-132">Using ADSI</span></span>](using-adsi.md)
</dt> <dd>

<span data-ttu-id="a27c4-133">Guida per programmatori per l'utilizzo di ADSI.</span><span class="sxs-lookup"><span data-stu-id="a27c4-133">Programmer's Guide to using ADSI.</span></span>

</dd> <dt>

[<span data-ttu-id="a27c4-134">Esercitazioni introduttive di ADSI</span><span class="sxs-lookup"><span data-stu-id="a27c4-134">ADSI Quick-start Tutorials</span></span>](adsi-quick-start-tutorials.md)
</dt> <dd>

<span data-ttu-id="a27c4-135">Uso di ADSI con automazione per la gestione delle directory.</span><span class="sxs-lookup"><span data-stu-id="a27c4-135">Using ADSI with Automation to manage directories.</span></span>

</dd> <dt>

[<span data-ttu-id="a27c4-136">Riferimenti ADSI</span><span class="sxs-lookup"><span data-stu-id="a27c4-136">ADSI Reference</span></span>](adsi-reference.md)
</dt> <dd>

<span data-ttu-id="a27c4-137">Documentazione di interfacce e metodi ADSI.</span><span class="sxs-lookup"><span data-stu-id="a27c4-137">Documentation of ADSI interfaces and methods.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="a27c4-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a27c4-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a27c4-139">Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="a27c4-139">The Component Object Model</span></span>](../com/the-component-object-model.md)
</dt> <dt>

[<span data-ttu-id="a27c4-140">Client e server COM</span><span class="sxs-lookup"><span data-stu-id="a27c4-140">COM Clients and Servers</span></span>](../com/com-clients-and-servers.md)
</dt> <dt>

[<span data-ttu-id="a27c4-141">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="a27c4-141">Active Directory Domain Services</span></span>](../ad/active-directory-domain-services.md)
</dt> </dl>

 

 