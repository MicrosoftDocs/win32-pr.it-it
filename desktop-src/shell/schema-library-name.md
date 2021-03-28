---
description: L' <name> elemento specifica il nome della libreria. Questo elemento è obbligatorio e non dispone di attributi o elementi figlio.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Elemento Name (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d38baa32587ee04c62c8c3086d5353e8eed9e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995176"
---
# <a name="name-element-library-schema"></a><span data-ttu-id="91003-104">Elemento Name (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="91003-104">name Element (Library Schema)</span></span>

<span data-ttu-id="91003-105">L' <name> elemento specifica il nome della libreria.</span><span class="sxs-lookup"><span data-stu-id="91003-105">The <name> element specifies the name of this library.</span></span> <span data-ttu-id="91003-106">Questo elemento è obbligatorio e non dispone di attributi o elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="91003-106">This element is required and has no attributes or child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="91003-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91003-107">Syntax</span></span>

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a><span data-ttu-id="91003-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="91003-108">Element Information</span></span>



| <span data-ttu-id="91003-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="91003-109">Parent Element</span></span>                                                               | <span data-ttu-id="91003-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="91003-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="91003-111">Elemento libraryDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="91003-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="91003-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="91003-112">Remarks</span></span>

<span data-ttu-id="91003-113">Il nome è il nome descrittivo della libreria visualizzato in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="91003-113">The name is the friendly library name that is displayed in Windows Explorer.</span></span> <span data-ttu-id="91003-114">Il nome può essere specificato in un <dllname> <index> formato, come nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="91003-114">The name can be specified in a <dllname>,<index> format, as in the following example.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a><span data-ttu-id="91003-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91003-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91003-116">Elemento libraryDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="91003-116">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="91003-117">Cerca nello schema di descrizione del connettore</span><span class="sxs-lookup"><span data-stu-id="91003-117">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
