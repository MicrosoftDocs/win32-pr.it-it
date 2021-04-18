---
description: Definisce un tipo esadecimale a 4 byte.
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: Tipo semplice HexInt32Type (contatori delle prestazioni)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d2392f2240ca9ca61525b27993e16bcab979a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312121"
---
# <a name="hexint32type-simple-type-performance-counters"></a><span data-ttu-id="fb5e7-103">Tipo semplice HexInt32Type (contatori delle prestazioni)</span><span class="sxs-lookup"><span data-stu-id="fb5e7-103">HexInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="fb5e7-104">Definisce un tipo esadecimale a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="fb5e7-104">Defines a 4-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="fb5e7-105">Modelli</span><span class="sxs-lookup"><span data-stu-id="fb5e7-105">Patterns</span></span>

<span data-ttu-id="fb5e7-106">Il tipo semplice **HexInt32Type** è **xs: String** limitato dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="fb5e7-106">The **HexInt32Type** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="fb5e7-107">Il valore può contenere da uno a otto caratteri esadecimali, ad esempio 0xA o 0xac7bd361.</span><span class="sxs-lookup"><span data-stu-id="fb5e7-107">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb5e7-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb5e7-108">Requirements</span></span>



| <span data-ttu-id="fb5e7-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb5e7-109">Requirement</span></span> | <span data-ttu-id="fb5e7-110">Valore</span><span class="sxs-lookup"><span data-stu-id="fb5e7-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fb5e7-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb5e7-111">Minimum supported client</span></span><br/> | <span data-ttu-id="fb5e7-112">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb5e7-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fb5e7-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb5e7-113">Minimum supported server</span></span><br/> | <span data-ttu-id="fb5e7-114">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fb5e7-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




