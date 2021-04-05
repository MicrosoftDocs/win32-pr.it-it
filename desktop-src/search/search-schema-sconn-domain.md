---
description: L' <domain> elemento facoltativo specifica l'URL del servizio di ricerca utilizzato da questo connettore di ricerca. Viene visualizzata nel riquadro dei dettagli. Questo elemento non ha elementi figlio e nessun attributo.
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: Elemento Domain (Schema connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b57819cf485bccbe63e7560f3fcb92811d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878790"
---
# <a name="domain-element-search-connector-schema"></a><span data-ttu-id="442cc-105">Elemento Domain (Schema connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="442cc-105">domain Element (Search Connector Schema)</span></span>

<span data-ttu-id="442cc-106">L' <domain> elemento facoltativo specifica l'URL del servizio di ricerca utilizzato da questo connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="442cc-106">The optional <domain> element specifies the URL of the search service used by this search connector.</span></span> <span data-ttu-id="442cc-107">Viene visualizzata nel riquadro dei dettagli.</span><span class="sxs-lookup"><span data-stu-id="442cc-107">It is displayed in the details pane.</span></span> <span data-ttu-id="442cc-108">Questo elemento non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="442cc-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="442cc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="442cc-109">Syntax</span></span>


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="442cc-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="442cc-110">Element Information</span></span>



| <span data-ttu-id="442cc-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="442cc-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="442cc-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="442cc-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="442cc-113">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="442cc-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="442cc-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="442cc-114">Remarks</span></span>

<span data-ttu-id="442cc-115">L'URL deve essere il dominio di primo livello per il provider di ricerca.</span><span class="sxs-lookup"><span data-stu-id="442cc-115">The URL should be the top-level domain for the search provider.</span></span> <span data-ttu-id="442cc-116">Ad esempio: https://www.example.com.</span><span class="sxs-lookup"><span data-stu-id="442cc-116">For example, https://www.example.com.</span></span>

## <a name="example"></a><span data-ttu-id="442cc-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="442cc-117">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 



