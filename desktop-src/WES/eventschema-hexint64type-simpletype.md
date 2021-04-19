---
title: Tipo semplice HexInt64Type (schema di eventi)
description: Definisce un tipo esadecimale a 8 byte. | Tipo semplice HexInt64Type (schema di eventi)
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
keywords:
- Log eventi di tipo semplice HexInt64Type
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e290c2326415664fbbae3feed9628b86452b10c6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321705"
---
# <a name="hexint64type-simple-type-event-schema"></a><span data-ttu-id="f26dc-105">Tipo semplice HexInt64Type (schema di eventi)</span><span class="sxs-lookup"><span data-stu-id="f26dc-105">HexInt64Type Simple Type (Event Schema)</span></span>

<span data-ttu-id="f26dc-106">Definisce un tipo esadecimale a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="f26dc-106">Defines an 8-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt64Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,16}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="f26dc-107">Modelli</span><span class="sxs-lookup"><span data-stu-id="f26dc-107">Patterns</span></span>

<span data-ttu-id="f26dc-108">Il tipo semplice **HexInt64Type** è una **stringa** limitata dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="f26dc-108">The **HexInt64Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,16}`

    <span data-ttu-id="f26dc-109">Il valore può contenere da uno a sedici caratteri esadecimali, ad esempio 0xA o 0xac7bd361004fe190.</span><span class="sxs-lookup"><span data-stu-id="f26dc-109">The value can contain from one to sixteen hexadecimal characters (for example, 0xa or 0xac7bd361004fe190).</span></span>

## <a name="requirements"></a><span data-ttu-id="f26dc-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f26dc-110">Requirements</span></span>



| <span data-ttu-id="f26dc-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f26dc-111">Requirement</span></span> | <span data-ttu-id="f26dc-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f26dc-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f26dc-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f26dc-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f26dc-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f26dc-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f26dc-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f26dc-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f26dc-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f26dc-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





