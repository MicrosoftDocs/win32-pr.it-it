---
description: Il componente lettore note Microsoft Windows Journal fornisce l'accesso in lettura a livello di codice ai file nel formato journal.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Utilizzo del componente Reader Journal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fd098db4ce1c0c92a5ded76b0950e264aa2a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966649"
---
# <a name="using-the-journal-reader-component"></a><span data-ttu-id="7f564-103">Utilizzo del componente Reader Journal</span><span class="sxs-lookup"><span data-stu-id="7f564-103">Using the Journal Reader Component</span></span>

<span data-ttu-id="7f564-104">Il componente lettore note Microsoft Windows Journal fornisce l'accesso in lettura a livello di codice ai file nel formato journal.</span><span class="sxs-lookup"><span data-stu-id="7f564-104">The Microsoft Windows Journal Note Reader component provides programmatic read access to files in the Journal format.</span></span>

## <a name="component-overview"></a><span data-ttu-id="7f564-105">Panoramica sui componenti</span><span class="sxs-lookup"><span data-stu-id="7f564-105">Component Overview</span></span>

<span data-ttu-id="7f564-106">File journal con estensione JNT.</span><span class="sxs-lookup"><span data-stu-id="7f564-106">Journal files have the .jnt file extension.</span></span> <span data-ttu-id="7f564-107">Questo componente semplice accetta un flusso contenente un file con estensione JNT e restituisce un flusso contenente il contenuto del file in formato XML.</span><span class="sxs-lookup"><span data-stu-id="7f564-107">This simple component takes a stream containing a .jnt file and returns a stream containing the file's content in XML format.</span></span> <span data-ttu-id="7f564-108">Il codice XML restituito dal componente è conforme allo schema del lettore di note del journal.</span><span class="sxs-lookup"><span data-stu-id="7f564-108">The XML returned by the component conforms to the Journal Note Reader schema.</span></span> <span data-ttu-id="7f564-109">Questo schema è documentato in [Journal Reader Schema Reference](journal-reader-schema-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7f564-109">This schema is documented in [Journal Reader Schema Reference](journal-reader-schema-reference.md).</span></span>

<span data-ttu-id="7f564-110">Il componente non offre la possibilità di scrivere file con estensione JNT.</span><span class="sxs-lookup"><span data-stu-id="7f564-110">The component does not provide the ability to write out .jnt files.</span></span>

<span data-ttu-id="7f564-111">Il componente è disponibile nelle versioni gestite e non gestite.</span><span class="sxs-lookup"><span data-stu-id="7f564-111">The component is available in unmanaged and managed versions.</span></span> <span data-ttu-id="7f564-112">Il componente non gestito è disponibile nella libreria a collegamento dinamico (DLL) di journal.dll.</span><span class="sxs-lookup"><span data-stu-id="7f564-112">The unmanaged component is available in the journal.dll dynamic link library (DLL).</span></span> <span data-ttu-id="7f564-113">La versione gestita è nell'assembly Microsoft.Ink.Journal.dll (per la ridistribuzione a Windows XP Tablet PC Edition o Windows Vista) o Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="7f564-113">The managed version is either in the Microsoft.Ink.Journal.dll assembly (for redistribution to Windows XP Tablet PC Edition or Windows Vista), or Microsoft.Ink.dll.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="7f564-114">A partire da Windows 10, versione 1607, journal.dll non è incluso nel sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="7f564-114">Beginning with Windows 10, version 1607, journal.dll is not included in the Windows operating system.</span></span> <span data-ttu-id="7f564-115">Tale libreria deve essere considerata deprecata o obsoleta e non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7f564-115">That library should be considered deprecated or obsolete and should not be used.</span></span>

 

### <a name="assembly-changes-of-note"></a><span data-ttu-id="7f564-116">Modifiche all'assembly della nota</span><span class="sxs-lookup"><span data-stu-id="7f564-116">Assembly Changes of Note</span></span>

