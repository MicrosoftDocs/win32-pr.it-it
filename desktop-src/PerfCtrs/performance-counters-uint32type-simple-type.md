---
description: Definisce un tipo di Unsigned Integer.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Tipo semplice UInt32Type (contatori delle prestazioni)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c32901167bcf181e5400ddb1d3b91ed7383965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312106"
---
# <a name="uint32type-simple-type-performance-counters"></a><span data-ttu-id="42e73-103">Tipo semplice UInt32Type (contatori delle prestazioni)</span><span class="sxs-lookup"><span data-stu-id="42e73-103">UInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="42e73-104">Definisce un tipo di Unsigned Integer.</span><span class="sxs-lookup"><span data-stu-id="42e73-104">Defines an unsigned integer type.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="42e73-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="42e73-105">Remarks</span></span>

<span data-ttu-id="42e73-106">È possibile specificare il valore come valore integer a 4 byte o esadecimale nell'intervallo compreso tra 0 e 4.294.967.295.</span><span class="sxs-lookup"><span data-stu-id="42e73-106">You can specify the value as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

## <a name="requirements"></a><span data-ttu-id="42e73-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42e73-107">Requirements</span></span>



| <span data-ttu-id="42e73-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="42e73-108">Requirement</span></span> | <span data-ttu-id="42e73-109">Valore</span><span class="sxs-lookup"><span data-stu-id="42e73-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="42e73-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42e73-110">Minimum supported client</span></span><br/> | <span data-ttu-id="42e73-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42e73-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="42e73-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42e73-112">Minimum supported server</span></span><br/> | <span data-ttu-id="42e73-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="42e73-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




