---
title: Tipo semplice UInt32Type (registro eventi di Windows)
description: 'Tipo semplice UInt32Type (registro eventi di Windows): definisce un tipo integer senza segno.'
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- EventLog di tipo semplice UInt32Type
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 631bb3e8424db8a5d781aaa43df6096730aaa4d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090569"
---
# <a name="uint32type-simple-type-windows-event-log"></a><span data-ttu-id="95aab-104">Tipo semplice UInt32Type (registro eventi di Windows)</span><span class="sxs-lookup"><span data-stu-id="95aab-104">UInt32Type Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="95aab-105">Definisce un tipo integer senza segno.</span><span class="sxs-lookup"><span data-stu-id="95aab-105">Defines an unsigned integer type.</span></span> <span data-ttu-id="95aab-106">Il valore può essere specificato come intero a 4 byte o valore esadecimale compreso nell'intervallo compreso tra 0 e 4.294.967.295.</span><span class="sxs-lookup"><span data-stu-id="95aab-106">The value can be specified as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="95aab-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95aab-107">Requirements</span></span>



| <span data-ttu-id="95aab-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="95aab-108">Requirement</span></span> | <span data-ttu-id="95aab-109">Valore</span><span class="sxs-lookup"><span data-stu-id="95aab-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="95aab-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95aab-110">Minimum supported client</span></span><br/> | <span data-ttu-id="95aab-111">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="95aab-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="95aab-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95aab-112">Minimum supported server</span></span><br/> | <span data-ttu-id="95aab-113">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="95aab-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





