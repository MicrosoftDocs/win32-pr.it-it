---
description: Definisce i tipi di rete wireless.
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: Tipo semplice networkTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d0acb998c879e718a0e201418610bb0aa6db8c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317112"
---
# <a name="networktypetype-simple-type"></a><span data-ttu-id="4b408-103">Tipo semplice networkTypeType</span><span class="sxs-lookup"><span data-stu-id="4b408-103">networkTypeType Simple Type</span></span>

<span data-ttu-id="4b408-104">Il tipo semplice networkTypeType definisce i tipi di rete wireless.</span><span class="sxs-lookup"><span data-stu-id="4b408-104">The networkTypeType simple type defines the wireless network types.</span></span> <span data-ttu-id="4b408-105">Esistono due tipi di reti: reti di infrastruttura (SSE) e reti ad hoc (IBSS).</span><span class="sxs-lookup"><span data-stu-id="4b408-105">There are two types of networks: infrastructure networks (ESS) and ad-hoc networks (IBSS).</span></span>

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="4b408-106">Valori di enumerazione</span><span class="sxs-lookup"><span data-stu-id="4b408-106">Enumeration values</span></span>

<span data-ttu-id="4b408-107">Il tipo semplice **networkTypeType** definisce i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4b408-107">The **networkTypeType** simple type defines the following values.</span></span>



| <span data-ttu-id="4b408-108">Valore</span><span class="sxs-lookup"><span data-stu-id="4b408-108">Value</span></span> | <span data-ttu-id="4b408-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b408-109">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="4b408-110">IBSS</span><span class="sxs-lookup"><span data-stu-id="4b408-110">IBSS</span></span>  |             |
| <span data-ttu-id="4b408-111">ESS</span><span class="sxs-lookup"><span data-stu-id="4b408-111">ESS</span></span>   |             |



## <a name="requirements"></a><span data-ttu-id="4b408-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b408-112">Requirements</span></span>



| <span data-ttu-id="4b408-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b408-113">Requirement</span></span> | <span data-ttu-id="4b408-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4b408-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4b408-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b408-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4b408-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b408-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4b408-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b408-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4b408-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4b408-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




