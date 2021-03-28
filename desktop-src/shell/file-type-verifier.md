---
description: Il tipo di file Verifier è uno strumento che consente ai fornitori di software indipendenti (ISV) di verificare che i tipi di file univoci siano implementati correttamente.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Tipo di file Verifier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8e4a588e4889241762a9d8e0567d4a4542c0255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881593"
---
# <a name="file-type-verifier"></a><span data-ttu-id="d5f5b-103">Tipo di file Verifier</span><span class="sxs-lookup"><span data-stu-id="d5f5b-103">File Type Verifier</span></span>

<span data-ttu-id="d5f5b-104">Il tipo di file Verifier è uno strumento che consente ai fornitori di software indipendenti (ISV) di verificare che i tipi di file univoci siano implementati correttamente.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-104">The File Type Verifier is a tool that enables independent software vendors (ISVs) to verify that their unique file types are implemented correctly.</span></span> <span data-ttu-id="d5f5b-105">Le implementazioni di qualità elevata dei gestori di tipi di file sono fondamentali per un'esperienza utente ottimale perché gli utenti interagiscono con il formato di file in molti modi in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-105">High quality implementations of your file type handlers are crucial for a good user experience because users interact with your file format in many ways in Windows Explorer.</span></span> <span data-ttu-id="d5f5b-106">Gli utenti possono eseguire ricerche full-text, ordinare in base a metadati personalizzati o visualizzare anteprime e anteprime avanzate del formato di file.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-106">Users can do full-text searches, sort by custom metadata, or view rich thumbnails and previews of your file format.</span></span>

<span data-ttu-id="d5f5b-107">Per istruzioni sull'utilizzo del verificatore del tipo di file, vedere [come utilizzare il tipo di file Verifier](how-to-use-the-file-type-verifier.md).</span><span class="sxs-lookup"><span data-stu-id="d5f5b-107">For instructions on using the File Type Verifier, see [How To Use the File Type Verifier](how-to-use-the-file-type-verifier.md).</span></span>

## <a name="about-the-file-type-verifier-tool"></a><span data-ttu-id="d5f5b-108">Informazioni sullo strumento File Type Verifier</span><span class="sxs-lookup"><span data-stu-id="d5f5b-108">About the File Type Verifier Tool</span></span>

<span data-ttu-id="d5f5b-109">Il tipo di file Verifier è un programma disponibile come parte di [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d5f5b-109">File Type Verifier is a program that is available as part of the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d5f5b-110">È progettato per aiutare gli sviluppatori che creano tipi di [file](fa-file-types.md) Windows personalizzati per rilevare potenziali problemi con i tipi di file.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-110">It is designed to help developers who create custom Windows [File Types](fa-file-types.md) to detect potential issues with their file types.</span></span> <span data-ttu-id="d5f5b-111">Sebbene il verificatore del tipo di file venga eseguito solo in Windows 7 e versioni successive, le regole applicate dal Verifier del tipo di file si applicano a tutte le versioni di Windows in cui sono disponibili le funzionalità che controlla.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-111">Although the File Type Verifier runs only on Windows 7 and later, the rules that the File Type Verifier enforces apply to all versions of Windows where the features it checks are available.</span></span>

<span data-ttu-id="d5f5b-112">Il tipo di file Verifier esegue diversi test sul tipo di file per verificare che sia correttamente registrato e che fornisca i [gestori dei tipi di file](fa-file-extensions.md) appropriati per visualizzare il tipo di file correttamente in Esplora risorse e, quando appropriato, supporta l'indicizzazione del contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="d5f5b-112">The File Type Verifier runs several tests on the file type to verify that it is properly registered, and that it provides the appropriate [File Type Handlers](fa-file-extensions.md) to display the file type properly in Windows Explorer, and when appropriate, that it supports indexing the file content.</span></span>

<span data-ttu-id="d5f5b-113">Il tipo di file Verifier Verifica gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d5f5b-113">The File Type Verifier tests the following things:</span></span>

-   [<span data-ttu-id="d5f5b-114">Gestori di anteprime</span><span class="sxs-lookup"><span data-stu-id="d5f5b-114">Preview Handlers</span></span>](building-preview-handlers.md)
-   [<span data-ttu-id="d5f5b-115">Gestori di anteprime</span><span class="sxs-lookup"><span data-stu-id="d5f5b-115">Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
-   [<span data-ttu-id="d5f5b-116">Gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="d5f5b-116">Property Handlers</span></span>](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [<span data-ttu-id="d5f5b-117">Gestori di verbi</span><span class="sxs-lookup"><span data-stu-id="d5f5b-117">Verb Handlers</span></span>](fa-verbs.md)
-   [<span data-ttu-id="d5f5b-118">Filtri (IFilter)</span><span class="sxs-lookup"><span data-stu-id="d5f5b-118">Filters (IFilter)</span></span>](../search/-search-3x-wds-extidx-filters.md)
-   [<span data-ttu-id="d5f5b-119">Associazioni di tipo</span><span class="sxs-lookup"><span data-stu-id="d5f5b-119">Kind Associations</span></span>](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="d5f5b-120">Tipi percepiti</span><span class="sxs-lookup"><span data-stu-id="d5f5b-120">Perceived Types</span></span>](fa-perceivedtypes.md)
-   [<span data-ttu-id="d5f5b-121">Proprietà importanti</span><span class="sxs-lookup"><span data-stu-id="d5f5b-121">Important Properties</span></span>](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a><span data-ttu-id="d5f5b-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5f5b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5f5b-123">Come utilizzare il tipo di file Verifier</span><span class="sxs-lookup"><span data-stu-id="d5f5b-123">How To Use the File Type Verifier</span></span>](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="d5f5b-124">Registrazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="d5f5b-124">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="d5f5b-125">Tipi di file</span><span class="sxs-lookup"><span data-stu-id="d5f5b-125">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="d5f5b-126">Funzionamento delle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="d5f5b-126">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="d5f5b-127">Visualizzazione contenuto per tipo di file o tipo</span><span class="sxs-lookup"><span data-stu-id="d5f5b-127">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="d5f5b-128">Gestori di tipi di file</span><span class="sxs-lookup"><span data-stu-id="d5f5b-128">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="d5f5b-129">Identificatori a livello di codice</span><span class="sxs-lookup"><span data-stu-id="d5f5b-129">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="d5f5b-130">Tipi percepiti</span><span class="sxs-lookup"><span data-stu-id="d5f5b-130">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="d5f5b-131">Matrici di associazione</span><span class="sxs-lookup"><span data-stu-id="d5f5b-131">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
