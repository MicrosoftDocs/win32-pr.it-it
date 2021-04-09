---
title: Tipo semplice HexInt32Type (schema di eventi)
description: Definisce un tipo esadecimale a 4 byte. | Tipo semplice HexInt32Type (schema di eventi)
ms.assetid: f4b5226d-2a5e-4756-b4c5-30cfbf13568e
keywords:
- Log eventi di tipo semplice HexInt32Type
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c9bd7a11d0e648cc451ec837f0f8711ca334d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969124"
---
# <a name="hexint32type-simple-type-event-schema"></a><span data-ttu-id="8e491-105">Tipo semplice HexInt32Type (schema di eventi)</span><span class="sxs-lookup"><span data-stu-id="8e491-105">HexInt32Type Simple Type (Event Schema)</span></span>

<span data-ttu-id="8e491-106">Definisce un tipo esadecimale a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="8e491-106">Defines a 4-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="8e491-107">Modelli</span><span class="sxs-lookup"><span data-stu-id="8e491-107">Patterns</span></span>

<span data-ttu-id="8e491-108">Il tipo semplice **HexInt32Type** è una **stringa** limitata dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="8e491-108">The **HexInt32Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="8e491-109">Il valore può contenere da uno a otto caratteri esadecimali, ad esempio 0xA o 0xac7bd361.</span><span class="sxs-lookup"><span data-stu-id="8e491-109">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e491-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e491-110">Requirements</span></span>



| <span data-ttu-id="8e491-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e491-111">Requirement</span></span> | <span data-ttu-id="8e491-112">Valore</span><span class="sxs-lookup"><span data-stu-id="8e491-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8e491-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e491-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8e491-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e491-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8e491-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e491-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8e491-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8e491-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





