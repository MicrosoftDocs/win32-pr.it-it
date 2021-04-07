---
description: La funzione PdhVbCreateCounterPathList Visualizza la finestra di dialogo esplorazione dei contatori delle prestazioni, che consente all'utente di selezionare diversi contatori delle prestazioni. Ogni percorso del contatore selezionato deve quindi essere letto utilizzando la funzione PdhVbGetCounterPathFromList.
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: PdhVbCreateCounterPathList (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbCreateCounterPathList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: bef484846507bf68d8ccfc0ad3ea10a250b83133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881761"
---
# <a name="pdhvbcreatecounterpathlist-function"></a><span data-ttu-id="5fde6-104">PdhVbCreateCounterPathList (funzione)</span><span class="sxs-lookup"><span data-stu-id="5fde6-104">PdhVbCreateCounterPathList function</span></span>

<span data-ttu-id="5fde6-105">La funzione **PdhVbCreateCounterPathList** Visualizza la finestra di dialogo esplorazione dei contatori delle prestazioni, che consente all'utente di selezionare diversi contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5fde6-105">The **PdhVbCreateCounterPathList** function displays the performance counter browsing dialog box, which lets the user select several performance counters.</span></span> <span data-ttu-id="5fde6-106">Ogni percorso del contatore selezionato deve quindi essere letto utilizzando la funzione [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) .</span><span class="sxs-lookup"><span data-stu-id="5fde6-106">Each selected counter path must then be read using the [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5fde6-107">La funzione descritta in questo argomento può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="5fde6-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="5fde6-108">Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5fde6-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="5fde6-109">Funzione PdhVbCreateCounterPathList ( \_ ByVal DetailLevel Long, \_ ByVal CaptionString As String \_ ) Long</span><span class="sxs-lookup"><span data-stu-id="5fde6-109">Function PdhVbCreateCounterPathList( \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="5fde6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fde6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fde6-111">*DetailLevel*</span><span class="sxs-lookup"><span data-stu-id="5fde6-111">*DetailLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="5fde6-112">Tipi di contatori da visualizzare nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="5fde6-112">Types of counters to be displayed in the dialog box.</span></span> <span data-ttu-id="5fde6-113">Usare uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5fde6-113">Use one of the following values.</span></span>



| <span data-ttu-id="5fde6-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5fde6-114">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="5fde6-115">Significato</span><span class="sxs-lookup"><span data-stu-id="5fde6-115">Meaning</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <span data-ttu-id="5fde6-116"><dt>**\_dettaglio prestazioni \_ avanzato**</dt></span><span class="sxs-lookup"><span data-stu-id="5fde6-116"><dt>**PERF\_DETAIL\_ADVANCED**</dt></span></span> </dl> | <span data-ttu-id="5fde6-117">Contatori che l'utente avanzato è in grado di comprendere, oltre ai contatori degli utenti meno esperti.</span><span class="sxs-lookup"><span data-stu-id="5fde6-117">Counters that the advanced user is likely to understand, in addition to the novice-user counters.</span></span><br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <span data-ttu-id="5fde6-118"><dt>**\_esperto Dettagli \_ prestazioni**</dt></span><span class="sxs-lookup"><span data-stu-id="5fde6-118"><dt>**PERF\_DETAIL\_EXPERT**</dt></span></span> </dl>       | <span data-ttu-id="5fde6-119">Contatori che l'utente esperto e lo sviluppatore di software possono conoscere, oltre ai contatori per gli utenti principianti e avanzati.</span><span class="sxs-lookup"><span data-stu-id="5fde6-119">Counters that the expert user and software developer is likely to understand, in addition to the counters for the novice and advanced users.</span></span><br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <span data-ttu-id="5fde6-120"><dt>**dettaglio prestazioni- \_ \_ novizio**</dt></span><span class="sxs-lookup"><span data-stu-id="5fde6-120"><dt>**PERF\_DETAIL\_NOVICE**</dt></span></span> </dl>       | <span data-ttu-id="5fde6-121">Solo i contatori che è probabile che l'utente del novizio possa comprendere.</span><span class="sxs-lookup"><span data-stu-id="5fde6-121">Only counters that the novice user is likely to understand.</span></span><br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <span data-ttu-id="5fde6-122"><dt>**\_ \_ procedura guidata Dettagli prestazioni**</dt></span><span class="sxs-lookup"><span data-stu-id="5fde6-122"><dt>**PERF\_DETAIL\_WIZARD**</dt></span></span> </dl>       | <span data-ttu-id="5fde6-123">Tutti i contatori nel sistema.</span><span class="sxs-lookup"><span data-stu-id="5fde6-123">All counters in the system.</span></span><br/>                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="5fde6-124">*CaptionString*</span><span class="sxs-lookup"><span data-stu-id="5fde6-124">*CaptionString*</span></span> 
</dt> <dd>

<span data-ttu-id="5fde6-125">Variabile di stringa che contiene il testo che verrà visualizzato nella barra del titolo della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="5fde6-125">String variable that contains the text that will be displayed in the caption bar of the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fde6-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fde6-126">Return value</span></span>

<span data-ttu-id="5fde6-127">La funzione restituisce il numero di percorsi del contatore selezionati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="5fde6-127">The function returns the number of counter paths that the user selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fde6-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fde6-128">Requirements</span></span>



| <span data-ttu-id="5fde6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fde6-129">Requirement</span></span> | <span data-ttu-id="5fde6-130">Valore</span><span class="sxs-lookup"><span data-stu-id="5fde6-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5fde6-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fde6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5fde6-132">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5fde6-132">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5fde6-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fde6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5fde6-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5fde6-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5fde6-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="5fde6-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="5fde6-136"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fde6-136"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="5fde6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5fde6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fde6-138"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fde6-138"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fde6-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fde6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fde6-140">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="5fde6-140">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="5fde6-141">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="5fde6-141">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[<span data-ttu-id="5fde6-142">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="5fde6-142">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




