---
description: L'elemento booleano <supportsAdvancedQuerySyntax> specifica se il provider di ricerca supporta la sintassi di query avanzata. Il valore predefinito è false. Questo elemento è facoltativo e non ha elementi figlio e nessun attributo.
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: Elemento supportsAdvancedQuerySyntax (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d31eb96615c952f703729fd9d22f2e5d27f38b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306075"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a><span data-ttu-id="6bca2-105">Elemento supportsAdvancedQuerySyntax (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="6bca2-105">supportsAdvancedQuerySyntax Element (Search Connector Schema)</span></span>

<span data-ttu-id="6bca2-106">L'elemento booleano <supportsAdvancedQuerySyntax> specifica se il provider di ricerca supporta la [sintassi di query avanzata](-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="6bca2-106">The Boolean <supportsAdvancedQuerySyntax> element specifies whether the search provider supports the [Advanced Query Syntax](-search-3x-advancedquerysyntax.md).</span></span> <span data-ttu-id="6bca2-107">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="6bca2-107">The default is false.</span></span> <span data-ttu-id="6bca2-108">Questo elemento è facoltativo e non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="6bca2-108">This element is optional and has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bca2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6bca2-109">Syntax</span></span>


```
<!-- supportsAdvancedQuerySyntax -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="6bca2-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6bca2-110">Element Information</span></span>



| <span data-ttu-id="6bca2-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="6bca2-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="6bca2-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="6bca2-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="6bca2-113">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="6bca2-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="6bca2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bca2-114">Remarks</span></span>

<span data-ttu-id="6bca2-115">Il valore `true` indica che il provider di ricerca supporta la sintassi di query avanzata inviata nelle query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="6bca2-115">The value `true` indicates that the search provider supports Advanced Query Syntax sent in search queries.</span></span>

## <a name="example"></a><span data-ttu-id="6bca2-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="6bca2-116">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 



