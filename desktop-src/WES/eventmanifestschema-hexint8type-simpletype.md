---
title: Tipo semplice UInt8Type
description: Definisce un tipo di byte senza segno.
ms.assetid: bda12d06-683f-4183-a84b-2bc3159c4eff
keywords:
- Log eventi di tipo semplice UInt8Type
topic_type:
- apiref
api_name:
- UInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3236d7416cbb199037813a8ae870d4f87718081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301553"
---
# <a name="uint8type-simple-type"></a><span data-ttu-id="3f75b-104">Tipo semplice UInt8Type</span><span class="sxs-lookup"><span data-stu-id="3f75b-104">UInt8Type Simple Type</span></span>

<span data-ttu-id="3f75b-105">Definisce un tipo di byte senza segno.</span><span class="sxs-lookup"><span data-stu-id="3f75b-105">Defines an unsigned byte type.</span></span> <span data-ttu-id="3f75b-106">Il valore può essere specificato come valore integer a 1 byte o esadecimale compreso nell'intervallo compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="3f75b-106">The value can be specified as a 1-byte integer or hexadecimal value in the range from 0 through 255.</span></span>

``` syntax
<xs:simpleType name="UInt8Type">
    <xs:union
        memberValues="unsignedByte HexInt8Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="3f75b-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f75b-107">Requirements</span></span>



| <span data-ttu-id="3f75b-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f75b-108">Requirement</span></span> | <span data-ttu-id="3f75b-109">Valore</span><span class="sxs-lookup"><span data-stu-id="3f75b-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f75b-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f75b-110">Minimum supported client</span></span><br/> | <span data-ttu-id="3f75b-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f75b-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3f75b-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f75b-112">Minimum supported server</span></span><br/> | <span data-ttu-id="3f75b-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f75b-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





