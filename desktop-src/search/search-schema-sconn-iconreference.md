---
description: L' <iconReference> elemento facoltativo specifica un'icona personalizzata per questa posizione. Questo elemento non ha attributi e nessun elemento figlio.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: Elemento iconReference (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c181efe3bb8ac04f08d4fa16016d3468af6f10c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525464"
---
# <a name="iconreference-element-search-connector-schema"></a><span data-ttu-id="7f700-104">Elemento iconReference (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="7f700-104">iconReference Element (Search Connector Schema)</span></span>

<span data-ttu-id="7f700-105">L' <iconReference> elemento facoltativo specifica un'icona personalizzata per questa posizione.</span><span class="sxs-lookup"><span data-stu-id="7f700-105">The optional <iconReference> element specifies a custom icon for this location.</span></span> <span data-ttu-id="7f700-106">Questo elemento non ha attributi e nessun elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="7f700-106">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f700-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f700-107">Syntax</span></span>


```
<!-- iconReference -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="7f700-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7f700-108">Element Information</span></span>



| <span data-ttu-id="7f700-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="7f700-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="7f700-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7f700-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="7f700-111">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="7f700-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="7f700-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f700-112">Remarks</span></span>

<span data-ttu-id="7f700-113">Il formato del riferimento deve essere specificato in un formato appropriato per la funzione [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) : (ad esempio, <dll file name> , <icon index> ).</span><span class="sxs-lookup"><span data-stu-id="7f700-113">The format of the reference must be specified in a form suitable for the [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) function: (for example, <dll file name>,<icon index>).</span></span>

## <a name="example"></a><span data-ttu-id="7f700-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="7f700-114">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 
