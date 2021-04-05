---
title: Tipo complesso namedValues
description: Definisce una coppia nome-valore in cui il nome è associato al valore.
ms.assetid: 07c512fd-3eab-4238-8d75-83827a958a1e
keywords:
- Utilità di pianificazione di tipo complesso namedValues
topic_type:
- apiref
api_name:
- namedValues
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f18c9fddab58f33ffc724a3e8df7bd65583cb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742162"
---
# <a name="namedvalues-complex-type"></a><span data-ttu-id="7e0c5-104">Tipo complesso namedValues</span><span class="sxs-lookup"><span data-stu-id="7e0c5-104">namedValues Complex Type</span></span>

<span data-ttu-id="7e0c5-105">Definisce una coppia nome-valore in cui il nome è associato al valore.</span><span class="sxs-lookup"><span data-stu-id="7e0c5-105">Defines a name-value pair in which the name is associated with the value.</span></span>

``` syntax
<xs:complexType name="namedValues">
    <xs:sequence>
        <xs:element name="Value"
            type="namedValue"
            minOccurs="1"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7e0c5-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7e0c5-106">Child elements</span></span>



| <span data-ttu-id="7e0c5-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7e0c5-107">Element</span></span>                                                        | <span data-ttu-id="7e0c5-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e0c5-108">Type</span></span>                                                | <span data-ttu-id="7e0c5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e0c5-109">Description</span></span>                                                                         |
|----------------------------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e0c5-110">**Valore**</span><span class="sxs-lookup"><span data-stu-id="7e0c5-110">**Value**</span></span>](taskschedulerschema-value-namedvalues-element.md) | [<span data-ttu-id="7e0c5-111">**namedValue**</span><span class="sxs-lookup"><span data-stu-id="7e0c5-111">**namedValue**</span></span>](schema-namedvalue-complextype.md) | <span data-ttu-id="7e0c5-112">Specifica il valore associato a un nome in una coppia nome-valore.</span><span class="sxs-lookup"><span data-stu-id="7e0c5-112">Specifies the value that is associated with a name in a name-value pair.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7e0c5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e0c5-113">Requirements</span></span>



| <span data-ttu-id="7e0c5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e0c5-114">Requirement</span></span> | <span data-ttu-id="7e0c5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7e0c5-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e0c5-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e0c5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7e0c5-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7e0c5-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7e0c5-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e0c5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7e0c5-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7e0c5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





