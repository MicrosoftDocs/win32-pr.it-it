---
description: L' <author> elemento facoltativo specifica l'autore della libreria. Questo elemento non ha elementi figlio e nessun attributo.
ms.assetid: c91042d5-9564-463a-9104-97b927027fc9
title: Elemento Author (Schema connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a2facbf4e3fa743b4dbe56a1c83eb57509c067
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306092"
---
# <a name="author-element-search-connector-schema"></a><span data-ttu-id="7f642-104">Elemento Author (Schema connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="7f642-104">author Element (Search Connector Schema)</span></span>

<span data-ttu-id="7f642-105">L' <author> elemento facoltativo specifica l'autore della libreria.</span><span class="sxs-lookup"><span data-stu-id="7f642-105">The optional <author> element specifies the author of this library.</span></span> <span data-ttu-id="7f642-106">Questo elemento non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="7f642-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f642-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f642-107">Syntax</span></span>


```
<!-- author -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="author" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="7f642-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7f642-108">Element Information</span></span>



| <span data-ttu-id="7f642-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="7f642-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="7f642-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7f642-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="7f642-111">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="7f642-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a><span data-ttu-id="7f642-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="7f642-112">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <author>Joe Smith</author>
    ...
</searchConnectionDescription>
```



 

 



