---
description: La funzione PdhVbUpdateLog Function aggiorna la query corrente e scrive nuovi dati nel file di log. Questa funzione chiama PdhUpdateLog.
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: PdhVbUpdateLog (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbUpdateLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c02e533f57481004b0a7de9f779399b20bddc0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312142"
---
# <a name="pdhvbupdatelog-function"></a><span data-ttu-id="badcb-104">PdhVbUpdateLog (funzione)</span><span class="sxs-lookup"><span data-stu-id="badcb-104">PdhVbUpdateLog function</span></span>

<span data-ttu-id="badcb-105">La funzione **PdhVbUpdateLog** Function aggiorna la query corrente e scrive nuovi dati nel file di log.</span><span class="sxs-lookup"><span data-stu-id="badcb-105">The **PdhVbUpdateLog** function function updates the current query and writes new data to the log file.</span></span> <span data-ttu-id="badcb-106">Questa funzione chiama [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).</span><span class="sxs-lookup"><span data-stu-id="badcb-106">This function calls [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="badcb-107">La funzione descritta in questo argomento può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="badcb-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="badcb-108">Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="badcb-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="badcb-109">Funzione PdhVbUpdateLog ( \_ ByVal numero As PDH \_ numero, \_ ByVal szUserString As LPCTSTR \_ )</span><span class="sxs-lookup"><span data-stu-id="badcb-109">Function PdhVbUpdateLog( \_ ByVal hLog As PDH\_HLOG, \_ ByVal szUserString As LPCTSTR \_ )</span></span>

## <a name="parameters"></a><span data-ttu-id="badcb-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="badcb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="badcb-111">*numero* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="badcb-111">*hLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="badcb-112">Handle per il file di log da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="badcb-112">Handle to the log file to be updated.</span></span> <span data-ttu-id="badcb-113">Questo handle viene restituito dalla funzione [**PdhVbOpenLog**](pdhvbopenlog.md) .</span><span class="sxs-lookup"><span data-stu-id="badcb-113">This handle is returned by the [**PdhVbOpenLog**](pdhvbopenlog.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="badcb-114">*szUserString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="badcb-114">*szUserString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="badcb-115">Puntatore a una stringa che specifica i dati da aggiungere al file di log.</span><span class="sxs-lookup"><span data-stu-id="badcb-115">Pointer to a string that specifies the data to be added to the log file.</span></span> <span data-ttu-id="badcb-116">Questa operazione viene in genere utilizzata per i commenti nel file di log.</span><span class="sxs-lookup"><span data-stu-id="badcb-116">This is generally used for comments within the log file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="badcb-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="badcb-117">Return value</span></span>

<span data-ttu-id="badcb-118">Se la funzione ha esito positivo, restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="badcb-118">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="badcb-119">Se la funzione ha esito negativo, il valore restituito è un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di [errore PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="badcb-119">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="badcb-120">Di seguito sono riportati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="badcb-120">The following are possible values.</span></span>



| <span data-ttu-id="badcb-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="badcb-121">Return code</span></span>                                                                                                | <span data-ttu-id="badcb-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="badcb-122">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="badcb-123"><dt>**\_buffer insufficiente PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="badcb-123"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="badcb-124">I dati richiesti sono maggiori del buffer fornito.</span><span class="sxs-lookup"><span data-stu-id="badcb-124">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="badcb-125">Impossibile restituire i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="badcb-125">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="badcb-126"><dt>**\_argomento PDH non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="badcb-126"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="badcb-127">La dimensione di uno o più buffer di stringa non è corretta.</span><span class="sxs-lookup"><span data-stu-id="badcb-127">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="badcb-128"><dt>**\_handle PDH non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="badcb-128"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="badcb-129">L'handle non è un oggetto PDH valido.</span><span class="sxs-lookup"><span data-stu-id="badcb-129">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="badcb-130"><dt>**\_errore di \_ apertura del file di registro PDH \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="badcb-130"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="badcb-131">Impossibile aprire il file di log specificato.</span><span class="sxs-lookup"><span data-stu-id="badcb-131">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="badcb-132"><dt>**il \_ file PDH non è stato \_ \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="badcb-132"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="badcb-133">Impossibile trovare il file specificato.</span><span class="sxs-lookup"><span data-stu-id="badcb-133">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="badcb-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="badcb-134">Remarks</span></span>

<span data-ttu-id="badcb-135">È necessario che sia presente una query attualmente aperta ed è necessario aggiungervi i contatori desiderati prima di chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="badcb-135">There must be a currently opened query, and the desired counters must be added to it before this function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="badcb-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="badcb-136">Requirements</span></span>



| <span data-ttu-id="badcb-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="badcb-137">Requirement</span></span> | <span data-ttu-id="badcb-138">Valore</span><span class="sxs-lookup"><span data-stu-id="badcb-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="badcb-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="badcb-139">Minimum supported client</span></span><br/> | <span data-ttu-id="badcb-140">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="badcb-140">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="badcb-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="badcb-141">Minimum supported server</span></span><br/> | <span data-ttu-id="badcb-142">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="badcb-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="badcb-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="badcb-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="badcb-144"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="badcb-144"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="badcb-145">DLL</span><span class="sxs-lookup"><span data-stu-id="badcb-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="badcb-146"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="badcb-146"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="badcb-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="badcb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="badcb-148">**PdhUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="badcb-148">**PdhUpdateLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[<span data-ttu-id="badcb-149">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="badcb-149">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
</dt> <dt>

[<span data-ttu-id="badcb-150">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="badcb-150">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
</dt> </dl>

 

