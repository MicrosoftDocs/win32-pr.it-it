---
description: L'elemento booleano <isSearchOnlyItem> specifica se il provider di ricerca supporta la modalità browse oltre alla modalità di ricerca. Questo elemento è facoltativo e non ha elementi figlio e nessun attributo.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: Elemento isSearchOnlyItem (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded7b62cde5cf813603d5cc87c41fe2c443b42d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525453"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a><span data-ttu-id="c786e-104">Elemento isSearchOnlyItem (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="c786e-104">isSearchOnlyItem Element (Search Connector Schema)</span></span>

<span data-ttu-id="c786e-105">L'elemento booleano <isSearchOnlyItem> specifica se il provider di ricerca supporta la modalità browse oltre alla modalità di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c786e-105">The Boolean <isSearchOnlyItem> element specifies whether the search provider supports browse mode in addition to search mode.</span></span> <span data-ttu-id="c786e-106">Questo elemento è facoltativo e non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="c786e-106">This element is optional and has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c786e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c786e-107">Syntax</span></span>


```
<!-- isSearchOnlyItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="c786e-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c786e-108">Element Information</span></span>



| <span data-ttu-id="c786e-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="c786e-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="c786e-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c786e-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="c786e-111">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="c786e-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="c786e-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="c786e-112">Remarks</span></span>

<span data-ttu-id="c786e-113">Il valore `true` indica che la posizione del connettore di ricerca non può essere esplorata dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="c786e-113">The value `true` indicates that the search connector location cannot be browsed by users.</span></span> <span data-ttu-id="c786e-114">Il valore `false` indica che gli utenti possono esplorare il percorso del connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c786e-114">The value `false` indicates that users can browse the search connector location.</span></span>

## <a name="example"></a><span data-ttu-id="c786e-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="c786e-115">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 



