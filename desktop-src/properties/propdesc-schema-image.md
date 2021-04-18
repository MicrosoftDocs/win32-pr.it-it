---
description: .
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: Elemento Image (schema della descrizione della proprietà)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb519d5f8104d114734e1f12676f213312e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310122"
---
# <a name="image"></a><span data-ttu-id="46ee8-103">image</span><span class="sxs-lookup"><span data-stu-id="46ee8-103">image</span></span>

<span data-ttu-id="46ee8-104">Deve essere presente un solo elemento [Image]() per ogni elemento padre.</span><span class="sxs-lookup"><span data-stu-id="46ee8-104">There should be only one [image]() element for each parent element.</span></span>

## <a name="syntax"></a><span data-ttu-id="46ee8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46ee8-105">Syntax</span></span>


```
<!-- image -->
<xs:element name="image">
    <xs:complexType>
        <xs:attribute name="res" use="required">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:maxLength value="260"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="46ee8-106">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="46ee8-106">Element Information</span></span>



| <span data-ttu-id="46ee8-107">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="46ee8-107">Parent Elements</span></span>                                                                  | <span data-ttu-id="46ee8-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="46ee8-108">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="46ee8-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="46ee8-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span></span> | <span data-ttu-id="46ee8-110">nessuno</span><span class="sxs-lookup"><span data-stu-id="46ee8-110">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="46ee8-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="46ee8-111">Attributes</span></span>



| <span data-ttu-id="46ee8-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="46ee8-112">Attribute</span></span> | <span data-ttu-id="46ee8-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46ee8-113">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="46ee8-114">res</span><span class="sxs-lookup"><span data-stu-id="46ee8-114">res</span></span>       | <span data-ttu-id="46ee8-115">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="46ee8-115">Public.</span></span> <span data-ttu-id="46ee8-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="46ee8-116">Required.</span></span> |



 

 

 
