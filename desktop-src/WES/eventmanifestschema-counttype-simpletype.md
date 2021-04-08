---
title: Tipo semplice CountType
description: Definisce un tipo di conteggio utilizzato per specificare il numero di elementi in una matrice.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- Log eventi di tipo semplice CountType
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f91b19df4182f5cff305de0429a308d0c5db234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743839"
---
# <a name="counttype-simple-type"></a><span data-ttu-id="b077e-104">Tipo semplice CountType</span><span class="sxs-lookup"><span data-stu-id="b077e-104">CountType Simple Type</span></span>

<span data-ttu-id="b077e-105">Definisce un tipo di conteggio utilizzato per specificare il numero di elementi in una matrice.</span><span class="sxs-lookup"><span data-stu-id="b077e-105">Defines a count type that is used to specify the number of elements in an array.</span></span> <span data-ttu-id="b077e-106">Il valore può essere specificato come valore xs: unsignedShort o come stringa che fa riferimento al nome del nodo dell'elemento dati che contiene il valore short unsiged.</span><span class="sxs-lookup"><span data-stu-id="b077e-106">The value can be specified as an xs:unsignedShort value or as a string that references the name of data item node that contains the unsiged short value.</span></span>

``` syntax
<xs:simpleType name="CountType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="b077e-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b077e-107">Requirements</span></span>



| <span data-ttu-id="b077e-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="b077e-108">Requirement</span></span> | <span data-ttu-id="b077e-109">Valore</span><span class="sxs-lookup"><span data-stu-id="b077e-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b077e-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b077e-110">Minimum supported client</span></span><br/> | <span data-ttu-id="b077e-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b077e-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b077e-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b077e-112">Minimum supported server</span></span><br/> | <span data-ttu-id="b077e-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b077e-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





