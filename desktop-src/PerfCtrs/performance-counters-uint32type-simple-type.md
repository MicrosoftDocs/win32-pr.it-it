---
description: 'Tipo semplice UInt32Type (contatori delle prestazioni): definisce un tipo integer senza segno.'
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Tipo semplice UInt32Type (contatori delle prestazioni)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32f8a4bbf00f569ba98dfc031f62717b1afc8734
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114579"
---
# <a name="uint32type-simple-type-performance-counters"></a><span data-ttu-id="88090-103">Tipo semplice UInt32Type (contatori delle prestazioni)</span><span class="sxs-lookup"><span data-stu-id="88090-103">UInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="88090-104">Definisce un tipo integer senza segno.</span><span class="sxs-lookup"><span data-stu-id="88090-104">Defines an unsigned integer type.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="88090-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="88090-105">Remarks</span></span>

<span data-ttu-id="88090-106">È possibile specificare il valore come intero a 4 byte o valore esadecimale compreso nell'intervallo compreso tra 0 e 4.294.967.295.</span><span class="sxs-lookup"><span data-stu-id="88090-106">You can specify the value as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

## <a name="requirements"></a><span data-ttu-id="88090-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88090-107">Requirements</span></span>



| <span data-ttu-id="88090-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="88090-108">Requirement</span></span> | <span data-ttu-id="88090-109">Valore</span><span class="sxs-lookup"><span data-stu-id="88090-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="88090-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88090-110">Minimum supported client</span></span><br/> | <span data-ttu-id="88090-111">Solo app desktop di Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="88090-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="88090-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88090-112">Minimum supported server</span></span><br/> | <span data-ttu-id="88090-113">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="88090-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




