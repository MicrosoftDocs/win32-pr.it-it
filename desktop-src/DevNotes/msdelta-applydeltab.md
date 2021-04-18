---
description: Usa il Delta e l'origine (forniti come buffer) per creare una nuova copia dei dati di destinazione. I dati di output vengono restituiti in un buffer allocato da MSDelta.
title: ApplyDeltaB (funzione)
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: ApplyDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplyDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 368788ba894064aa8ac3f8c9711f987a32f306af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331466"
---
# <a name="applydeltab-function"></a><span data-ttu-id="40f66-104">ApplyDeltaB (funzione)</span><span class="sxs-lookup"><span data-stu-id="40f66-104">ApplyDeltaB function</span></span>

<span data-ttu-id="40f66-105">Usa il Delta e l'origine (forniti come buffer) per creare una nuova copia dei dati di destinazione.</span><span class="sxs-lookup"><span data-stu-id="40f66-105">Uses the delta and source (provided as buffers) to create a new copy of the target data.</span></span> <span data-ttu-id="40f66-106">I dati di output vengono restituiti in un buffer allocato da MSDelta.</span><span class="sxs-lookup"><span data-stu-id="40f66-106">The output data is returned in an MSDelta-allocated buffer.</span></span>

> [!NOTE]
> <span data-ttu-id="40f66-107">È necessario chiamare [DeltaFree](msdelta-deltafree.md) per liberare il buffer di output dopo che questa funzione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="40f66-107">You must call [DeltaFree](msdelta-deltafree.md) to free the output buffer after this function has completed.</span></span>

> [!NOTE]
> <span data-ttu-id="40f66-108">Se il delta specificato è stato creato con [PatchAPI](patchapi.md)e viene impostato il FLAG di [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) , msdelta chiamerà PatchAPI per applicare il Delta.</span><span class="sxs-lookup"><span data-stu-id="40f66-108">If the specified delta was created using [PatchAPI](patchapi.md), and the [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) flag is set, MSDelta will call PatchAPI to apply the delta.</span></span>

## <a name="syntax"></a><span data-ttu-id="40f66-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40f66-109">Syntax</span></span>

```cpp
BOOL  WINAPI  ApplyDeltaB(
    DELTA_FLAG_TYPE  ApplyFlags,
    DELTA_INPUT      Source,
    DELTA_INPUT      Delta,
    LPDELTA_OUTPUT   lpTarget
   );
```

## <a name="parameters"></a><span data-ttu-id="40f66-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="40f66-110">Parameters</span></span>

<span data-ttu-id="40f66-111">*ApplyFlags*</span><span class="sxs-lookup"><span data-stu-id="40f66-111">*ApplyFlags*</span></span>

<span data-ttu-id="40f66-112">in [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) o [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).</span><span class="sxs-lookup"><span data-stu-id="40f66-112">[in] Either [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) or [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).</span></span>

<span data-ttu-id="40f66-113">*Origine*</span><span class="sxs-lookup"><span data-stu-id="40f66-113">*Source*</span></span>

<span data-ttu-id="40f66-114">in Struttura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenente un puntatore al buffer che contiene i dati di origine.</span><span class="sxs-lookup"><span data-stu-id="40f66-114">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the source data.</span></span>

<span data-ttu-id="40f66-115">*Delta*</span><span class="sxs-lookup"><span data-stu-id="40f66-115">*Delta*</span></span>

<span data-ttu-id="40f66-116">in Struttura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenente un puntatore al buffer che contiene i dati Delta.</span><span class="sxs-lookup"><span data-stu-id="40f66-116">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the delta data.</span></span>

<span data-ttu-id="40f66-117">*lpTarget*</span><span class="sxs-lookup"><span data-stu-id="40f66-117">*lpTarget*</span></span>

<span data-ttu-id="40f66-118">out Puntatore alla struttura [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) in cui deve essere scritta la destinazione.</span><span class="sxs-lookup"><span data-stu-id="40f66-118">[out] Pointer to the [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) structure where the target is to be written.</span></span>

## <a name="return-value"></a><span data-ttu-id="40f66-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40f66-119">Return value</span></span>

<span data-ttu-id="40f66-120">Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="40f66-120">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="40f66-121">Quando la funzione restituisce **false**, è possibile chiamare [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere il codice di errore del sistema Win32 corrispondente.</span><span class="sxs-lookup"><span data-stu-id="40f66-121">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="40f66-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40f66-122">Requirements</span></span>

| <span data-ttu-id="40f66-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="40f66-123">Requirement</span></span> | <span data-ttu-id="40f66-124">Valore</span><span class="sxs-lookup"><span data-stu-id="40f66-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40f66-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40f66-125">Header</span></span> | <span data-ttu-id="40f66-126">msdelta. h</span><span class="sxs-lookup"><span data-stu-id="40f66-126">msdelta.h</span></span> |
| <span data-ttu-id="40f66-127">DLL</span><span class="sxs-lookup"><span data-stu-id="40f66-127">DLL</span></span> | <span data-ttu-id="40f66-128">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="40f66-128">msdelta.dll</span></span> |
| <span data-ttu-id="40f66-129">Unicode</span><span class="sxs-lookup"><span data-stu-id="40f66-129">Unicode</span></span> | <span data-ttu-id="40f66-130">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="40f66-130">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="40f66-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40f66-131">See also</span></span>

[<span data-ttu-id="40f66-132">MSDelta</span><span class="sxs-lookup"><span data-stu-id="40f66-132">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="40f66-133">DeltaFree</span><span class="sxs-lookup"><span data-stu-id="40f66-133">DeltaFree</span></span>](msdelta-deltafree.md)
