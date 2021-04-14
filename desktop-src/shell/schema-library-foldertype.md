---
description: L' <folderType> elemento specifica un GUID per il tipo di cartella. Questo elemento è obbligatorio se l' <templateInfo> elemento esiste, in caso contrario è facoltativo. Questo elemento non ha attributi e nessun elemento figlio.
title: Elemento folderType (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c6d94906fa8c0debfa1ee49d95f5acd47aea2526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977858"
---
# <a name="foldertype-element-library-schema"></a><span data-ttu-id="c725f-105">Elemento folderType (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="c725f-105">folderType Element (Library Schema)</span></span>

<span data-ttu-id="c725f-106">L' <folderType> elemento specifica un GUID per il tipo di cartella.</span><span class="sxs-lookup"><span data-stu-id="c725f-106">The <folderType> element specifies a GUID for the folder type.</span></span> <span data-ttu-id="c725f-107">Questo elemento è obbligatorio se l' <templateInfo> elemento esiste, in caso contrario è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c725f-107">This element is required if the <templateInfo> element exists, otherwise it is optional.</span></span> <span data-ttu-id="c725f-108">Questo elemento non ha attributi e nessun elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="c725f-108">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="c725f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c725f-109">Syntax</span></span>


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="c725f-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c725f-110">Element Information</span></span>



| <span data-ttu-id="c725f-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="c725f-111">Parent Element</span></span>                                                           | <span data-ttu-id="c725f-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c725f-112">Child Elements</span></span> |
|--------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="c725f-113">Elemento templateInfo (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="c725f-113">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="c725f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c725f-114">Remarks</span></span>

<span data-ttu-id="c725f-115">L'impostazione di un tipo di cartella determina le colonne e i dettagli visualizzati in Esplora risorse per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c725f-115">Setting a folder type determines the columns and details that appear in Windows Explorer by default.</span></span> <span data-ttu-id="c725f-116">Gli identificatori del tipo di cartella ([**FOLDERTYPEID**](foldertypeid.md)) sono GUID definiti in Shlguid. h.</span><span class="sxs-lookup"><span data-stu-id="c725f-116">Folder type identifiers ([**FOLDERTYPEID**](foldertypeid.md)) are GUIDs defined in Shlguid.h.</span></span> <span data-ttu-id="c725f-117">Nella tabella seguente sono elencati i GUID dei tipi di cartelle comuni.</span><span class="sxs-lookup"><span data-stu-id="c725f-117">The following table lists the GUIDs of common folder types.</span></span>



| <span data-ttu-id="c725f-118">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="c725f-118">Folder Type</span></span>      | <span data-ttu-id="c725f-119">GUID</span><span class="sxs-lookup"><span data-stu-id="c725f-119">GUID</span></span>                                   |
|------------------|----------------------------------------|
| <span data-ttu-id="c725f-120">Libreria generica</span><span class="sxs-lookup"><span data-stu-id="c725f-120">Generic Library</span></span>  | <span data-ttu-id="c725f-121">{5f4eab9a-6833-4f61-899d-31cf46979d49}</span><span class="sxs-lookup"><span data-stu-id="c725f-121">{5f4eab9a-6833-4f61-899d-31cf46979d49}</span></span> |
| <span data-ttu-id="c725f-122">Librerie utenti</span><span class="sxs-lookup"><span data-stu-id="c725f-122">Users Libraries</span></span>  | <span data-ttu-id="c725f-123">{C4D98F09-6124-4fe0-9942-826416082DA9}</span><span class="sxs-lookup"><span data-stu-id="c725f-123">{C4D98F09-6124-4fe0-9942-826416082DA9}</span></span> |
| <span data-ttu-id="c725f-124">Cartella documenti</span><span class="sxs-lookup"><span data-stu-id="c725f-124">Documents Folder</span></span> | <span data-ttu-id="c725f-125">{7D49D726-3C21-4F05-99AA-FDC2C9474656}</span><span class="sxs-lookup"><span data-stu-id="c725f-125">{7D49D726-3C21-4F05-99AA-FDC2C9474656}</span></span> |
| <span data-ttu-id="c725f-126">Cartella immagini</span><span class="sxs-lookup"><span data-stu-id="c725f-126">Pictures Folder</span></span>  | <span data-ttu-id="c725f-127">{B3690E58-E961-423B-B687-386EBFD83239}</span><span class="sxs-lookup"><span data-stu-id="c725f-127">{B3690E58-E961-423B-B687-386EBFD83239}</span></span> |
| <span data-ttu-id="c725f-128">Cartella video</span><span class="sxs-lookup"><span data-stu-id="c725f-128">Videos Folder</span></span>    | <span data-ttu-id="c725f-129">{5fa96407-7e77-483c-ac93-691d05850de8}</span><span class="sxs-lookup"><span data-stu-id="c725f-129">{5fa96407-7e77-483c-ac93-691d05850de8}</span></span> |
| <span data-ttu-id="c725f-130">Cartella giochi</span><span class="sxs-lookup"><span data-stu-id="c725f-130">Games Folder</span></span>     | <span data-ttu-id="c725f-131">{b689b0d0-76d3-4cbb-87f7-585d0e0ce070}</span><span class="sxs-lookup"><span data-stu-id="c725f-131">{b689b0d0-76d3-4cbb-87f7-585d0e0ce070}</span></span> |
| <span data-ttu-id="c725f-132">Cartella musica</span><span class="sxs-lookup"><span data-stu-id="c725f-132">Music Folder</span></span>     | <span data-ttu-id="c725f-133">{94d6ddcc-4a68-4175-a374-bd584a510b78}</span><span class="sxs-lookup"><span data-stu-id="c725f-133">{94d6ddcc-4a68-4175-a374-bd584a510b78}</span></span> |
| <span data-ttu-id="c725f-134">Contatti</span><span class="sxs-lookup"><span data-stu-id="c725f-134">Contacts</span></span>         | <span data-ttu-id="c725f-135">{DE2B70EC-9BF7-4A93-BD3D-243F7881D492}</span><span class="sxs-lookup"><span data-stu-id="c725f-135">{DE2B70EC-9BF7-4A93-BD3D-243F7881D492}</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c725f-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c725f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c725f-137">Elemento iconReference (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="c725f-137">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="c725f-138">Elemento isLibraryPinned (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="c725f-138">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="c725f-139">Elemento libraryDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="c725f-139">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="c725f-140">Elemento Name (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="c725f-140">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="c725f-141">Elemento ownerSID (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="c725f-141">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="c725f-142">Elemento propertyStore (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="c725f-142">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="c725f-143">Elemento searchConnectorDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="c725f-143">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="c725f-144">Elemento searchConnectorDescriptionList (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="c725f-144">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="c725f-145">Elemento templateInfo (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="c725f-145">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="c725f-146">Elemento Version (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="c725f-146">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> </dl>

 

 



