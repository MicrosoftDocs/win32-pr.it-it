---
title: Proprietà TimeTrigger. RandomDelay
description: Per gli script, ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger. | Proprietà TimeTrigger. RandomDelay
ms.assetid: ee55dd85-9696-4872-8670-f919fca7481d
keywords:
- Utilità di pianificazione proprietà RandomDelay
- Utilità di pianificazione proprietà RandomDelay, oggetto TimeTrigger
- Oggetto TimeTrigger Utilità di pianificazione, proprietà RandomDelay
topic_type:
- apiref
api_name:
- TimeTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39c4acf4f38670332e723ac0824276695919cb1d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321508"
---
# <a name="timetriggerrandomdelay-property"></a><span data-ttu-id="eca82-107">Proprietà TimeTrigger. RandomDelay</span><span class="sxs-lookup"><span data-stu-id="eca82-107">TimeTrigger.RandomDelay property</span></span>

<span data-ttu-id="eca82-108">Per gli script, ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="eca82-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca82-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eca82-109">Syntax</span></span>


```VB
TimeTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="eca82-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="eca82-110">Property value</span></span>

<span data-ttu-id="eca82-111">Tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="eca82-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="eca82-112">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="eca82-112">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="eca82-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eca82-113">Requirements</span></span>



| <span data-ttu-id="eca82-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eca82-114">Requirement</span></span> | <span data-ttu-id="eca82-115">Valore</span><span class="sxs-lookup"><span data-stu-id="eca82-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eca82-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eca82-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eca82-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eca82-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="eca82-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eca82-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eca82-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eca82-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eca82-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="eca82-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="eca82-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eca82-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eca82-122">DLL</span><span class="sxs-lookup"><span data-stu-id="eca82-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eca82-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eca82-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





