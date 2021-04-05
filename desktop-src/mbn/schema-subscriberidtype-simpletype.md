---
description: Definisce un tipo per l'elemento SubscriberID del profilo Mobile Broadband.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: Tipo semplice subscriberIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: c3c776bbd721bbb03b4f5549f87d48248a35206b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049463"
---
# <a name="subscriberidtype-simple-type"></a><span data-ttu-id="710aa-103">Tipo semplice subscriberIdType</span><span class="sxs-lookup"><span data-stu-id="710aa-103">subscriberIdType Simple Type</span></span>

<span data-ttu-id="710aa-104">Il tipo semplice **subscriberIdType** definisce un tipo per l'elemento [**SubscriberID**](schema-subscriberid-mbnprofile-element.md) del profilo Mobile Broadband.</span><span class="sxs-lookup"><span data-stu-id="710aa-104">The **subscriberIdType** simple type defines a type for the [**SubscriberID**](schema-subscriberid-mbnprofile-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="710aa-105">Questo tipo è una raccolta di uno o più caratteri.</span><span class="sxs-lookup"><span data-stu-id="710aa-105">This type is a collection of one or more characters.</span></span>

``` syntax
<xs:simpleType name="subscriberIdType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="710aa-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="710aa-106">Requirements</span></span>



| <span data-ttu-id="710aa-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="710aa-107">Requirement</span></span> | <span data-ttu-id="710aa-108">Valore</span><span class="sxs-lookup"><span data-stu-id="710aa-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="710aa-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="710aa-109">Minimum supported client</span></span><br/> | <span data-ttu-id="710aa-110">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="710aa-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="710aa-111">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="710aa-111">Minimum supported server</span></span><br/> | <span data-ttu-id="710aa-112">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="710aa-112">None supported</span></span><br/>                         |



 

 




