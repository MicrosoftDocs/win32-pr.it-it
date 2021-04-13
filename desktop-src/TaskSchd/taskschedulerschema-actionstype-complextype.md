---
title: Tipo complesso actionsType
description: Definisce gli elementi figlio e l'attributo per l'elemento Actions.
ms.assetid: 01577b65-4bfa-4b9f-b9b9-6b2b0dbd582a
keywords:
- Utilità di pianificazione di tipo complesso actionsType
topic_type:
- apiref
api_name:
- actionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ebc2cf95803f6e4a02d4ec00d7aa767aa4e8a8a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400797"
---
# <a name="actionstype-complex-type"></a><span data-ttu-id="41a0f-104">Tipo complesso actionsType</span><span class="sxs-lookup"><span data-stu-id="41a0f-104">actionsType Complex Type</span></span>

<span data-ttu-id="41a0f-105">Definisce gli elementi figlio e l'attributo per l'elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="41a0f-105">Defines the child elements and attribute for the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="actionsType">
    <xs:sequence>
        <xs:group
            maxOccurs="32"
            ref="actionGroup"
         />
    </xs:sequence>
    <xs:attribute name="Context"
        type="IDREF"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="41a0f-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="41a0f-106">Attributes</span></span>



| <span data-ttu-id="41a0f-107">Nome</span><span class="sxs-lookup"><span data-stu-id="41a0f-107">Name</span></span>    | <span data-ttu-id="41a0f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="41a0f-108">Type</span></span>  | <span data-ttu-id="41a0f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41a0f-109">Description</span></span>                                                                                          |
|---------|-------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41a0f-110">Context</span><span class="sxs-lookup"><span data-stu-id="41a0f-110">Context</span></span> | <span data-ttu-id="41a0f-111">IDREF</span><span class="sxs-lookup"><span data-stu-id="41a0f-111">IDREF</span></span> | <span data-ttu-id="41a0f-112">Identificatore dell'entità utilizzata che rappresenta il contesto di sicurezza per le azioni dell'attività.</span><span class="sxs-lookup"><span data-stu-id="41a0f-112">Principal identifier of the used who is the security context for the actions of the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="41a0f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41a0f-113">Requirements</span></span>



| <span data-ttu-id="41a0f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="41a0f-114">Requirement</span></span> | <span data-ttu-id="41a0f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="41a0f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="41a0f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41a0f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="41a0f-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41a0f-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="41a0f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41a0f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="41a0f-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41a0f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41a0f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41a0f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41a0f-121">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="41a0f-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="41a0f-122">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="41a0f-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





