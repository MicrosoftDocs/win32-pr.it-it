---
title: Tipo semplice runLevelType
description: Definisce i valori possibili per l'elemento RunLevel (principalType).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- Utilità di pianificazione di tipo semplice runLevelType
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d037dceeb3e6e4957cc96a17a2ac511a03a94b94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302220"
---
# <a name="runleveltype-simple-type"></a><span data-ttu-id="6c891-104">Tipo semplice runLevelType</span><span class="sxs-lookup"><span data-stu-id="6c891-104">runLevelType Simple Type</span></span>

<span data-ttu-id="6c891-105">Definisce i valori possibili per l'elemento [**runlevel (PrincipalType)**](taskschedulerschema-runlevel-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6c891-105">Defines the possible values for the [**RunLevel (principalType)**](taskschedulerschema-runlevel-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="runLevelType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="LeastPrivilege"
         />
        <xs:enumeration
            value="HighestAvailable"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="6c891-106">Valori di enumerazione</span><span class="sxs-lookup"><span data-stu-id="6c891-106">Enumeration values</span></span>

<span data-ttu-id="6c891-107">Il tipo semplice **runLevelType** definisce i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6c891-107">The **runLevelType** simple type defines the following values.</span></span>



| <span data-ttu-id="6c891-108">Valore</span><span class="sxs-lookup"><span data-stu-id="6c891-108">Value</span></span>            | <span data-ttu-id="6c891-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c891-109">Description</span></span>                                               |
|------------------|-----------------------------------------------------------|
| <span data-ttu-id="6c891-110">LeastPrivilege</span><span class="sxs-lookup"><span data-stu-id="6c891-110">LeastPrivilege</span></span>   | <span data-ttu-id="6c891-111">Le attività vengono eseguite con i privilegi minimi (LUA).</span><span class="sxs-lookup"><span data-stu-id="6c891-111">Tasks are run with the least privileges (LUA).</span></span><br/> |
| <span data-ttu-id="6c891-112">HighestAvailable</span><span class="sxs-lookup"><span data-stu-id="6c891-112">HighestAvailable</span></span> | <span data-ttu-id="6c891-113">Le attività vengono eseguite con i privilegi più elevati.</span><span class="sxs-lookup"><span data-stu-id="6c891-113">Tasks are run with the highest privileges.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="6c891-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c891-114">Requirements</span></span>



| <span data-ttu-id="6c891-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c891-115">Requirement</span></span> | <span data-ttu-id="6c891-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6c891-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c891-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c891-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6c891-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c891-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6c891-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c891-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6c891-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6c891-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





