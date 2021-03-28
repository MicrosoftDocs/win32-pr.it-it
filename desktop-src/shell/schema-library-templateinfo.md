---
description: L' <templateInfo> elemento è un contenitore per l'elemento FolderType, che specifica un tipo di cartella per la visualizzazione dei risultati di una query su questa libreria. Questo elemento è facoltativo e non ha attributi.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Elemento templateInfo (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dae06a57a1b30407e2513e03f30ae6a4da13e849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527306"
---
# <a name="templateinfo-element-library-schema"></a><span data-ttu-id="71f7d-104">Elemento templateInfo (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="71f7d-104">templateInfo Element (Library Schema)</span></span>

<span data-ttu-id="71f7d-105">L' <templateInfo> elemento è un contenitore per l'elemento [FolderType](schema-library-foldertype.md) , che specifica un tipo di cartella per la visualizzazione dei risultati di una query su questa libreria.</span><span class="sxs-lookup"><span data-stu-id="71f7d-105">The <templateInfo> element is a container for the [folderType](schema-library-foldertype.md) element, which specifies a folder type for displaying the results from a query over this library.</span></span> <span data-ttu-id="71f7d-106">Questo elemento è facoltativo e non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="71f7d-106">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="71f7d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71f7d-107">Syntax</span></span>

``` syntax
<!-- templateInfo -->
<xs:element name="templateInfo" minOccurs="0">
    <xs:complexType>
        <xs:all>
            <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="71f7d-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="71f7d-108">Element Information</span></span>



| <span data-ttu-id="71f7d-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="71f7d-109">Parent Element</span></span>                                                               | <span data-ttu-id="71f7d-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="71f7d-110">Child Elements</span></span>                                                             |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="71f7d-111">Elemento libraryDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="71f7d-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="71f7d-112">Elemento folderType (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="71f7d-112">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)       |
|                                                                              | [<span data-ttu-id="71f7d-113">Elemento propertyStore (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="71f7d-113">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md) |



 

## <a name="related-topics"></a><span data-ttu-id="71f7d-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71f7d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71f7d-115">Schema Descrizione libreria</span><span class="sxs-lookup"><span data-stu-id="71f7d-115">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

<span data-ttu-id="71f7d-116">[Cerca nello schema di descrizione del connettore](/previous-versions//dd743009(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="71f7d-116">[Search Connector Description Schema](/previous-versions//dd743009(v=vs.85))</span></span>
</dt> </dl>

 

 
