---
description: L' <dateCreated> elemento facoltativo identifica la data e l'ora in cui è stato creato il connettore di ricerca usando lo standard ISO 8601. Non ha elementi figlio e nessun attributo.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: Elemento dateCreated (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6017c0555d464a49192c4fe8cb7e347bbab0e367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750343"
---
# <a name="datecreated-element-search-connector-schema"></a><span data-ttu-id="e59f5-104">Elemento dateCreated (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="e59f5-104">dateCreated Element (Search Connector Schema)</span></span>

<span data-ttu-id="e59f5-105">L' <dateCreated> elemento facoltativo identifica la data e l'ora in cui è stato creato il connettore di ricerca usando lo standard ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="e59f5-105">The optional <dateCreated> element identifies the date and the time when this search connector was created, using the ISO 8601 standard.</span></span> <span data-ttu-id="e59f5-106">Non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="e59f5-106">It has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e59f5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e59f5-107">Syntax</span></span>


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="e59f5-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e59f5-108">Element Information</span></span>



| <span data-ttu-id="e59f5-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="e59f5-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="e59f5-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e59f5-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="e59f5-111">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="e59f5-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="e59f5-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e59f5-112">Remarks</span></span>

<span data-ttu-id="e59f5-113">Il formato del valore di questo elemento segue lo standard ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="e59f5-113">The format of the value of this element follows the ISO 8601 standard.</span></span> <span data-ttu-id="e59f5-114">Un uso comune è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="e59f5-114">A common use would be either of the following:</span></span>

-   <span data-ttu-id="e59f5-115">\[Aaaa \] - \[ mm \] - \[ gg \] T \[ HH \] : \[ mm \] : \[ SS \] ± \[ HH \] : \[ mm \] ("1981-04-05T14:30:30-05:00")</span><span class="sxs-lookup"><span data-stu-id="e59f5-115">\[YYYY\]-\[MM\]-\[DD\]T\[hh\]:\[mm\]:\[ss\]±\[hh\]:\[mm\] ("1981-04-05T14:30:30-05:00")</span></span>
-   <span data-ttu-id="e59f5-116">\[AAAA \] \[ mm \] \[ gg \] T \[ HH \] \[ mm \] \[ SS \] Z ("19810405T193030Z")</span><span class="sxs-lookup"><span data-stu-id="e59f5-116">\[YYYY\]\[MM\]\[DD\]T\[hh\]\[mm\]\[ss\]Z ("19810405T193030Z")</span></span>

## <a name="example"></a><span data-ttu-id="e59f5-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="e59f5-117">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 



