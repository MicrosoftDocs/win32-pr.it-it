---
description: L'elemento booleano facoltativo <isIndexed> specifica se il percorso descritto dal connettore di ricerca è indicizzato (in locale o in remoto usando Windows Search 4 o versione successiva).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Elemento SetIndex (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f658f6b932f6241b7af84e763d564ca0a8f1b5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128495"
---
# <a name="isindexed-element-search-connector-schema"></a><span data-ttu-id="41f7b-103">Elemento SetIndex (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="41f7b-103">isIndexed Element (Search Connector Schema)</span></span>

<span data-ttu-id="41f7b-104">L'elemento booleano facoltativo <isIndexed> specifica se il percorso descritto dal connettore di ricerca è indicizzato (in locale o in remoto usando Windows Search 4 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="41f7b-104">The optional Boolean <isIndexed> element specifies whether the location described by the search connector is indexed (either locally or remotely using Windows Search 4 or higher).</span></span> <span data-ttu-id="41f7b-105">Il valore predefinito è true per le cartelle locali.</span><span class="sxs-lookup"><span data-stu-id="41f7b-105">The default value is true for local folders.</span></span> <span data-ttu-id="41f7b-106">Questo elemento non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="41f7b-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="41f7b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41f7b-107">Syntax</span></span>


```
<!-- isIndexed -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isIndexed" type="xsIboolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="41f7b-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="41f7b-108">Element Information</span></span>



| <span data-ttu-id="41f7b-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="41f7b-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="41f7b-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="41f7b-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="41f7b-111">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="41f7b-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a><span data-ttu-id="41f7b-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="41f7b-112">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 



