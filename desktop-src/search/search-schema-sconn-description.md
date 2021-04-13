---
description: Il parametro facoltativo <description> l'elemento specifica una descrizione per questo connettore di ricerca. Questo elemento non ha elementi figlio e nessun attributo.
ms.assetid: 0e9d806c-7dfd-4e7f-8843-15a4e22f317f
title: Elemento Description (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d82fd6ad3ae45c4a8c3700c4822387a81880d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342921"
---
# <a name="description-element-search-connector-schema"></a><span data-ttu-id="36019-105">Elemento Description (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="36019-105">description Element (Search Connector Schema)</span></span>

<span data-ttu-id="36019-106">Il parametro facoltativo</span><span class="sxs-lookup"><span data-stu-id="36019-106">The optional</span></span> <description> <span data-ttu-id="36019-107">l'elemento specifica una descrizione per questo connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="36019-107">element specifies a description for this search connector.</span></span> <span data-ttu-id="36019-108">Questo elemento non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="36019-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="36019-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36019-109">Syntax</span></span>


```
<!-- description -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="description" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="36019-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="36019-110">Element Information</span></span>



| <span data-ttu-id="36019-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="36019-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="36019-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="36019-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="36019-113">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="36019-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="36019-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="36019-114">Remarks</span></span>

<span data-ttu-id="36019-115">La descrizione deve essere intuitiva perché può essere usata nelle descrizioni comandi.</span><span class="sxs-lookup"><span data-stu-id="36019-115">The description should be user-friendly as it may be used in tooltips.</span></span>

## <a name="example"></a><span data-ttu-id="36019-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="36019-116">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <description>Search AdventureWorks.com</description>
    ...
</searchConnectionDescription>
```



 

 



