---
title: Tipo semplice UInt32Type (registro eventi di Windows)
description: Definisce un tipo di Unsigned Integer.
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- Log eventi di tipo semplice UInt32Type
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2a24326197c72b08032f5144fea1a69fbe68089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964170"
---
# <a name="uint32type-simple-type-windows-event-log"></a><span data-ttu-id="966f5-104">Tipo semplice UInt32Type (registro eventi di Windows)</span><span class="sxs-lookup"><span data-stu-id="966f5-104">UInt32Type Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="966f5-105">Definisce un tipo di Unsigned Integer.</span><span class="sxs-lookup"><span data-stu-id="966f5-105">Defines an unsigned integer type.</span></span> <span data-ttu-id="966f5-106">Il valore può essere specificato come un Integer a 4 byte o un valore esadecimale compreso nell'intervallo compreso tra 0 e 4.294.967.295.</span><span class="sxs-lookup"><span data-stu-id="966f5-106">The value can be specified as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="966f5-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="966f5-107">Requirements</span></span>



| <span data-ttu-id="966f5-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="966f5-108">Requirement</span></span> | <span data-ttu-id="966f5-109">Valore</span><span class="sxs-lookup"><span data-stu-id="966f5-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="966f5-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="966f5-110">Minimum supported client</span></span><br/> | <span data-ttu-id="966f5-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="966f5-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="966f5-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="966f5-112">Minimum supported server</span></span><br/> | <span data-ttu-id="966f5-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="966f5-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





