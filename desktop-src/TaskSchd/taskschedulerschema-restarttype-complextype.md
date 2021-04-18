---
title: Tipo complesso restartType
description: Definisce gli elementi figlio e le informazioni sulla sequenza per l'elemento RestartOnFailure.
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- Utilità di pianificazione di tipo complesso restartType
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f83dcac376fcdd8d2059649350502111f5a732f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519126"
---
# <a name="restarttype-complex-type"></a><span data-ttu-id="1d88b-104">Tipo complesso restartType</span><span class="sxs-lookup"><span data-stu-id="1d88b-104">restartType Complex Type</span></span>

<span data-ttu-id="1d88b-105">Definisce gli elementi figlio e le informazioni sulla sequenza per l'elemento [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1d88b-105">Defines the child elements and sequence information for the [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="restartType">
    <xs:all>
        <xs:element name="Interval">
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                    <xs:maxInclusive
                        value="P31D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Count">
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1d88b-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1d88b-106">Child elements</span></span>



| <span data-ttu-id="1d88b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="1d88b-107">Element</span></span>                                                              | <span data-ttu-id="1d88b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d88b-108">Type</span></span> | <span data-ttu-id="1d88b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d88b-109">Description</span></span>                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [<span data-ttu-id="1d88b-110">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="1d88b-110">**Count**</span></span>](taskschedulerschema-count-restarttype-element.md)       |      | <span data-ttu-id="1d88b-111">Numero di tentativi di riavvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="1d88b-111">Number of attempts to restart the task.</span></span><br/> |
| [<span data-ttu-id="1d88b-112">**Interval**</span><span class="sxs-lookup"><span data-stu-id="1d88b-112">**Interval**</span></span>](taskschedulerschema-interval-restarttype-element.md) |      | <span data-ttu-id="1d88b-113">Per quanto tempo provare ad avviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="1d88b-113">How long to try to start the task.</span></span><br/>      |



## <a name="requirements"></a><span data-ttu-id="1d88b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d88b-114">Requirements</span></span>



| <span data-ttu-id="1d88b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d88b-115">Requirement</span></span> | <span data-ttu-id="1d88b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1d88b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1d88b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d88b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1d88b-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d88b-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1d88b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d88b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1d88b-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1d88b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d88b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d88b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d88b-122">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="1d88b-122">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="1d88b-123">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="1d88b-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





