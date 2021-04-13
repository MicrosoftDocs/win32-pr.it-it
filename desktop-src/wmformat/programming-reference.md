---
title: Guida di riferimento alla programmazione di Windows Media Format SDK
description: Guida di riferimento alla programmazione di Windows Media Format SDK
ms.assetid: cafb8aa7-6b0a-4bcc-b618-2520a31cd7a6
keywords:
- Windows Media Format SDK, Guida di riferimento alla programmazione
- Windows Media Format SDK, Advanced Systems Format (ASF)
- ASF (Advanced Systems Format), Guida di riferimento alla programmazione
- ASF (Advanced Systems Format), Guida di riferimento alla programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c316b85e91c31b513fbfcdff003ba37efea93b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400149"
---
# <a name="windows-media-format-sdk-programming-reference"></a><span data-ttu-id="f06b7-107">Guida di riferimento alla programmazione di Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="f06b7-107">Windows Media Format SDK Programming Reference</span></span>

<span data-ttu-id="f06b7-108">Il Software Development Kit (SDK) di Microsoft® Windows Media® Format supporta una gamma di oggetti, interfacce, funzioni indipendenti, strutture, tipi di enumerazione, attributi e così via.</span><span class="sxs-lookup"><span data-stu-id="f06b7-108">The Microsoft® Windows Media® Format Software Development Kit (SDK) supports a range of objects, interfaces, independent functions, structures, enumeration types, attributes, and so on.</span></span> <span data-ttu-id="f06b7-109">Le sezioni seguenti illustrano in dettaglio questi argomenti.</span><span class="sxs-lookup"><span data-stu-id="f06b7-109">The following sections document these in detail.</span></span>



