---
title: WeeklyTrigger.RandomDelay - proprietà
description: Per lo scripting, ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger. | WeeklyTrigger.RandomDelay - proprietà
ms.assetid: 711b188d-b283-4c99-b43d-644f39a31cdc
keywords:
- Proprietà RandomDelay Utilità di pianificazione
- Proprietà RandomDelay Utilità di pianificazione, oggetto WeeklyTrigger
- Proprietà WeeklyTrigger Utilità di pianificazione , RandomDelay
topic_type:
- apiref
api_name:
- WeeklyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2b320b0def6f8e9cb0dabff9ff04bdfea3d858e
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734156"
---
# <a name="weeklytriggerrandomdelay-property"></a><span data-ttu-id="1fa00-107">WeeklyTrigger.RandomDelay - proprietà</span><span class="sxs-lookup"><span data-stu-id="1fa00-107">WeeklyTrigger.RandomDelay property</span></span>

<span data-ttu-id="1fa00-108">Per lo scripting, ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="1fa00-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa00-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1fa00-109">Syntax</span></span>


```VB
WeeklyTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="1fa00-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1fa00-110">Property value</span></span>

<span data-ttu-id="1fa00-111">Tempo di ritardo aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="1fa00-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="1fa00-112">Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, P2DT5S è un ritardo di 2 giorni e 5 secondi).</span><span class="sxs-lookup"><span data-stu-id="1fa00-112">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa00-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fa00-113">Requirements</span></span>



| <span data-ttu-id="1fa00-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fa00-114">Requirement</span></span> | <span data-ttu-id="1fa00-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1fa00-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa00-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fa00-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1fa00-117">Solo app desktop di Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="1fa00-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1fa00-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fa00-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1fa00-119">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1fa00-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1fa00-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1fa00-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="1fa00-121"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1fa00-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1fa00-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1fa00-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fa00-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fa00-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





