---
title: Tipo complesso sessionStateChangeTriggerType
description: Definisce gli elementi utilizzati per creare un trigger di attività per la connessione o la disconnessione della console, la connessione remota o disconnessione o le notifiche di blocco o sblocco della workstation.
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- Utilità di pianificazione di tipo complesso sessionStateChangeTriggerType
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8eb3ad02aef3f5bbbc078f8eafa52f3439819cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341302"
---
# <a name="sessionstatechangetriggertype-complex-type"></a><span data-ttu-id="63610-104">Tipo complesso sessionStateChangeTriggerType</span><span class="sxs-lookup"><span data-stu-id="63610-104">sessionStateChangeTriggerType Complex Type</span></span>

<span data-ttu-id="63610-105">Definisce gli elementi utilizzati per creare un trigger di attività per la connessione o la disconnessione della console, la connessione remota o disconnessione o le notifiche di blocco o sblocco della workstation.</span><span class="sxs-lookup"><span data-stu-id="63610-105">Defines the elements used to create a task trigger for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.</span></span>

``` syntax
<xs:complexType name="sessionStateChangeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="StateChange"
                    type="sessionStateChangeType"
                    minOccurs="1"
                    maxOccurs="1"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="63610-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="63610-106">Child elements</span></span>



| <span data-ttu-id="63610-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="63610-107">Element</span></span>                                                                                      | <span data-ttu-id="63610-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="63610-108">Type</span></span>                                                                                    | <span data-ttu-id="63610-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63610-109">Description</span></span>                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63610-110">**Ritardo**</span><span class="sxs-lookup"><span data-stu-id="63610-110">**Delay**</span></span>](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | <span data-ttu-id="63610-111">duration</span><span class="sxs-lookup"><span data-stu-id="63610-111">duration</span></span>                                                                                | <span data-ttu-id="63610-112">Specifica un valore che indica la lunghezza del ritardo prima che un'attività venga avviata quando viene rilevata una modifica dello stato della sessione Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="63610-112">Specifies a value that indicates the length of the delay before a task is started when a Terminal Server session state change is detected.</span></span><br/> |
| [<span data-ttu-id="63610-113">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="63610-113">**StateChange**</span></span>](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [<span data-ttu-id="63610-114">**sessionStateChangeType**</span><span class="sxs-lookup"><span data-stu-id="63610-114">**sessionStateChangeType**</span></span>](taskschedulerschema-sessionstatechangetype-simpletype.md) | <span data-ttu-id="63610-115">Specifica il tipo di modifica della sessione di Terminal Server che attiverà l'avvio di un'attività.</span><span class="sxs-lookup"><span data-stu-id="63610-115">Specifies the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                     |
| [<span data-ttu-id="63610-116">**UserId**</span><span class="sxs-lookup"><span data-stu-id="63610-116">**UserId**</span></span>](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [<span data-ttu-id="63610-117">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="63610-117">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                 | <span data-ttu-id="63610-118">Specifica l'utente per la sessione di Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="63610-118">Specifies the user for the Terminal Server session.</span></span> <span data-ttu-id="63610-119">Quando viene rilevata una modifica dello stato della sessione per questo utente, viene avviata un'attività.</span><span class="sxs-lookup"><span data-stu-id="63610-119">When a session state change is detected for this user, a task is started.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="63610-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63610-120">Requirements</span></span>



| <span data-ttu-id="63610-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="63610-121">Requirement</span></span> | <span data-ttu-id="63610-122">Valore</span><span class="sxs-lookup"><span data-stu-id="63610-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="63610-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63610-123">Minimum supported client</span></span><br/> | <span data-ttu-id="63610-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63610-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="63610-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63610-125">Minimum supported server</span></span><br/> | <span data-ttu-id="63610-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63610-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





