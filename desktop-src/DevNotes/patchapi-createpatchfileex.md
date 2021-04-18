---
description: Crea un delta tra il file di origine specificato e il file di destinazione specificato.
title: Funzione CreatePatchFileExA/W
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: CreatePatchFileExA, CreatePatchFileExW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePatchFileExW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: c84be2d859a780e46e7e940aa4a7e7da5296f0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324441"
---
# <a name="createpatchfileexaw-function"></a><span data-ttu-id="852f7-103">Funzione CreatePatchFileExA/W</span><span class="sxs-lookup"><span data-stu-id="852f7-103">CreatePatchFileExA/W function</span></span>

<span data-ttu-id="852f7-104">Le funzioni **CreatePatchFileExA** e **CreatePatchFileExW** creano un delta tra il file di origine specificato e il file di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="852f7-104">The **CreatePatchFileExA** and **CreatePatchFileExW** functions create a delta between the specified source file and the specified target file.</span></span> <span data-ttu-id="852f7-105">I file di origine e di destinazione vengono forniti come percorsi.</span><span class="sxs-lookup"><span data-stu-id="852f7-105">Both the source and the target files are provided as paths.</span></span> <span data-ttu-id="852f7-106">Anche il Delta di output viene scritto in un percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="852f7-106">The output delta is also written to a provided path.</span></span> <span data-ttu-id="852f7-107">Queste funzioni forniscono report sullo stato di avanzamento durante il processo di creazione.</span><span class="sxs-lookup"><span data-stu-id="852f7-107">These functions provide progress reporting during the create process.</span></span>

## <a name="syntax"></a><span data-ttu-id="852f7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="852f7-108">Syntax</span></span>

```cpp
BOOL  PATCHAPI  CreatePatchFileExA(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCTSTR                   NewFileName,
    LPCTSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );

BOOL  PATCHAPI  CreatePatchFileExW(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCWSTR                   NewFileName,
    LPCWSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );
```

## <a name="parameters"></a><span data-ttu-id="852f7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="852f7-109">Parameters</span></span>

<span data-ttu-id="852f7-110">*OldFileCount*</span><span class="sxs-lookup"><span data-stu-id="852f7-110">*OldFileCount*</span></span>

<span data-ttu-id="852f7-111">Numero totale di file di origine.</span><span class="sxs-lookup"><span data-stu-id="852f7-111">The total number of source files.</span></span> <span data-ttu-id="852f7-112">Utilizzato per creare Delta rispetto a più file di origine (massimo 255).</span><span class="sxs-lookup"><span data-stu-id="852f7-112">Used to create deltas against multiple source files (maximum 255).</span></span>

<span data-ttu-id="852f7-113">*OldFileInfoArray*</span><span class="sxs-lookup"><span data-stu-id="852f7-113">*OldFileInfoArray*</span></span>

<span data-ttu-id="852f7-114">Puntatore alla matrice di informazioni sul file di origine.</span><span class="sxs-lookup"><span data-stu-id="852f7-114">Pointer to source file information array.</span></span>

<span data-ttu-id="852f7-115">*Nomenuovofile*</span><span class="sxs-lookup"><span data-stu-id="852f7-115">*NewFileName*</span></span>

<span data-ttu-id="852f7-116">Nome del file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="852f7-116">The name of the target file.</span></span>

<span data-ttu-id="852f7-117">*PatchFileName*</span><span class="sxs-lookup"><span data-stu-id="852f7-117">*PatchFileName*</span></span>

<span data-ttu-id="852f7-118">Nome del Delta creato.</span><span class="sxs-lookup"><span data-stu-id="852f7-118">The name of the delta that is created.</span></span>

<span data-ttu-id="852f7-119">*OptionFlags*</span><span class="sxs-lookup"><span data-stu-id="852f7-119">*OptionFlags*</span></span>

<span data-ttu-id="852f7-120">Flag di creazione.</span><span class="sxs-lookup"><span data-stu-id="852f7-120">Creation flags.</span></span>

<span data-ttu-id="852f7-121">*ProgressCallback*</span><span class="sxs-lookup"><span data-stu-id="852f7-121">*ProgressCallback*</span></span>

<span data-ttu-id="852f7-122">Puntatore al callback di stato definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="852f7-122">Pointer to application-defined progress callback.</span></span>

<span data-ttu-id="852f7-123">*CallbackContext*</span><span class="sxs-lookup"><span data-stu-id="852f7-123">*CallbackContext*</span></span>

<span data-ttu-id="852f7-124">Puntatore al contesto definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="852f7-124">Pointer to application-defined context.</span></span>

## <a name="return-value"></a><span data-ttu-id="852f7-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="852f7-125">Return value</span></span>

<span data-ttu-id="852f7-126">Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="852f7-126">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="852f7-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="852f7-127">Requirements</span></span>

| <span data-ttu-id="852f7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="852f7-128">Requirement</span></span> | <span data-ttu-id="852f7-129">Valore</span><span class="sxs-lookup"><span data-stu-id="852f7-129">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="852f7-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="852f7-130">Header</span></span> | <span data-ttu-id="852f7-131">PatchAPI. h</span><span class="sxs-lookup"><span data-stu-id="852f7-131">patchapi.h</span></span> |
| <span data-ttu-id="852f7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="852f7-132">DLL</span></span> | <span data-ttu-id="852f7-133">mspatchc.dll</span><span class="sxs-lookup"><span data-stu-id="852f7-133">mspatchc.dll</span></span> |
| <span data-ttu-id="852f7-134">Unicode</span><span class="sxs-lookup"><span data-stu-id="852f7-134">Unicode</span></span> | <span data-ttu-id="852f7-135">Implementato come CreatePatchFileExW (Unicode) e CreatePatchFileExA (ANSI)</span><span class="sxs-lookup"><span data-stu-id="852f7-135">Implemented as CreatePatchFileExW (Unicode) and CreatePatchFileExA (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="852f7-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="852f7-136">See also</span></span>

[<span data-ttu-id="852f7-137">PatchAPI</span><span class="sxs-lookup"><span data-stu-id="852f7-137">PatchAPI</span></span>](patchapi.md)
