---
title: Tipo semplice HexInt8Type
description: Definisce un tipo esadecimale a 1 byte.
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- Log eventi di tipo semplice HexInt8Type
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68e56340ee535531fb6711dcf01a72d92665cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479204"
---
# <a name="hexint8type-simple-type"></a><span data-ttu-id="81d53-104">Tipo semplice HexInt8Type</span><span class="sxs-lookup"><span data-stu-id="81d53-104">HexInt8Type Simple Type</span></span>

<span data-ttu-id="81d53-105">Definisce un tipo esadecimale a 1 byte.</span><span class="sxs-lookup"><span data-stu-id="81d53-105">Defines a 1-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt8Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,2}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="81d53-106">Modelli</span><span class="sxs-lookup"><span data-stu-id="81d53-106">Patterns</span></span>

<span data-ttu-id="81d53-107">Il tipo semplice **HexInt8Type** è una [stringa](/dotnet/api/system.string) limitata dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="81d53-107">The **HexInt8Type** simple type is a [string](/dotnet/api/system.string) that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,2}`

    <span data-ttu-id="81d53-108">Il valore può contenere da uno a due caratteri esadecimali, ad esempio 0xA o 0xAC.</span><span class="sxs-lookup"><span data-stu-id="81d53-108">The value can contain from one to two hexadecimal characters (for example, 0xa or 0xac).</span></span>

## <a name="requirements"></a><span data-ttu-id="81d53-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81d53-109">Requirements</span></span>



| <span data-ttu-id="81d53-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="81d53-110">Requirement</span></span> | <span data-ttu-id="81d53-111">Valore</span><span class="sxs-lookup"><span data-stu-id="81d53-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="81d53-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81d53-112">Minimum supported client</span></span><br/> | <span data-ttu-id="81d53-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81d53-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="81d53-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81d53-114">Minimum supported server</span></span><br/> | <span data-ttu-id="81d53-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="81d53-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

