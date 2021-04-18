---
description: Definisce i valori validi per l'attributo di stile dell'elemento LineLayout.
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: Tipo semplice LineLayoutStyleType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LineLayoutStyleType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 67b07d9de51e16148905768d7a6f268038bb1afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318699"
---
# <a name="linelayoutstyletype-simple-type"></a><span data-ttu-id="87fbd-103">Tipo semplice LineLayoutStyleType</span><span class="sxs-lookup"><span data-stu-id="87fbd-103">LineLayoutStyleType Simple Type</span></span>

<span data-ttu-id="87fbd-104">Definisce i valori validi per l'attributo di **stile** dell' [elemento LineLayout](linelayout-element.md).</span><span class="sxs-lookup"><span data-stu-id="87fbd-104">Defines the valid values for the **Style** attribute of the [LineLayout element](linelayout-element.md).</span></span>

``` syntax
<xs:simpleType name="LineLayoutStyleType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="None|Solid|Dash|Dot|DashDot|DashDotDot|Double"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="87fbd-105">Modelli</span><span class="sxs-lookup"><span data-stu-id="87fbd-105">Patterns</span></span>

<span data-ttu-id="87fbd-106">Il tipo semplice **LineLayoutStyleType** è una stringa limitata dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="87fbd-106">The **LineLayoutStyleType** simple type is a string that is restricted by the following pattern:</span></span>

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a><span data-ttu-id="87fbd-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="87fbd-107">Remarks</span></span>

<span data-ttu-id="87fbd-108">I valori validi per l'attributo di **stile** dell' [elemento LineLayout](linelayout-element.md) sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="87fbd-108">Valid values for the **Style** attribute of the [LineLayout element](linelayout-element.md) are:</span></span>

-   <span data-ttu-id="87fbd-109">nessuno</span><span class="sxs-lookup"><span data-stu-id="87fbd-109">None</span></span>
-   <span data-ttu-id="87fbd-110">Tinta unita</span><span class="sxs-lookup"><span data-stu-id="87fbd-110">Solid</span></span>
-   <span data-ttu-id="87fbd-111">Trattino</span><span class="sxs-lookup"><span data-stu-id="87fbd-111">Dash</span></span>
-   <span data-ttu-id="87fbd-112">Punto</span><span class="sxs-lookup"><span data-stu-id="87fbd-112">Dot</span></span>
-   <span data-ttu-id="87fbd-113">DashDot</span><span class="sxs-lookup"><span data-stu-id="87fbd-113">DashDot</span></span>
-   <span data-ttu-id="87fbd-114">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="87fbd-114">DashDotDot</span></span>
-   <span data-ttu-id="87fbd-115">Double</span><span class="sxs-lookup"><span data-stu-id="87fbd-115">Double</span></span>

## <a name="requirements"></a><span data-ttu-id="87fbd-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87fbd-116">Requirements</span></span>



| <span data-ttu-id="87fbd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="87fbd-117">Requirement</span></span> | <span data-ttu-id="87fbd-118">Valore</span><span class="sxs-lookup"><span data-stu-id="87fbd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="87fbd-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87fbd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="87fbd-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="87fbd-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="87fbd-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87fbd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="87fbd-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="87fbd-122">None supported</span></span><br/>                                     |



 

 




