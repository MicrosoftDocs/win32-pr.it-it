---
description: Definisce il tipo che contiene i valori validi per l'attributo del tipo per l'elemento Margin.
ms.assetid: 5448ead5-0249-4cc7-9f2a-d2181e2af734
title: Tipo semplice MarginTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MarginTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4e8a09e98611fabc54a029c9cac9cb37dfc1373f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233548"
---
# <a name="margintypetype-simple-type"></a><span data-ttu-id="f698d-103">Tipo semplice MarginTypeType</span><span class="sxs-lookup"><span data-stu-id="f698d-103">MarginTypeType Simple Type</span></span>

<span data-ttu-id="f698d-104">Definisce il tipo che contiene i valori validi per l'attributo del **tipo** per l' [elemento Margin](margin-element.md).</span><span class="sxs-lookup"><span data-stu-id="f698d-104">Defines the type that contains valid values for the **Type** attribute for the [Margin element](margin-element.md).</span></span>

``` syntax
<xs:simpleType name="MarginTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Left|Right"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="f698d-105">Modelli</span><span class="sxs-lookup"><span data-stu-id="f698d-105">Patterns</span></span>

<span data-ttu-id="f698d-106">Il tipo semplice **MarginTypeType** è una **stringa** limitata dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="f698d-106">The **MarginTypeType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `Left|Right`

## <a name="remarks"></a><span data-ttu-id="f698d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="f698d-107">Remarks</span></span>

<span data-ttu-id="f698d-108">I valori validi per l'attributo **Type** per l' [elemento Margin](margin-element.md) sono "left" e "Right".</span><span class="sxs-lookup"><span data-stu-id="f698d-108">The valid values for the **Type** attribute for the [Margin element](margin-element.md) are "Left" and "Right".</span></span>

## <a name="requirements"></a><span data-ttu-id="f698d-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f698d-109">Requirements</span></span>



| <span data-ttu-id="f698d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f698d-110">Requirement</span></span> | <span data-ttu-id="f698d-111">Valore</span><span class="sxs-lookup"><span data-stu-id="f698d-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f698d-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f698d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f698d-113">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f698d-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f698d-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f698d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f698d-115">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f698d-115">None supported</span></span><br/>                                     |



 

 




