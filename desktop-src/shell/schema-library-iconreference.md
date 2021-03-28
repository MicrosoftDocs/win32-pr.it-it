---
description: L' <iconReference> elemento specifica un'icona personalizzata per questa libreria. Questo elemento è facoltativo e non dispone di attributi o elementi figlio.
title: Elemento iconReference (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f307ecd4fa523cc28881164869dca3329dfd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994149"
---
# <a name="iconreference-element-library-schema"></a><span data-ttu-id="32a1b-104">Elemento iconReference (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="32a1b-104">iconReference Element (Library Schema)</span></span>

<span data-ttu-id="32a1b-105">L' <iconReference> elemento specifica un'icona personalizzata per questa libreria.</span><span class="sxs-lookup"><span data-stu-id="32a1b-105">The <iconReference> element specifies a custom icon for this library.</span></span> <span data-ttu-id="32a1b-106">Questo elemento è facoltativo e non dispone di attributi o elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="32a1b-106">This element is optional and has no attributes or child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="32a1b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32a1b-107">Syntax</span></span>


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a><span data-ttu-id="32a1b-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="32a1b-108">Element Information</span></span>



| <span data-ttu-id="32a1b-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="32a1b-109">Parent Element</span></span>                                                               | <span data-ttu-id="32a1b-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="32a1b-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="32a1b-111">Elemento libraryDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="32a1b-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="32a1b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="32a1b-112">Remarks</span></span>

<span data-ttu-id="32a1b-113">Il riferimento all'icona deve essere specificato in un formato appropriato per la funzione [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) .</span><span class="sxs-lookup"><span data-stu-id="32a1b-113">The icon reference must be specified in a form suitable for the [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) function.</span></span> <span data-ttu-id="32a1b-114">Ad esempio: `ModuleFileName,IconResourceIndex`.</span><span class="sxs-lookup"><span data-stu-id="32a1b-114">For example: `ModuleFileName,IconResourceIndex`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32a1b-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="32a1b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32a1b-116">Elemento folderType (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="32a1b-116">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="32a1b-117">Elemento isLibraryPinned (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="32a1b-117">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="32a1b-118">Elemento libraryDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="32a1b-118">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="32a1b-119">Elemento Name (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="32a1b-119">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="32a1b-120">Elemento ownerSID (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="32a1b-120">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="32a1b-121">Elemento propertyStore (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="32a1b-121">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="32a1b-122">Elemento searchConnectorDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="32a1b-122">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="32a1b-123">Elemento searchConnectorDescriptionList (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="32a1b-123">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="32a1b-124">Elemento templateInfo (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="32a1b-124">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="32a1b-125">Elemento Version (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="32a1b-125">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> </dl>

 

 



