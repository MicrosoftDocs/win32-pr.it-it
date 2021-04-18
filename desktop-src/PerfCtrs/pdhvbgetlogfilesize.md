---
description: La funzione PdhVbGetLogFileSize restituisce le dimensioni del file di log specificato. Questa funzione chiama PdhGetLogFileSize.
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: PdhVbGetLogFileSize (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetLogFileSize
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 0b9f490477704086bd9aa8c53dd32456d486471e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312148"
---
# <a name="pdhvbgetlogfilesize-function"></a><span data-ttu-id="2503b-104">PdhVbGetLogFileSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="2503b-104">PdhVbGetLogFileSize function</span></span>

<span data-ttu-id="2503b-105">La funzione **PdhVbGetLogFileSize** restituisce le dimensioni del file di log specificato.</span><span class="sxs-lookup"><span data-stu-id="2503b-105">The **PdhVbGetLogFileSize** function returns the size of the specified log file.</span></span> <span data-ttu-id="2503b-106">Questa funzione chiama [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).</span><span class="sxs-lookup"><span data-stu-id="2503b-106">This function calls [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2503b-107">La funzione descritta in questo argomento può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="2503b-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="2503b-108">Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="2503b-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="2503b-109">Funzione PdhVbGetLogFileSize ( \_ ByVal numero As PDH \_ numero, \_ ByRef llSize Long \_ ) As DWORD</span><span class="sxs-lookup"><span data-stu-id="2503b-109">Function PdhVbGetLogFileSize( \_ ByVal hLog As PDH\_HLOG, \_ ByRef llSize As LONG \_ ) As DWORD</span></span>

## <a name="parameters"></a><span data-ttu-id="2503b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2503b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2503b-111">*numero* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2503b-111">*hLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2503b-112">Handle per il file di log.</span><span class="sxs-lookup"><span data-stu-id="2503b-112">Handle to the log file.</span></span> <span data-ttu-id="2503b-113">Questo handle viene restituito dalla funzione [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) .</span><span class="sxs-lookup"><span data-stu-id="2503b-113">This handle is returned by the [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) function.</span></span>

</dd> <dt>

<span data-ttu-id="2503b-114">*llSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2503b-114">*llSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2503b-115">Puntatore a una variabile che riceve le dimensioni, in byte, del file di log.</span><span class="sxs-lookup"><span data-stu-id="2503b-115">Pointer to a variable that receives the size of the log file, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2503b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2503b-116">Return value</span></span>

<span data-ttu-id="2503b-117">Se la funzione ha esito positivo, restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="2503b-117">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="2503b-118">Se la funzione ha esito negativo, il valore restituito è un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di [errore PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2503b-118">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="2503b-119">Di seguito sono riportati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="2503b-119">The following are possible values.</span></span>



| <span data-ttu-id="2503b-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2503b-120">Return code</span></span>                                                                                                | <span data-ttu-id="2503b-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2503b-121">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2503b-122"><dt>**\_buffer insufficiente PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2503b-122"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="2503b-123">I dati richiesti sono maggiori del buffer fornito.</span><span class="sxs-lookup"><span data-stu-id="2503b-123">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="2503b-124">Impossibile restituire i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="2503b-124">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="2503b-125"><dt>**\_argomento PDH non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2503b-125"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="2503b-126">La dimensione di uno o più buffer di stringa non è corretta.</span><span class="sxs-lookup"><span data-stu-id="2503b-126">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="2503b-127"><dt>**\_handle PDH non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2503b-127"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="2503b-128">L'handle non è un oggetto PDH valido.</span><span class="sxs-lookup"><span data-stu-id="2503b-128">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="2503b-129"><dt>**\_errore di \_ apertura del file di registro PDH \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2503b-129"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="2503b-130">Impossibile aprire il file di log specificato.</span><span class="sxs-lookup"><span data-stu-id="2503b-130">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="2503b-131"><dt>**il \_ file PDH non è stato \_ \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="2503b-131"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="2503b-132">Impossibile trovare il file specificato.</span><span class="sxs-lookup"><span data-stu-id="2503b-132">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="requirements"></a><span data-ttu-id="2503b-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2503b-133">Requirements</span></span>



| <span data-ttu-id="2503b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2503b-134">Requirement</span></span> | <span data-ttu-id="2503b-135">Valore</span><span class="sxs-lookup"><span data-stu-id="2503b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2503b-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2503b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2503b-137">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2503b-137">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2503b-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2503b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2503b-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2503b-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2503b-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="2503b-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="2503b-141"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2503b-141"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="2503b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2503b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2503b-143"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2503b-143"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2503b-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2503b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2503b-145">**PdhGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="2503b-145">**PdhGetLogFileSize**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[<span data-ttu-id="2503b-146">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="2503b-146">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
</dt> <dt>

[<span data-ttu-id="2503b-147">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="2503b-147">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)
</dt> </dl>

 

