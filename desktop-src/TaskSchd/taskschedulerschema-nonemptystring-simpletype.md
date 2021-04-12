---
title: Tipo semplice nonEmptyStringType
description: Definisce i valori utilizzati per una stringa di testo non vuota.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- Utilità di pianificazione di tipo semplice nonEmptyString
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab9c9fa84c510fc4e67f6f63664a58d6d4093709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400749"
---
# <a name="nonemptystringtype-simple-type"></a><span data-ttu-id="b27db-104">Tipo semplice nonEmptyStringType</span><span class="sxs-lookup"><span data-stu-id="b27db-104">nonEmptyStringType Simple Type</span></span>

<span data-ttu-id="b27db-105">Definisce i valori utilizzati per una stringa di testo non vuota.</span><span class="sxs-lookup"><span data-stu-id="b27db-105">Defines the values used for a non-empty string of text.</span></span>

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="b27db-106">Valori di enumerazione</span><span class="sxs-lookup"><span data-stu-id="b27db-106">Enumeration values</span></span>

<span data-ttu-id="b27db-107">Il tipo semplice **nonEmptyString** definisce il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="b27db-107">The **nonEmptyString** simple type defines the following value.</span></span>



| <span data-ttu-id="b27db-108">Valore</span><span class="sxs-lookup"><span data-stu-id="b27db-108">Value</span></span> | <span data-ttu-id="b27db-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b27db-109">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="b27db-110">1</span><span class="sxs-lookup"><span data-stu-id="b27db-110">1</span></span>     | <span data-ttu-id="b27db-111">La stringa contiene almeno un carattere.</span><span class="sxs-lookup"><span data-stu-id="b27db-111">The string contains at least one character.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b27db-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b27db-112">Requirements</span></span>



| <span data-ttu-id="b27db-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b27db-113">Requirement</span></span> | <span data-ttu-id="b27db-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b27db-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b27db-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b27db-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b27db-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b27db-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b27db-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b27db-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b27db-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b27db-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





