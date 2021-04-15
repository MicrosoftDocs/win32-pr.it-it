---
title: Tipo complesso execType
description: Definisce gli elementi figlio e le informazioni di sequenziazione dell'elemento Exec (actionGroup).
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- Utilità di pianificazione di tipo complesso execType
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f6186c15e8bbe059abaa6cc33580fca45286cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475652"
---
# <a name="exectype-complex-type"></a><span data-ttu-id="bee4b-104">Tipo complesso execType</span><span class="sxs-lookup"><span data-stu-id="bee4b-104">execType Complex Type</span></span>

<span data-ttu-id="bee4b-105">Definisce gli elementi figlio e le informazioni di sequenziazione dell'elemento [**Exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bee4b-105">Defines the child elements and sequencing information of the [**Exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="execType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Command"
                    type="pathType"
                 />
                <xs:element name="Arguments"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="WorkingDirectory"
                    type="pathType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="bee4b-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="bee4b-106">Child elements</span></span>



| <span data-ttu-id="bee4b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="bee4b-107">Element</span></span>                                                                           | <span data-ttu-id="bee4b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="bee4b-108">Type</span></span>                                                        | <span data-ttu-id="bee4b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bee4b-109">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bee4b-110">**Argomenti**</span><span class="sxs-lookup"><span data-stu-id="bee4b-110">**Arguments**</span></span>](taskschedulerschema-arguments-exectype-element.md)               | <span data-ttu-id="bee4b-111">**string**</span><span class="sxs-lookup"><span data-stu-id="bee4b-111">**string**</span></span>                                                  | <span data-ttu-id="bee4b-112">Specifica gli argomenti associati all'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="bee4b-112">Specifies the arguments associated with the command-line operation.</span></span> <br/>                              |
| [<span data-ttu-id="bee4b-113">**Comando**</span><span class="sxs-lookup"><span data-stu-id="bee4b-113">**Command**</span></span>](taskschedulerschema-command-exectype-element.md)                   | [<span data-ttu-id="bee4b-114">**pathType**</span><span class="sxs-lookup"><span data-stu-id="bee4b-114">**pathType**</span></span>](taskschedulerschema-pathtype-simpletype.md) | <span data-ttu-id="bee4b-115">Specifica il file eseguibile o il documento da eseguire.</span><span class="sxs-lookup"><span data-stu-id="bee4b-115">Specifies the executable file or document to be run.</span></span><br/>                                              |
| [<span data-ttu-id="bee4b-116">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="bee4b-116">**WorkingDirectory**</span></span>](taskschedulerschema-workingdirectory-exectype-element.md) | [<span data-ttu-id="bee4b-117">**pathType**</span><span class="sxs-lookup"><span data-stu-id="bee4b-117">**pathType**</span></span>](taskschedulerschema-pathtype-simpletype.md) | <span data-ttu-id="bee4b-118">Specifica la directory in cui si trova il file eseguibile o i file utilizzati dall'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="bee4b-118">Specifies the directory where either the executable or those files used by the executable exists.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bee4b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bee4b-119">Requirements</span></span>



| <span data-ttu-id="bee4b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bee4b-120">Requirement</span></span> | <span data-ttu-id="bee4b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bee4b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bee4b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bee4b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bee4b-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bee4b-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bee4b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bee4b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bee4b-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bee4b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bee4b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bee4b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bee4b-127">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="bee4b-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="bee4b-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="bee4b-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





