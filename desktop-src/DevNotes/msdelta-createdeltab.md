---
description: Crea un delta tra l'origine e la destinazione (forniti come buffer) e restituisce il Delta di output come buffer allocato da MSDelta.
title: CreateDeltaB (funzione)
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: a2142f26499514c24967e5334d782c2dee559cd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324693"
---
# <a name="createdeltab-function"></a><span data-ttu-id="0b262-103">CreateDeltaB (funzione)</span><span class="sxs-lookup"><span data-stu-id="0b262-103">CreateDeltaB function</span></span>

<span data-ttu-id="0b262-104">Crea un delta tra l'origine e la destinazione (forniti come buffer) e restituisce il Delta di output come buffer allocato da MSDelta.</span><span class="sxs-lookup"><span data-stu-id="0b262-104">Creates a delta between the source and target (provided as buffers) and returns the output delta as an MSDelta-allocated buffer.</span></span>

> [!NOTE]
> <span data-ttu-id="0b262-105">È necessario chiamare [DeltaFree](msdelta-deltafree.md) per liberare il buffer di output dopo che questa funzione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0b262-105">You must call [DeltaFree](msdelta-deltafree.md) to free the output buffer after this function has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b262-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b262-106">Syntax</span></span>

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a><span data-ttu-id="0b262-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b262-107">Parameters</span></span>

<span data-ttu-id="0b262-108">*Filetype*</span><span class="sxs-lookup"><span data-stu-id="0b262-108">*FileTypeSet*</span></span>

<span data-ttu-id="0b262-109">in Valore [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) che indica il tipo di file impostato da utilizzare per il processo di creazione.</span><span class="sxs-lookup"><span data-stu-id="0b262-109">[in] The [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) value that indicates the file type set to be used for the create process.</span></span>

<span data-ttu-id="0b262-110">*SetFlags*</span><span class="sxs-lookup"><span data-stu-id="0b262-110">*SetFlags*</span></span>

<span data-ttu-id="0b262-111">in Uno o più valori [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) che specificano i flag da utilizzare durante il processo di creazione, oltre ai flag predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0b262-111">[in] One or more [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) values that specify the flags to be used during the create process, in addition to the default flags.</span></span>

<span data-ttu-id="0b262-112">*ResetFlags*</span><span class="sxs-lookup"><span data-stu-id="0b262-112">*ResetFlags*</span></span>

<span data-ttu-id="0b262-113">in Uno o più valori [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) che specificano i flag predefiniti da reimpostare durante il processo di creazione.</span><span class="sxs-lookup"><span data-stu-id="0b262-113">[in] One or more [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) values that specify the default flags to be reset during the create process.</span></span>

<span data-ttu-id="0b262-114">*Origine*</span><span class="sxs-lookup"><span data-stu-id="0b262-114">*Source*</span></span>

<span data-ttu-id="0b262-115">in Struttura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenente un puntatore al buffer che contiene i dati di origine.</span><span class="sxs-lookup"><span data-stu-id="0b262-115">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the source data.</span></span>

<span data-ttu-id="0b262-116">*Destinazione*</span><span class="sxs-lookup"><span data-stu-id="0b262-116">*Target*</span></span>

<span data-ttu-id="0b262-117">in Struttura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenente un puntatore al buffer che contiene i dati di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0b262-117">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the target data.</span></span>

<span data-ttu-id="0b262-118">*SourceOptions*</span><span class="sxs-lookup"><span data-stu-id="0b262-118">*SourceOptions*</span></span>

