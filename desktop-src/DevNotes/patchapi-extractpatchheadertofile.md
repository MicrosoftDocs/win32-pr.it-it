---
description: Estrae le informazioni di intestazione da un Delta.
title: Funzione ExtractPatchHeaderToFileA/W
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: ExtractPatchHeaderToFileA, ExtractPatchHeaderToFileW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtractPatchHeaderToFileW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 40835a0b88558046ff9086ffcd7ec4609d1ed863
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327844"
---
# <a name="extractpatchheadertofileaw-function"></a><span data-ttu-id="f7f51-103">Funzione ExtractPatchHeaderToFileA/W</span><span class="sxs-lookup"><span data-stu-id="f7f51-103">ExtractPatchHeaderToFileA/W function</span></span>

<span data-ttu-id="f7f51-104">Le funzioni **ExtractPatchHeaderToFileA** e **ExtractPatchHeaderToFileW** estraggono le informazioni di intestazione da un Delta.</span><span class="sxs-lookup"><span data-stu-id="f7f51-104">The **ExtractPatchHeaderToFileA** and **ExtractPatchHeaderToFileW** functions extract the header information from a delta.</span></span> <span data-ttu-id="f7f51-105">Il Delta viene fornito come percorso di file.</span><span class="sxs-lookup"><span data-stu-id="f7f51-105">The delta is provided as a file path.</span></span> <span data-ttu-id="f7f51-106">L'intestazione di output viene scritta anche in un percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="f7f51-106">The output header is also written to a provided path.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7f51-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7f51-107">Syntax</span></span>

```cpp
BOOL  PATCHAPI  ExtractPatchHeaderToFileA(
    LPCTSTR  PatchFileName,
    LPCTSTR  PatchHeaderFileName
    );

BOOL  PATCHAPI  ExtractPatchHeaderToFileW(
    LPCWSTR  PatchFileName,
    LPCWSTR  PatchHeaderFileName
    );
```

## <a name="parameters"></a><span data-ttu-id="f7f51-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7f51-108">Parameters</span></span>

<span data-ttu-id="f7f51-109">*PatchFileName*</span><span class="sxs-lookup"><span data-stu-id="f7f51-109">*PatchFileName*</span></span>

<span data-ttu-id="f7f51-110">Nome del Delta che contiene l'intestazione.</span><span class="sxs-lookup"><span data-stu-id="f7f51-110">The name of the delta containing the header.</span></span>

<span data-ttu-id="f7f51-111">*PatchHeaderFileName*</span><span class="sxs-lookup"><span data-stu-id="f7f51-111">*PatchHeaderFileName*</span></span>

<span data-ttu-id="f7f51-112">Nome del file di intestazione da creare.</span><span class="sxs-lookup"><span data-stu-id="f7f51-112">The name of the header file that is to be created.</span></span>

## <a name="return-value"></a><span data-ttu-id="f7f51-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7f51-113">Return value</span></span>

<span data-ttu-id="f7f51-114">Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="f7f51-114">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7f51-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7f51-115">Requirements</span></span>

| <span data-ttu-id="f7f51-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7f51-116">Requirement</span></span> | <span data-ttu-id="f7f51-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f7f51-117">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f51-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7f51-118">Header</span></span> | <span data-ttu-id="f7f51-119">PatchAPI. h</span><span class="sxs-lookup"><span data-stu-id="f7f51-119">patchapi.h</span></span> |
| <span data-ttu-id="f7f51-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f7f51-120">DLL</span></span> | <span data-ttu-id="f7f51-121">mspatchc.dll</span><span class="sxs-lookup"><span data-stu-id="f7f51-121">mspatchc.dll</span></span> |
| <span data-ttu-id="f7f51-122">Unicode</span><span class="sxs-lookup"><span data-stu-id="f7f51-122">Unicode</span></span> | <span data-ttu-id="f7f51-123">Implementato come ExtractPatchHeaderToFileW (Unicode) e ExtractPatchHeaderToFileA (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f7f51-123">Implemented as ExtractPatchHeaderToFileW (Unicode) and ExtractPatchHeaderToFileA (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="f7f51-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7f51-124">See also</span></span>

[<span data-ttu-id="f7f51-125">PatchAPI</span><span class="sxs-lookup"><span data-stu-id="f7f51-125">PatchAPI</span></span>](patchapi.md)
