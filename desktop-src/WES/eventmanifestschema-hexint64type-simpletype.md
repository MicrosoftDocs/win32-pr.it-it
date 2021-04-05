---
title: Tipo semplice UInt64Type (schema EventManifest)
description: Definisce un tipo long senza segno.
ms.assetid: 6f69dbde-8292-4f8e-bf49-3ef41ea7315e
keywords:
- Log eventi di tipo semplice UInt64Type
topic_type:
- apiref
api_name:
- UInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b375a8e452760f9e59bae9cae8449889483d9b4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048318"
---
# <a name="uint64type-simple-type"></a><span data-ttu-id="ac9bd-104">Tipo semplice UInt64Type</span><span class="sxs-lookup"><span data-stu-id="ac9bd-104">UInt64Type Simple Type</span></span>

<span data-ttu-id="ac9bd-105">Definisce un tipo long senza segno.</span><span class="sxs-lookup"><span data-stu-id="ac9bd-105">Defines an unsigned long type.</span></span> <span data-ttu-id="ac9bd-106">Il valore può essere specificato come un Integer a 8 byte o un valore esadecimale compreso nell'intervallo compreso tra 0 e 18.446.744.073.709.551.615.</span><span class="sxs-lookup"><span data-stu-id="ac9bd-106">The value can be specified as an 8-byte integer or hexadecimal value in the range from 0 through 18,446,744,073,709,551,615.</span></span>

``` syntax
<xs:simpleType name="UInt64Type">
    <xs:union
        memberValues="unsignedLong HexInt64Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="ac9bd-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac9bd-107">Requirements</span></span>



| <span data-ttu-id="ac9bd-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac9bd-108">Requirement</span></span> | <span data-ttu-id="ac9bd-109">Valore</span><span class="sxs-lookup"><span data-stu-id="ac9bd-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ac9bd-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac9bd-110">Minimum supported client</span></span><br/> | <span data-ttu-id="ac9bd-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac9bd-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ac9bd-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac9bd-112">Minimum supported server</span></span><br/> | <span data-ttu-id="ac9bd-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ac9bd-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