| <span data-ttu-id="f06b7-110">Sezione</span><span class="sxs-lookup"><span data-stu-id="f06b7-110">Section</span></span>                                                                              | <span data-ttu-id="f06b7-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f06b7-111">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f06b7-112">Oggetti</span><span class="sxs-lookup"><span data-stu-id="f06b7-112">Objects</span></span>](objects.md)                                                               | <span data-ttu-id="f06b7-113">Vengono descritti gli oggetti e le interfacce supportate da ogni oggetto in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="f06b7-113">Describes the objects and the interfaces supported by each object in the Windows Media Format SDK.</span></span>           |
| [<span data-ttu-id="f06b7-114">Funzioni</span><span class="sxs-lookup"><span data-stu-id="f06b7-114">Functions</span></span>](functions.md)                                                           | <span data-ttu-id="f06b7-115">Descrive tutte le funzioni indipendenti, in genere quelle utilizzate per creare e inizializzare vari oggetti.</span><span class="sxs-lookup"><span data-stu-id="f06b7-115">Describes all the independent functions, typically those used to create and initialize various objects.</span></span>      |
| [<span data-ttu-id="f06b7-116">Interfacce</span><span class="sxs-lookup"><span data-stu-id="f06b7-116">Interfaces</span></span>](interfaces.md)                                                         | <span data-ttu-id="f06b7-117">Descrive tutte le interfacce e i metodi in questo SDK.</span><span class="sxs-lookup"><span data-stu-id="f06b7-117">Describes all the interfaces and methods in this SDK.</span></span>                                                        |
| [<span data-ttu-id="f06b7-118">Strutture</span><span class="sxs-lookup"><span data-stu-id="f06b7-118">Structures</span></span>](structures.md)                                                         | <span data-ttu-id="f06b7-119">Descrive le strutture supportate da questo SDK.</span><span class="sxs-lookup"><span data-stu-id="f06b7-119">Describes the structures supported by this SDK.</span></span>                                                              |
| [<span data-ttu-id="f06b7-120">Tipi di enumerazione</span><span class="sxs-lookup"><span data-stu-id="f06b7-120">Enumeration Types</span></span>](enumeration-types.md)                                           | <span data-ttu-id="f06b7-121">Descrive i tipi di enumerazione supportati da questo SDK.</span><span class="sxs-lookup"><span data-stu-id="f06b7-121">Describes the enumeration types supported by this SDK.</span></span>                                                       |
| [<span data-ttu-id="f06b7-122">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="f06b7-122">Attributes</span></span>](attributes.md)                                                         | <span data-ttu-id="f06b7-123">Vengono descritti gli attributi che possono essere specificati nelle intestazioni dei file ASF.</span><span class="sxs-lookup"><span data-stu-id="f06b7-123">Describes the attributes that can be specified in the headers of ASF files.</span></span>                                  |
| [<span data-ttu-id="f06b7-124">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="f06b7-124">Media Types</span></span>](media-types.md)                                                       | <span data-ttu-id="f06b7-125">Descrive gli identificatori del tipo di supporto usati da questo SDK.</span><span class="sxs-lookup"><span data-stu-id="f06b7-125">Describes the media type identifiers used by this SDK.</span></span>                                                       |
| [<span data-ttu-id="f06b7-126">Impostazioni di output</span><span class="sxs-lookup"><span data-stu-id="f06b7-126">Output Settings</span></span>](output-settings.md)                                               | <span data-ttu-id="f06b7-127">Descrive le costanti globali utilizzate per identificare le impostazioni di output del lettore.</span><span class="sxs-lookup"><span data-stu-id="f06b7-127">Describes the global constants used to identify reader output settings.</span></span>                                      |
| [<span data-ttu-id="f06b7-128">Stringhe relative a lingue</span><span class="sxs-lookup"><span data-stu-id="f06b7-128">Language Strings</span></span>](language-strings.md)                                             | <span data-ttu-id="f06b7-129">Vengono descritti gli identificatori di linguaggio conformi a RFC 1766 di uso comune.</span><span class="sxs-lookup"><span data-stu-id="f06b7-129">Describes the commonly used RFC 1766-compliant language identifiers.</span></span>                                         |
| [<span data-ttu-id="f06b7-130">Parametri del modello di conformità del dispositivo</span><span class="sxs-lookup"><span data-stu-id="f06b7-130">Device Conformance Template Parameters</span></span>](device-conformance-template-parameters.md) | <span data-ttu-id="f06b7-131">Descrive i modelli di conformità dei dispositivi, che descrivono gli intervalli di valori appropriati per i vari dispositivi.</span><span class="sxs-lookup"><span data-stu-id="f06b7-131">Describes the device conformance templates, which describe ranges of values appropriate for various devices.</span></span> |
| [<span data-ttu-id="f06b7-132">Profili di sistema</span><span class="sxs-lookup"><span data-stu-id="f06b7-132">System Profiles</span></span>](system-profiles.md)                                               | <span data-ttu-id="f06b7-133">Elenca tutti i profili di sistema supportati.</span><span class="sxs-lookup"><span data-stu-id="f06b7-133">Lists all supported system profiles.</span></span>                                                                         |
| [<span data-ttu-id="f06b7-134">Profili di sistema localizzati</span><span class="sxs-lookup"><span data-stu-id="f06b7-134">Localized System Profiles</span></span>](localized-system-profiles.md)                           | <span data-ttu-id="f06b7-135">Elenca i file del profilo di sistema localizzati inclusi nell'SDK e le lingue associate a ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="f06b7-135">Lists the localized system profile files included with the SDK and the languages associated with each.</span></span>       |
| [<span data-ttu-id="f06b7-136">Valori GUID</span><span class="sxs-lookup"><span data-stu-id="f06b7-136">GUID Values</span></span>](guid-values.md)                                                       | <span data-ttu-id="f06b7-137">Descrive i valori GUID usati da questo SDK.</span><span class="sxs-lookup"><span data-stu-id="f06b7-137">Describes the GUID values used by this SDK.</span></span>                                                                  |
| [<span data-ttu-id="f06b7-138">Codici errore</span><span class="sxs-lookup"><span data-stu-id="f06b7-138">Error Codes</span></span>](error-codes.md)                                                       | <span data-ttu-id="f06b7-139">Vengono descritti i codici di errore comuni restituiti da metodi e funzioni nell'SDK.</span><span class="sxs-lookup"><span data-stu-id="f06b7-139">Describes common error codes returned by methods and functions in the SDK.</span></span>                                   |
| [<span data-ttu-id="f06b7-140">Plug-in di origine</span><span class="sxs-lookup"><span data-stu-id="f06b7-140">Source Plug-ins</span></span>](source-plug-ins.md)                                               | <span data-ttu-id="f06b7-141">Vengono descritti i requisiti per le origini implementate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f06b7-141">Describes the requirements for user-implemented sources.</span></span>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="f06b7-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f06b7-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f06b7-143">**Informazioni su Windows Media Format SDK**</span><span class="sxs-lookup"><span data-stu-id="f06b7-143">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="f06b7-144">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="f06b7-144">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="f06b7-145">**SDK di Windows Media Format 11**</span><span class="sxs-lookup"><span data-stu-id="f06b7-145">**Windows Media Format 11 SDK**</span></span>](windows-media-format-11-sdk.md)
</dt> </dl>

 

 




