---
description: Definisce un tipo stringa per il profilo a banda larga mobile.
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: tipo semplice nameType (Mobile Broadband)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: d8c6032e17eaf2d067dc23030a7a6279bd41eafa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307537"
---
# <a name="nametype-simple-type-mobile-broadband"></a><span data-ttu-id="5a903-103">tipo semplice nameType (Mobile Broadband)</span><span class="sxs-lookup"><span data-stu-id="5a903-103">nameType simple type (Mobile Broadband)</span></span>

<span data-ttu-id="5a903-104">Il tipo semplice **nameType** definisce un tipo stringa per il profilo Mobile Broadband.</span><span class="sxs-lookup"><span data-stu-id="5a903-104">The **nameType** simple type defines a string type for the Mobile Broadband profile.</span></span> <span data-ttu-id="5a903-105">Questa stringa ha una lunghezza compresa tra almeno un carattere e una lunghezza massima di 255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5a903-105">This string is at least one character long and at most 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="5a903-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a903-106">Requirements</span></span>



| <span data-ttu-id="5a903-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a903-107">Requirement</span></span> | <span data-ttu-id="5a903-108">Valore</span><span class="sxs-lookup"><span data-stu-id="5a903-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="5a903-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a903-109">Minimum supported client</span></span><br/> | <span data-ttu-id="5a903-110">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5a903-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="5a903-111">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a903-111">Minimum supported server</span></span><br/> | <span data-ttu-id="5a903-112">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5a903-112">None supported</span></span><br/>                         |



 

 




