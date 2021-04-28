---
description: image
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: Elemento image (schema di descrizione proprietà)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24ecb1b88b8b724ce299a81281f926972180743
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104989"
---
# <a name="image"></a><span data-ttu-id="5f929-103">image</span><span class="sxs-lookup"><span data-stu-id="5f929-103">image</span></span>

<span data-ttu-id="5f929-104">Deve essere presente un solo [elemento image]() per ogni elemento padre.</span><span class="sxs-lookup"><span data-stu-id="5f929-104">There should be only one [image]() element for each parent element.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f929-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f929-105">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="5f929-106">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5f929-106">Element Information</span></span>



| <span data-ttu-id="5f929-107">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="5f929-107">Parent Elements</span></span>                                                                  | <span data-ttu-id="5f929-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5f929-108">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="5f929-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="5f929-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span></span> | <span data-ttu-id="5f929-110">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5f929-110">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="5f929-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="5f929-111">Attributes</span></span>



| <span data-ttu-id="5f929-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="5f929-112">Attribute</span></span> | <span data-ttu-id="5f929-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f929-113">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="5f929-114">res</span><span class="sxs-lookup"><span data-stu-id="5f929-114">res</span></span>       | <span data-ttu-id="5f929-115">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="5f929-115">Public.</span></span> <span data-ttu-id="5f929-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5f929-116">Required.</span></span> |



 

 

 
