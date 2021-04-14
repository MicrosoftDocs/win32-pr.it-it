---
title: Tipo semplice HexInt16Type
description: Definisce un tipo esadecimale a 2 byte.
ms.assetid: d33d24e7-d260-49ea-a8ba-187b9b7a3a9c
keywords:
- Log eventi di tipo semplice HexInt16Type
topic_type:
- apiref
api_name:
- HexInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6aaa5021fbc5a7de5c16083c0f7744bc4a154c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478664"
---
# <a name="hexint16type-simple-type"></a><span data-ttu-id="1a854-104">Tipo semplice HexInt16Type</span><span class="sxs-lookup"><span data-stu-id="1a854-104">HexInt16Type Simple Type</span></span>

<span data-ttu-id="1a854-105">Definisce un tipo esadecimale a 2 byte.</span><span class="sxs-lookup"><span data-stu-id="1a854-105">Defines a 2-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt16Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,4}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="1a854-106">Modelli</span><span class="sxs-lookup"><span data-stu-id="1a854-106">Patterns</span></span>

<span data-ttu-id="1a854-107">Il tipo semplice **HexInt16Type** è una **stringa** limitata dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="1a854-107">The **HexInt16Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,4}`

    <span data-ttu-id="1a854-108">Il valore può contenere da uno a quattro caratteri esadecimali, ad esempio 0xA o 0xac7b.</span><span class="sxs-lookup"><span data-stu-id="1a854-108">The value can contain from one to four hexadecimal characters (for example, 0xa or 0xac7b).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a854-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a854-109">Requirements</span></span>



| <span data-ttu-id="1a854-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a854-110">Requirement</span></span> | <span data-ttu-id="1a854-111">Valore</span><span class="sxs-lookup"><span data-stu-id="1a854-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1a854-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a854-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1a854-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a854-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1a854-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a854-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1a854-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1a854-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





