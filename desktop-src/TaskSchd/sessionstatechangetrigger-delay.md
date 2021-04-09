---
title: Proprietà SessionStateChangeTrigger. Delay
description: Per gli script, ottiene o imposta un valore che indica per quanto tempo si verifica un ritardo prima che venga avviata un'attività dopo che è stata rilevata una modifica dello stato della sessione Terminal Server.
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Utilità di pianificazione di proprietà delay
- Utilità di pianificazione di proprietà delay, oggetto SessionStateChangeTrigger
- Utilità di pianificazione oggetto SessionStateChangeTrigger, proprietà delay
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd5afde8ebd2884aee19fbdafb785355b9fedb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119295"
---
# <a name="sessionstatechangetriggerdelay-property"></a><span data-ttu-id="1c5f0-106">Proprietà SessionStateChangeTrigger. Delay</span><span class="sxs-lookup"><span data-stu-id="1c5f0-106">SessionStateChangeTrigger.Delay property</span></span>

<span data-ttu-id="1c5f0-107">Per gli script, ottiene o imposta un valore che indica per quanto tempo si verifica un ritardo prima che venga avviata un'attività dopo che è stata rilevata una modifica dello stato della sessione Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="1c5f0-107">For scripting, gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.</span></span> <span data-ttu-id="1c5f0-108">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="1c5f0-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="1c5f0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c5f0-109">Syntax</span></span>


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="1c5f0-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1c5f0-110">Property value</span></span>

<span data-ttu-id="1c5f0-111">Il ritardo che si verifica prima dell'avvio di un'attività dopo che è stata rilevata una modifica dello stato della sessione Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="1c5f0-111">The delay that takes place before a task is started after a Terminal Server session state change is detected.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c5f0-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c5f0-112">Requirements</span></span>



| <span data-ttu-id="1c5f0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c5f0-113">Requirement</span></span> | <span data-ttu-id="1c5f0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1c5f0-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c5f0-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c5f0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1c5f0-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c5f0-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1c5f0-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c5f0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1c5f0-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1c5f0-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1c5f0-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1c5f0-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="1c5f0-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1c5f0-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1c5f0-121">DLL</span><span class="sxs-lookup"><span data-stu-id="1c5f0-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c5f0-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c5f0-122"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