<span data-ttu-id="7f564-117">È importante tenere presente alcune modifiche apportate all'assembly contenente il componente Reader note Journal che si è verificato tra la versione rilasciata in combinazione con la versione 1,7 del kit per sviluppatori di Tablet e la versione fornita nel sistema operativo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7f564-117">It is important to be aware of some changes to the assembly containing the Journal Note Reader component that occurred between the version released in conjunction with version 1.7 of the Tablet Developers Kit and the version that ships in the Windows Vista operating system.</span></span>

<span data-ttu-id="7f564-118">La versione 1,7 del componente Reader, che può essere ridistribuita in Windows XP o Windows Vista, è contenuta in un assembly denominato Microsoft.Ink.Journal.dll.</span><span class="sxs-lookup"><span data-stu-id="7f564-118">The 1.7 version of the reader component, which can be redistributed to either Windows XP or Windows Vista, is contained in an assembly called Microsoft.Ink.Journal.dll.</span></span> <span data-ttu-id="7f564-119">Il componente Reader è incluso in Windows Vista, ma è stato integrato nell'assembly di base Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="7f564-119">The reader component ships in Windows Vista, but has been integrated into the core Microsoft.Ink.dll assembly.</span></span> <span data-ttu-id="7f564-120">Ciò significa che le applicazioni che usano l'assembly 1,7 devono ridistribuire l'assembly con la relativa configurazione.</span><span class="sxs-lookup"><span data-stu-id="7f564-120">This means that applications that make use of the 1.7 assembly need to redistribute that assembly with their setup.</span></span>

## <a name="using-the-component"></a><span data-ttu-id="7f564-121">Utilizzo del componente</span><span class="sxs-lookup"><span data-stu-id="7f564-121">Using the Component</span></span>

<span data-ttu-id="7f564-122">Il componente Reader note Journal è utile per estrarre i dati di input penna e altre informazioni sul file da un file journal.</span><span class="sxs-lookup"><span data-stu-id="7f564-122">The Journal Note Reader component is useful for extracting the ink data and other information about the file from a Journal file.</span></span>

### <a name="com"></a><span data-ttu-id="7f564-123">COM</span><span class="sxs-lookup"><span data-stu-id="7f564-123">COM</span></span>

<span data-ttu-id="7f564-124">Il componente COM Journal note Reader si trova nel file Journal.dll, che viene installato e registrato quando si scarica e si esegue il file di installazione Journal note Reader.</span><span class="sxs-lookup"><span data-stu-id="7f564-124">The Journal Note Reader COM component is in the file Journal.dll, which is installed and registered when you download and run the Journal Note Reader installation file.</span></span>

<span data-ttu-id="7f564-125">Il componente COM non supporta l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="7f564-125">The COM component does not support the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span>

### <a name="managed"></a><span data-ttu-id="7f564-126">Gestita</span><span class="sxs-lookup"><span data-stu-id="7f564-126">Managed</span></span>

<span data-ttu-id="7f564-127">Il componente del Journal note Reader gestito si trova nell'assembly Microsoft.Ink.JournalReader.dll.</span><span class="sxs-lookup"><span data-stu-id="7f564-127">The Journal Note Reader managed component is in the Microsoft.Ink.JournalReader.dll assembly.</span></span> <span data-ttu-id="7f564-128">Questo assembly viene installato e registrato nella Global Assembly Cache quando si esegue il file di installazione Journal note Reader.</span><span class="sxs-lookup"><span data-stu-id="7f564-128">This assembly is installed and registered in the global assembly cache when you run the Journal Note Reader installation file.</span></span>

<span data-ttu-id="7f564-129">Aggiungere un riferimento all'assembly per utilizzarlo nel progetto gestito.</span><span class="sxs-lookup"><span data-stu-id="7f564-129">Add a reference to the assembly to use it in your managed project.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f564-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f564-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f564-131">**Interfaccia IJournalReader**</span><span class="sxs-lookup"><span data-stu-id="7f564-131">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> <dt>

[<span data-ttu-id="7f564-132">Riferimento allo schema del lettore Journal</span><span class="sxs-lookup"><span data-stu-id="7f564-132">Journal Reader Schema Reference</span></span>](journal-reader-schema-reference.md)
</dt> </dl>

 

 
