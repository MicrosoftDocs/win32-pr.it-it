---
description: Identifica l'APN o la stringa di connessione da utilizzare per stabilire una connessione dati.
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: Elemento AccessString (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 8cf0d37b8a1870011ae6ae3ea6febf22a98cdeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307548"
---
# <a name="accessstring-contexttype-element"></a><span data-ttu-id="84c05-103">Elemento AccessString (contextType)</span><span class="sxs-lookup"><span data-stu-id="84c05-103">AccessString (contextType) Element</span></span>

<span data-ttu-id="84c05-104">L'elemento **AccessString (ContextType)** identifica l'APN o la stringa di connessione da usare per stabilire una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="84c05-104">The **AccessString (contextType)** element identifies the APN or dial string to be used to establish a data connection.</span></span>

<span data-ttu-id="84c05-105">Questo elemento può avere una lunghezza massima di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="84c05-105">This element can have a maximum length of 100 characters.</span></span>

<span data-ttu-id="84c05-106">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84c05-106">This element is optional.</span></span>

``` syntax
<xs:element name="AccessString">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="84c05-107">L'elemento **AccessString** è definito dal tipo complesso [**contextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="84c05-107">The **AccessString** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="84c05-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84c05-108">Requirements</span></span>



| <span data-ttu-id="84c05-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="84c05-109">Requirement</span></span> | <span data-ttu-id="84c05-110">Valore</span><span class="sxs-lookup"><span data-stu-id="84c05-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="84c05-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84c05-111">Minimum supported client</span></span><br/> | <span data-ttu-id="84c05-112">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="84c05-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="84c05-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84c05-113">Minimum supported server</span></span><br/> | <span data-ttu-id="84c05-114">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="84c05-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="84c05-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84c05-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="84c05-116">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="84c05-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="84c05-117">**contextType**</span><span class="sxs-lookup"><span data-stu-id="84c05-117">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="84c05-118">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="84c05-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="84c05-119">**Contesto (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="84c05-119">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




