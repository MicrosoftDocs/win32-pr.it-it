---
description: I file di descrizione della libreria sono file XML che definiscono le librerie.
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: Schema Descrizione libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bebbd7ed168cd977530ccfeb0b319c33142687
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104981063"
---
# <a name="library-description-schema"></a><span data-ttu-id="cd4bc-103">Schema Descrizione libreria</span><span class="sxs-lookup"><span data-stu-id="cd4bc-103">Library Description Schema</span></span>

<span data-ttu-id="cd4bc-104">I file di descrizione della libreria sono file XML che definiscono le librerie.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-104">Library description files are XML files that define libraries.</span></span> <span data-ttu-id="cd4bc-105">Le librerie aggregano gli elementi da percorsi di archiviazione locali e remoti in una singola visualizzazione in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-105">Libraries aggregate items from local and remote storage locations into a single view in Windows Explorer.</span></span> <span data-ttu-id="cd4bc-106">I file di descrizione della libreria seguono lo schema della descrizione della libreria e vengono salvati come \* file con estensione library-ms.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-106">Library description files follow the Library Description schema and are saved as \*.library-ms files.</span></span>

<span data-ttu-id="cd4bc-107">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd4bc-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="cd4bc-108">Panoramica dello schema di descrizione della libreria</span><span class="sxs-lookup"><span data-stu-id="cd4bc-108">Overview of the Library Description Schema</span></span>](#overview-of-the-library-description-schema)
-   [<span data-ttu-id="cd4bc-109">Controllo delle versioni dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cd4bc-109">Namespace Versioning</span></span>](#namespace-versioning)
-   [<span data-ttu-id="cd4bc-110">Esempio di un file di descrizione della libreria</span><span class="sxs-lookup"><span data-stu-id="cd4bc-110">Example of a Library Description File</span></span>](#example-of-a-library-description-file)
-   [<span data-ttu-id="cd4bc-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cd4bc-111">Related topics</span></span>](#related-topics)

## <a name="overview-of-the-library-description-schema"></a><span data-ttu-id="cd4bc-112">Panoramica dello schema di descrizione della libreria</span><span class="sxs-lookup"><span data-stu-id="cd4bc-112">Overview of the Library Description Schema</span></span>

<span data-ttu-id="cd4bc-113">Le librerie contengono file archiviati in uno o più percorsi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-113">Libraries contain files that are stored in one or more storage locations.</span></span> <span data-ttu-id="cd4bc-114">Le librerie non archiviano effettivamente questi file; al contrario, monitorano le cartelle che contengono i file e consentono agli utenti di accedere ai file e disporli in modi diversi.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-114">Libraries do not actually store these files; instead, they monitor the folders that contain the files, and let users access and arrange the files in different ways.</span></span> <span data-ttu-id="cd4bc-115">Ad esempio, un utente può avere file musicali in più cartelle in un disco rigido locale e anche in un disco rigido esterno.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-115">For example, a user can have music files in multiple folders on a local hard disk and also on an external hard disk.</span></span> <span data-ttu-id="cd4bc-116">Utilizzando la **libreria musicale**, l'utente può accedere a tutti i file contemporaneamente e ordinarli tutti in base al nome dell'artista o al titolo dell'album come singolo gruppo.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-116">Using the **Music Library**, the user can access all of those files at the same time and sort them all by artist name or album title as a single group.</span></span>

<span data-ttu-id="cd4bc-117">Lo schema di descrizione della libreria è costituito da tre parti principali, descritte nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="cd4bc-117">The Library Description schema consists of three major parts, described in the following table:</span></span>



|                             |                                                                                                                                                            |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd4bc-118">Informazioni generali sulla libreria</span><span class="sxs-lookup"><span data-stu-id="cd4bc-118">General library information</span></span> | <span data-ttu-id="cd4bc-119">Informazioni sulla libreria, ad esempio nome, proprietario, versione, icona, che Esplora risorse può usare quando Visualizza la libreria a un utente.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-119">Information about the library, such as name, owner, version, icon, that Windows Explorer can use when it displays the library to a user.</span></span>                   |
| <span data-ttu-id="cd4bc-120">Proprietà libreria</span><span class="sxs-lookup"><span data-stu-id="cd4bc-120">Library properties</span></span>          | <span data-ttu-id="cd4bc-121">Una o più proprietà che descrivono la libreria.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-121">One or more properties that describe the library.</span></span> <span data-ttu-id="cd4bc-122">Queste proprietà personalizzate sono specifiche della libreria.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-122">These custom properties are specific to the library.</span></span>                                                     |
| <span data-ttu-id="cd4bc-123">Percorsi di libreria</span><span class="sxs-lookup"><span data-stu-id="cd4bc-123">Library locations</span></span>           | <span data-ttu-id="cd4bc-124">Uno o più connettori di ricerca che identificano i percorsi di archiviazione da includere nella libreria.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-124">One or more search connectors that identify storage locations to include in the library.</span></span> <span data-ttu-id="cd4bc-125">Ognuno di questi percorsi può avere anche un set univoco di proprietà.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-125">Each of these locations can also have a unique set of properties.</span></span> |



 

<span data-ttu-id="cd4bc-126">I file di libreria in Windows 7 sono archiviati nella cartella nota FOLDERID \_ Libraries.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-126">Library files in Windows 7 are stored in the known folder, FOLDERID\_Libraries.</span></span> <span data-ttu-id="cd4bc-127">Per impostazione predefinita, la \_ cartella FOLDERID Libraries si trova in% UserProfile% \\ AppData \\ roaming \\ Microsoft \\ Windows \\ Libraries.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-127">By default, the FOLDERID\_Libraries folder is located at %USERPROFILE%\\AppData\\Roaming\\Microsoft\\Windows\\Libraries.</span></span>

## <a name="namespace-versioning"></a><span data-ttu-id="cd4bc-128">Controllo delle versioni dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cd4bc-128">Namespace Versioning</span></span>

<span data-ttu-id="cd4bc-129">Le versioni del formato di file della descrizione della libreria ( \* . Library-MS) vengono rilevate modificando lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-129">Versions of the Library Description file format (\*.library-ms) are tracked by changing the namespace.</span></span> <span data-ttu-id="cd4bc-130">Per Windows 7, il formato del file è lo spazio dei nomi predefinito seguente: https://schemas.microsoft.com/windows/2009/library .</span><span class="sxs-lookup"><span data-stu-id="cd4bc-130">For Windows 7, the file format has the following default namespace: https://schemas.microsoft.com/windows/2009/library.</span></span>

<span data-ttu-id="cd4bc-131">Le versioni del contenuto della libreria, tuttavia, vengono rilevate usando l' [<version>](schema-library-version.md) elemento in un file di descrizione della libreria specifico.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-131">Versions of the library contents, however, are tracked by using the [<version>](schema-library-version.md) element in a specific Library Description file.</span></span>

## <a name="example-of-a-library-description-file"></a><span data-ttu-id="cd4bc-132">Esempio di un file di descrizione della libreria</span><span class="sxs-lookup"><span data-stu-id="cd4bc-132">Example of a Library Description File</span></span>

<span data-ttu-id="cd4bc-133">Di seguito è riportato un esempio di un file di descrizione della libreria che definisce una raccolta per i file di documento.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-133">The following is an example of a Library Description file that defines a library for document files.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
    <name>@shell32.dll,-34575</name>
    <ownerSID>S-1-5-21-379071477-2495173225-776587366-1000</ownerSID>
    <version>1</version>
    <isLibraryPinned>true</isLibraryPinned>
    <iconReference>imageres.dll,-1002</iconReference>
    <templateInfo>
        <folderType>{7d49d726-3c21-4f05-99aa-fdc2c9474656}</folderType>
    </templateInfo>
    <searchConnectorDescriptionList>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34577</description>
            <isDefaultSaveLocation>true</isDefaultSaveLocation>
            <simpleLocation>
                <url>knownfolder:{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</url>
                <serialized>MBAAAEAFCAAA...MFNVAAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34579</description>
            <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
            <simpleLocation>
                <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
                <serialized>MBAAAEAFCAAA...HJIfK9AAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
    </searchConnectorDescriptionList>
</libraryDescription>
```



## <a name="related-topics"></a><span data-ttu-id="cd4bc-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cd4bc-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd4bc-135">Elemento folderType (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-135">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="cd4bc-136">Elemento iconReference (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-136">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="cd4bc-137">Elemento isLibraryPinned (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-137">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="cd4bc-138">Elemento libraryDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-138">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="cd4bc-139">Elemento Name (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-139">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="cd4bc-140">Elemento ownerSID (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-140">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="cd4bc-141">Elemento Property (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-141">property Element (Library Schema)</span></span>](schema-library-property.md)
</dt> <dt>

[<span data-ttu-id="cd4bc-142">Elemento propertyStore (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-142">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="cd4bc-143">Elemento searchConnectorDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-143">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="cd4bc-144">Elemento searchConnectorDescriptionList (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-144">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="cd4bc-145">Elemento templateInfo (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-145">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="cd4bc-146">Elemento Version (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-146">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> <dt>

[<span data-ttu-id="cd4bc-147">Cerca nello schema di descrizione del connettore</span><span class="sxs-lookup"><span data-stu-id="cd4bc-147">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
