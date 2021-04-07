---
description: La funzione PdhVbGetOneCounterPath Visualizza una finestra di dialogo che consente all'utente di visualizzare i contatori delle prestazioni disponibili e di selezionare un contatore.
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: PdhVbGetOneCounterPath (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetOneCounterPath
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 980665372d49f483e3fb59b7571ec38fa9c2851a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881757"
---
# <a name="pdhvbgetonecounterpath-function"></a><span data-ttu-id="912e5-103">PdhVbGetOneCounterPath (funzione)</span><span class="sxs-lookup"><span data-stu-id="912e5-103">PdhVbGetOneCounterPath function</span></span>

<span data-ttu-id="912e5-104">La funzione **PdhVbGetOneCounterPath** Visualizza una finestra di dialogo che consente all'utente di visualizzare i contatori delle prestazioni disponibili e di selezionare un contatore.</span><span class="sxs-lookup"><span data-stu-id="912e5-104">The **PdhVbGetOneCounterPath** function displays a dialog box that lets the user browse the available performance counters and select one counter.</span></span> <span data-ttu-id="912e5-105">Il contatore selezionato viene restituito nella variabile *PathString* .</span><span class="sxs-lookup"><span data-stu-id="912e5-105">The counter selected is returned in the *PathString* variable.</span></span> <span data-ttu-id="912e5-106">La variabile *PathString* deve essere dimensionata e inizializzata prima che questa funzione venga chiamata e la dimensione dimensione deve essere indicata dalla variabile *PathLength* .</span><span class="sxs-lookup"><span data-stu-id="912e5-106">The *PathString* variable must be dimensioned and initialized before this function is called, and the dimensioned size must be indicated by the *PathLength* variable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="912e5-107">La funzione descritta in questo argomento può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="912e5-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="912e5-108">Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="912e5-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="912e5-109">Funzione PdhVbGetOneCounterPath ( \_ ByVal PathString As String, \_ ByVal PathLength As Long, \_ ByVal DetailLevel Long, \_ ByVal CaptionString As String \_ ) Long</span><span class="sxs-lookup"><span data-stu-id="912e5-109">Function PdhVbGetOneCounterPath( \_ ByVal PathString As String, \_ ByVal PathLength As Long, \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="912e5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="912e5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="912e5-111">*PathString*</span><span class="sxs-lookup"><span data-stu-id="912e5-111">*PathString*</span></span> 
</dt> <dd>

<span data-ttu-id="912e5-112">Variabile di stringa inizializzata utilizzata per ricevere il percorso del contatore selezionato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="912e5-112">Initialized string variable used to receive the counter path selected by the user.</span></span>

</dd> <dt>

<span data-ttu-id="912e5-113">*PathLength*</span><span class="sxs-lookup"><span data-stu-id="912e5-113">*PathLength*</span></span> 
</dt> <dd>

<span data-ttu-id="912e5-114">Lunghezza del PathString inizializzato.</span><span class="sxs-lookup"><span data-stu-id="912e5-114">Length of the initialized PathString.</span></span>

</dd> <dt>

<span data-ttu-id="912e5-115">*DetailLevel*</span><span class="sxs-lookup"><span data-stu-id="912e5-115">*DetailLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="912e5-116">Tipi di contatori da visualizzare nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="912e5-116">Types of counters to be displayed in the dialog box.</span></span> <span data-ttu-id="912e5-117">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="912e5-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="912e5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="912e5-118">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="912e5-119">Significato</span><span class="sxs-lookup"><span data-stu-id="912e5-119">Meaning</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <span data-ttu-id="912e5-120"><dt>**\_dettaglio prestazioni \_ avanzato**</dt></span><span class="sxs-lookup"><span data-stu-id="912e5-120"><dt>**PERF\_DETAIL\_ADVANCED**</dt></span></span> </dl> | <span data-ttu-id="912e5-121">Contatori che l'utente avanzato è in grado di comprendere, oltre ai contatori degli utenti meno esperti.</span><span class="sxs-lookup"><span data-stu-id="912e5-121">Counters that the advanced user is likely to understand, in addition to the novice-user counters.</span></span><br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <span data-ttu-id="912e5-122"><dt>**\_esperto Dettagli \_ prestazioni**</dt></span><span class="sxs-lookup"><span data-stu-id="912e5-122"><dt>**PERF\_DETAIL\_EXPERT**</dt></span></span> </dl>       | <span data-ttu-id="912e5-123">Contatori che l'utente esperto e lo sviluppatore di software possono conoscere, oltre ai contatori per gli utenti principianti e avanzati.</span><span class="sxs-lookup"><span data-stu-id="912e5-123">Counters that the expert user and software developer is likely to understand, in addition to the counters for the novice and advanced users.</span></span><br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <span data-ttu-id="912e5-124"><dt>**dettaglio prestazioni- \_ \_ novizio**</dt></span><span class="sxs-lookup"><span data-stu-id="912e5-124"><dt>**PERF\_DETAIL\_NOVICE**</dt></span></span> </dl>       | <span data-ttu-id="912e5-125">Solo i contatori che è probabile che l'utente del novizio possa comprendere.</span><span class="sxs-lookup"><span data-stu-id="912e5-125">Only counters that the novice user is likely to understand.</span></span><br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <span data-ttu-id="912e5-126"><dt>**\_ \_ procedura guidata Dettagli prestazioni**</dt></span><span class="sxs-lookup"><span data-stu-id="912e5-126"><dt>**PERF\_DETAIL\_WIZARD**</dt></span></span> </dl>       | <span data-ttu-id="912e5-127">Tutti i contatori nel sistema.</span><span class="sxs-lookup"><span data-stu-id="912e5-127">All counters in the system.</span></span><br/>                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="912e5-128">*CaptionString*</span><span class="sxs-lookup"><span data-stu-id="912e5-128">*CaptionString*</span></span> 
</dt> <dd>

<span data-ttu-id="912e5-129">Variabile di stringa che contiene il testo che verrà visualizzato nella barra del titolo della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="912e5-129">String variable that contains the text that will be displayed in the caption bar of the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="912e5-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="912e5-130">Return value</span></span>

<span data-ttu-id="912e5-131">La funzione restituisce il numero di caratteri scritti nel buffer *PathString* .</span><span class="sxs-lookup"><span data-stu-id="912e5-131">The function returns the number of characters written to the *PathString* buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="912e5-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="912e5-132">Requirements</span></span>



| <span data-ttu-id="912e5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="912e5-133">Requirement</span></span> | <span data-ttu-id="912e5-134">Valore</span><span class="sxs-lookup"><span data-stu-id="912e5-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="912e5-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="912e5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="912e5-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="912e5-136">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="912e5-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="912e5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="912e5-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="912e5-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="912e5-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="912e5-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="912e5-140"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="912e5-140"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="912e5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="912e5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="912e5-142"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="912e5-142"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="912e5-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="912e5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="912e5-144">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="912e5-144">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="912e5-145">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="912e5-145">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="912e5-146">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="912e5-146">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




