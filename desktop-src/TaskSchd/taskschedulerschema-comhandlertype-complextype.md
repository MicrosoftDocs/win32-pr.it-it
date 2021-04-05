---
title: Tipo complesso comHandlerType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento comhandler.
ms.assetid: 688e79f3-8b7e-4892-8119-b0a457ce9c7f
keywords:
- Utilità di pianificazione di tipo complesso comHandlerType
topic_type:
- apiref
api_name:
- comHandlerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d36a92651fc46c0a1950ecff00fa59fe56e1d758
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048152"
---
# <a name="comhandlertype-complex-type"></a><span data-ttu-id="5f473-104">Tipo complesso comHandlerType</span><span class="sxs-lookup"><span data-stu-id="5f473-104">comHandlerType Complex Type</span></span>

<span data-ttu-id="5f473-105">Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**Comhandler**](taskschedulerschema-comhandler-actiongroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5f473-105">Defines the child elements and sequencing information for the [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="comHandlerType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="ClassId"
                    type="guidType"
                 />
                <xs:element name="Data"
                    type="dataType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5f473-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5f473-106">Child elements</span></span>



| <span data-ttu-id="5f473-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="5f473-107">Element</span></span>                                                               | <span data-ttu-id="5f473-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f473-108">Type</span></span>                                                         | <span data-ttu-id="5f473-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f473-109">Description</span></span>                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="5f473-110">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="5f473-110">**ClassId**</span></span>](taskschedulerschema-classid-comhandlertype-element.md) | [<span data-ttu-id="5f473-111">**guidType**</span><span class="sxs-lookup"><span data-stu-id="5f473-111">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md)  | <span data-ttu-id="5f473-112">Specifica l'identificatore della classe del gestore.</span><span class="sxs-lookup"><span data-stu-id="5f473-112">Specifies the identifier of the handler class.</span></span><br/>          |
| [<span data-ttu-id="5f473-113">**Data**</span><span class="sxs-lookup"><span data-stu-id="5f473-113">**Data**</span></span>](taskschedulerschema-data-comhandlertype-element.md)       | [<span data-ttu-id="5f473-114">**dataType**</span><span class="sxs-lookup"><span data-stu-id="5f473-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md) | <span data-ttu-id="5f473-115">Specifica i dati aggiuntivi associati al gestore.</span><span class="sxs-lookup"><span data-stu-id="5f473-115">Specifies additional data associated with the handler.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="5f473-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f473-116">Requirements</span></span>



| <span data-ttu-id="5f473-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f473-117">Requirement</span></span> | <span data-ttu-id="5f473-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5f473-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5f473-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f473-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5f473-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f473-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5f473-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f473-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5f473-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5f473-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f473-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f473-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f473-124">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5f473-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="5f473-125">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5f473-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