<span data-ttu-id="0b262-119">[in] Riservato.</span><span class="sxs-lookup"><span data-stu-id="0b262-119">[in] Reserved.</span></span> <span data-ttu-id="0b262-120">Passare una struttura di [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con l'oggetto *modificabile* impostato su **false**, *lpStart* impostato su **null** e *uSize* impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="0b262-120">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *Editable* set to **FALSE**, *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="0b262-121">*TargetOptions*</span><span class="sxs-lookup"><span data-stu-id="0b262-121">*TargetOptions*</span></span>

<span data-ttu-id="0b262-122">[in] Riservato.</span><span class="sxs-lookup"><span data-stu-id="0b262-122">[in] Reserved.</span></span> <span data-ttu-id="0b262-123">Passare una struttura di [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con l'oggetto *modificabile* impostato su **false**, *lpStart* impostato su **null** e *uSize* impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="0b262-123">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *Editable* set to **FALSE**, *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="0b262-124">*GlobalOptions*</span><span class="sxs-lookup"><span data-stu-id="0b262-124">*GlobalOptions*</span></span>

<span data-ttu-id="0b262-125">[in] Riservato.</span><span class="sxs-lookup"><span data-stu-id="0b262-125">[in] Reserved.</span></span> <span data-ttu-id="0b262-126">Passare una struttura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con *LpStart* impostato su **null** e *uSize* impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="0b262-126">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="0b262-127">*lpTargetFileTime*</span><span class="sxs-lookup"><span data-stu-id="0b262-127">*lpTargetFileTime*</span></span>

<span data-ttu-id="0b262-128">in Timestamp impostato sul file di destinazione dopo l'applicazione del Delta.</span><span class="sxs-lookup"><span data-stu-id="0b262-128">[in] The time stamp set on the target file after delta apply.</span></span> <span data-ttu-id="0b262-129">Se **null**, il timestamp di destinazione sarà l'ora corrente durante il processo di creazione.</span><span class="sxs-lookup"><span data-stu-id="0b262-129">If **NULL**, the target timestamp will be the current time during the create process.</span></span>

<span data-ttu-id="0b262-130">*HashAlgId*</span><span class="sxs-lookup"><span data-stu-id="0b262-130">*HashAlgId*</span></span>

<span data-ttu-id="0b262-131">in ALG_ID dell'algoritmo da utilizzare per generare la firma di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0b262-131">[in] ALG_ID of the algorithm to be used to generate the target signature.</span></span> <span data-ttu-id="0b262-132">Alcuni valori speciali sono:</span><span class="sxs-lookup"><span data-stu-id="0b262-132">Some special values are:</span></span>

- <span data-ttu-id="0b262-133">0 = nessuna firma</span><span class="sxs-lookup"><span data-stu-id="0b262-133">0 = No signature</span></span>
- <span data-ttu-id="0b262-134">32 = CRC a 32 bit definito in msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="0b262-134">32 = 32-bit CRC defined in msdelta.dll</span></span>

<span data-ttu-id="0b262-135">*lpDelta*</span><span class="sxs-lookup"><span data-stu-id="0b262-135">*lpDelta*</span></span>

<span data-ttu-id="0b262-136">out Puntatore alla struttura [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) in cui deve essere scritto il Delta.</span><span class="sxs-lookup"><span data-stu-id="0b262-136">[out] Pointer to the [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) structure where the delta is to be written.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b262-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b262-137">Return value</span></span>

<span data-ttu-id="0b262-138">Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="0b262-138">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="0b262-139">Quando la funzione restituisce **false**, è possibile chiamare [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere il codice di errore del sistema Win32 corrispondente.</span><span class="sxs-lookup"><span data-stu-id="0b262-139">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b262-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b262-140">Requirements</span></span>

| <span data-ttu-id="0b262-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b262-141">Requirement</span></span> | <span data-ttu-id="0b262-142">Valore</span><span class="sxs-lookup"><span data-stu-id="0b262-142">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b262-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b262-143">Header</span></span> | <span data-ttu-id="0b262-144">msdelta. h</span><span class="sxs-lookup"><span data-stu-id="0b262-144">msdelta.h</span></span> |
| <span data-ttu-id="0b262-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0b262-145">DLL</span></span> | <span data-ttu-id="0b262-146">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="0b262-146">msdelta.dll</span></span> |
| <span data-ttu-id="0b262-147">Unicode</span><span class="sxs-lookup"><span data-stu-id="0b262-147">Unicode</span></span> | <span data-ttu-id="0b262-148">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0b262-148">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="0b262-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b262-149">See also</span></span>

[<span data-ttu-id="0b262-150">MSDelta</span><span class="sxs-lookup"><span data-stu-id="0b262-150">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="0b262-151">DeltaFree</span><span class="sxs-lookup"><span data-stu-id="0b262-151">DeltaFree</span></span>](msdelta-deltafree.md)
