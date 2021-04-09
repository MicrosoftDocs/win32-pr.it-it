---
title: Elemento Delay (sessionStateChangeTriggerType)
description: Contiene un valore che indica la lunghezza del ritardo per l'ora di inizio di un'attività, quando viene rilevata una modifica dello stato della sessione Terminal Server.
ms.assetid: 7fb87c4c-0b69-4c5b-b038-d61fb7c4ab9a
keywords:
- Utilità di pianificazione elemento Delay
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03f230465f2e2b49ce83f1af358dfa1f84f21433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121570"
---
# <a name="delay-sessionstatechangetriggertype-element"></a><span data-ttu-id="12c1b-104">Elemento Delay (sessionStateChangeTriggerType)</span><span class="sxs-lookup"><span data-stu-id="12c1b-104">Delay (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="12c1b-105">Contiene un valore che indica la lunghezza del ritardo per l'ora di inizio di un'attività, quando viene rilevata una modifica dello stato della sessione Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="12c1b-105">Contains a value that indicates the delay length for a task start time, when a Terminal Server session state change is detected.</span></span> <span data-ttu-id="12c1b-106">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="12c1b-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="12c1b-107">Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="12c1b-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="12c1b-108">L'elemento **delay** viene definito dal tipo complesso [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="12c1b-108">The **Delay** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="12c1b-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="12c1b-109">Parent element</span></span>



| <span data-ttu-id="12c1b-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="12c1b-110">Element</span></span>                       | <span data-ttu-id="12c1b-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="12c1b-111">Derived from</span></span>                                                                                           | <span data-ttu-id="12c1b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12c1b-112">Description</span></span>                                                                                      |
|-------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12c1b-113">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="12c1b-113">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="12c1b-114">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="12c1b-114">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="12c1b-115">Specifica un trigger che avvia un'attività quando una sessione di Terminal Server modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="12c1b-115">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="12c1b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="12c1b-116">Remarks</span></span>

<span data-ttu-id="12c1b-117">Per lo sviluppo di script, il ritardo del trigger di modifica dello stato della sessione viene specificato tramite la proprietà [**SessionStateChangeTrigger. Delay**](sessionstatechangetrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="12c1b-117">For scripting development, the session state change trigger delay is specified using the [**SessionStateChangeTrigger.Delay**](sessionstatechangetrigger-delay.md) property.</span></span>

<span data-ttu-id="12c1b-118">Per lo sviluppo in C++, il ritardo del trigger di modifica dello stato della sessione viene specificato utilizzando la [**Proprietà Delay di ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).</span><span class="sxs-lookup"><span data-stu-id="12c1b-118">For C++ development, the session state change trigger delay is specified using the [**Delay property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="12c1b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12c1b-119">Requirements</span></span>



| <span data-ttu-id="12c1b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="12c1b-120">Requirement</span></span> | <span data-ttu-id="12c1b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="12c1b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="12c1b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12c1b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="12c1b-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12c1b-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="12c1b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12c1b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="12c1b-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="12c1b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





