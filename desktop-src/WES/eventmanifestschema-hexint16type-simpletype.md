---
title: Tipo semplice UInt16Type
description: Definisce un tipo short senza segno.
ms.assetid: 2200bb14-8f38-43fd-aed3-2a6b3ac33ed5
keywords:
- Log eventi di tipo semplice UInt16Type
topic_type:
- apiref
api_name:
- UInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e687f42a43a12266267a0531ce078e8c6b5d1031
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743231"
---
# <a name="uint16type-simple-type"></a><span data-ttu-id="ccbc2-104">Tipo semplice UInt16Type</span><span class="sxs-lookup"><span data-stu-id="ccbc2-104">UInt16Type Simple Type</span></span>

<span data-ttu-id="ccbc2-105">Definisce un tipo short senza segno.</span><span class="sxs-lookup"><span data-stu-id="ccbc2-105">Defines an unsigned short type.</span></span> <span data-ttu-id="ccbc2-106">Il valore può essere specificato come un Integer a 2 byte o un valore esadecimale compreso nell'intervallo compreso tra 0 e 65.535.</span><span class="sxs-lookup"><span data-stu-id="ccbc2-106">The value can be specified as a 2-byte integer or hexadecimal value in the range from 0 through 65,535.</span></span>

``` syntax
<xs:simpleType name="UInt16Type">
    <xs:union
        memberValues="unsignedShort HexInt16Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="ccbc2-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccbc2-107">Requirements</span></span>



| <span data-ttu-id="ccbc2-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccbc2-108">Requirement</span></span> | <span data-ttu-id="ccbc2-109">Valore</span><span class="sxs-lookup"><span data-stu-id="ccbc2-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ccbc2-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccbc2-110">Minimum supported client</span></span><br/> | <span data-ttu-id="ccbc2-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ccbc2-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ccbc2-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccbc2-112">Minimum supported server</span></span><br/> | <span data-ttu-id="ccbc2-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ccbc2-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





