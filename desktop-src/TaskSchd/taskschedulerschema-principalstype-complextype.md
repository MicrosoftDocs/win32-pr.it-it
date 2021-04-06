---
title: Tipo complesso principalsType
description: Definisce l'elemento figlio per l'elemento principals.
ms.assetid: a501534b-eb0f-480f-a2c9-d2015262a9a7
keywords:
- Utilità di pianificazione di tipo complesso principalsType
topic_type:
- apiref
api_name:
- principalsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56cd26a4dff31ce86b218e5a4a2662d678327625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963857"
---
# <a name="principalstype-complex-type"></a><span data-ttu-id="8c700-104">Tipo complesso principalsType</span><span class="sxs-lookup"><span data-stu-id="8c700-104">principalsType Complex Type</span></span>

<span data-ttu-id="8c700-105">Definisce l'elemento figlio per l'elemento [**Principals**](taskschedulerschema-principals-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8c700-105">Defines the child element for the [**Principals**](taskschedulerschema-principals-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="principalsType">
    <xs:sequence>
        <xs:element name="Principal"
            type="principalType"
            maxOccurs="1"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8c700-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8c700-106">Child elements</span></span>



| <span data-ttu-id="8c700-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="8c700-107">Element</span></span>                                                                  | <span data-ttu-id="8c700-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c700-108">Type</span></span>                                                                   | <span data-ttu-id="8c700-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c700-109">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="8c700-110">**Principale**</span><span class="sxs-lookup"><span data-stu-id="8c700-110">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="8c700-111">**principalType**</span><span class="sxs-lookup"><span data-stu-id="8c700-111">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="8c700-112">Specifica le credenziali di sicurezza per un'entità.</span><span class="sxs-lookup"><span data-stu-id="8c700-112">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8c700-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c700-113">Requirements</span></span>



| <span data-ttu-id="8c700-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c700-114">Requirement</span></span> | <span data-ttu-id="8c700-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8c700-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8c700-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c700-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8c700-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c700-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8c700-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c700-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8c700-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c700-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





