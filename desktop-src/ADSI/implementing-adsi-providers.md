---
title: Implementazione di provider di interfacce del servizio Active Directory
description: Le interfacce ADSI (Active Directory Service Interfaces) sono interfacce COM che eseguono il wrapping di oggetti del servizio directory per esporli ai client dei servizi directory. Fornendo un'implementazione di ADSI, espandere la base client al set di applicazioni client ADSI.
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- Implementazione di Active Directory provider di interfacce di servizio ADSI
- Implementazione di ADSI Providers ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bdd0da406d9e65af898664e76b5e455540ebeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707414"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a><span data-ttu-id="8e344-106">Implementazione di provider di interfacce del servizio Active Directory</span><span class="sxs-lookup"><span data-stu-id="8e344-106">Implementing Active Directory Service Interfaces Providers</span></span>

<span data-ttu-id="8e344-107">Le interfacce ADSI (Active Directory Service Interfaces) sono interfacce COM che eseguono il wrapping di oggetti del servizio directory per esporli ai client dei servizi directory.</span><span class="sxs-lookup"><span data-stu-id="8e344-107">Active Directory Service Interfaces (ADSI) are COM interfaces that wrap directory service objects to expose them to clients of directory services.</span></span> <span data-ttu-id="8e344-108">Fornendo un'implementazione di ADSI, espandere la base client al set di applicazioni client ADSI.</span><span class="sxs-lookup"><span data-stu-id="8e344-108">By supplying an implementation of ADSI, you expand your client-base to the set of ADSI client applications.</span></span>

<span data-ttu-id="8e344-109">Come per qualsiasi implementazione COM, è possibile scrivere un provider ADSI in molte lingue.</span><span class="sxs-lookup"><span data-stu-id="8e344-109">As with any COM implementation, you can write an ADSI provider in many languages.</span></span> <span data-ttu-id="8e344-110">Le interfacce COM ADSI sono definite come interfacce duali che consentono la risoluzione dei nomi in fase di esecuzione e in fase di compilazione e possono essere chiamate da linguaggi conformi all'automazione, ad esempio Visual Basic, Visual Basic Scripting Edition, nonché i linguaggi più efficienti in termini di prestazioni e efficienza, ad esempio C e C++.</span><span class="sxs-lookup"><span data-stu-id="8e344-110">The ADSI COM interfaces are defined as dual interfaces that allow both run-time and compile-time name resolution and can be called by Automation-compliant languages such as Visual Basic, Visual Basic Scripting Edition, and also the more performance and efficiency-conscious languages such as C and C++.</span></span> <span data-ttu-id="8e344-111">I client ADSI includono inoltre le applicazioni Web che utilizzano Active Server pagine e gli snap-in di amministrazione tramite Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="8e344-111">ADSI clients also include web applications using Active Server Pages and administration snap-ins through the Microsoft Management Console.</span></span>

<span data-ttu-id="8e344-112">Poiché ADSI fornisce il proprio provider OLE DB, l'implementazione delle funzionalità di ricerca definite da [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) consente inoltre ai client ADSI di eseguire query sul servizio directory per i dati.</span><span class="sxs-lookup"><span data-stu-id="8e344-112">Because ADSI supplies its own OLE DB provider, implementing the search features defined by [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) also enables ADSI clients to query your directory service for data.</span></span>

<span data-ttu-id="8e344-113">Tutti gli oggetti del servizio di directory possono essere rappresentati tramite un oggetto ADSI generico che supporta [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="8e344-113">All directory service objects can be represented through a generic ADSI object supporting [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject).</span></span> <span data-ttu-id="8e344-114">ADSI fornisce i blocchi predefiniti necessari per rappresentare le funzionalità e i servizi di qualsiasi servizio di directory.</span><span class="sxs-lookup"><span data-stu-id="8e344-114">ADSI supplies the building blocks necessary to represent the features and services of any directory service.</span></span>

<span data-ttu-id="8e344-115">Inoltre, le metainterfacce ADSI rappresentano gli oggetti comuni utilizzati dagli amministratori di directory.</span><span class="sxs-lookup"><span data-stu-id="8e344-115">In addition, the ADSI meta-interfaces represent common objects used by directory administrators.</span></span> <span data-ttu-id="8e344-116">È possibile eseguire il mapping delle proprietà delle metainterfacce alle proprietà supportate dal servizio directory.</span><span class="sxs-lookup"><span data-stu-id="8e344-116">You map the properties of the meta-interfaces to the properties supported by your directory service.</span></span> <span data-ttu-id="8e344-117">I client ADSI che programmano le interfacce del servizio Active Directory ottengono l'accesso al servizio directory non appena il provider viene installato e il sistema viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="8e344-117">ADSI clients programming to the Active Directory Service Interfaces gain access to your directory service as soon as the provider is installed and the system restarted.</span></span>

<span data-ttu-id="8e344-118">Se il servizio Directory supporta una rappresentazione dello schema, il supporto delle interfacce di gestione dello schema rende lo spazio dei nomi accessibile direttamente ai browser del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="8e344-118">If your directory service supports a schema representation, supporting the schema management interfaces makes your namespace directly accessible to directory service browsers.</span></span> <span data-ttu-id="8e344-119">Grazie alla pubblicazione delle funzionalità tramite lo schema, i client possono eseguire query sul servizio directory online e usufruire dei servizi offerti.</span><span class="sxs-lookup"><span data-stu-id="8e344-119">By publishing your features through the schema, clients can query your directory service online and take advantage of the services you offer.</span></span> <span data-ttu-id="8e344-120">Grazie alla disponibilità dello schema online e al vantaggio dell'interfaccia COM, è possibile continuare a rendere disponibili nuove funzionalità per il software client, supportando al tempo stesso le versioni di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="8e344-120">Because of the online schema availability and the COM interface advantage, you can continue to make new features available to your client software while supporting down-level versions.</span></span>

 

 




