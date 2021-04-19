---
description: Libera il blocco di memoria specificato.
title: DeltaFree (funzione)
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: DeltaFree
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- DeltaFree
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 15885cfa3e879ed6a1e85b2f9553af92d436ca71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328692"
---
# <a name="deltafree-function"></a><span data-ttu-id="a4100-103">DeltaFree (funzione)</span><span class="sxs-lookup"><span data-stu-id="a4100-103">DeltaFree function</span></span>

<span data-ttu-id="a4100-104">Libera il blocco di memoria specificato.</span><span class="sxs-lookup"><span data-stu-id="a4100-104">Frees the specified memory block.</span></span> <span data-ttu-id="a4100-105">È necessario chiamare questa funzione dopo le chiamate a [CreateDeltaB](msdelta-createdeltab.md) e [ApplyDeltaB](msdelta-applydeltab.md) riuscite per liberare il buffer di memoria allocato da msdelta.</span><span class="sxs-lookup"><span data-stu-id="a4100-105">You must call this function after successful calls to [CreateDeltaB](msdelta-createdeltab.md) and [ApplyDeltaB](msdelta-applydeltab.md) to free the MSDelta-allocated memory buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4100-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4100-106">Syntax</span></span>

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a><span data-ttu-id="a4100-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4100-107">Parameters</span></span>

<span data-ttu-id="a4100-108">*lpMemory*</span><span class="sxs-lookup"><span data-stu-id="a4100-108">*lpMemory*</span></span>

<span data-ttu-id="a4100-109">in Blocco di memoria da liberare.</span><span class="sxs-lookup"><span data-stu-id="a4100-109">[in] Memory block to be freed.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4100-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4100-110">Return value</span></span>

<span data-ttu-id="a4100-111">Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="a4100-111">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="a4100-112">Quando la funzione restituisce **false**, è possibile chiamare [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere il codice di errore del sistema Win32 corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a4100-112">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4100-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4100-113">Requirements</span></span>

| <span data-ttu-id="a4100-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4100-114">Requirement</span></span> | <span data-ttu-id="a4100-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a4100-115">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4100-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4100-116">Header</span></span> | <span data-ttu-id="a4100-117">msdelta. h</span><span class="sxs-lookup"><span data-stu-id="a4100-117">msdelta.h</span></span> |
| <span data-ttu-id="a4100-118">DLL</span><span class="sxs-lookup"><span data-stu-id="a4100-118">DLL</span></span> | <span data-ttu-id="a4100-119">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="a4100-119">msdelta.dll</span></span> |
| <span data-ttu-id="a4100-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4100-120">Unicode</span></span> | <span data-ttu-id="a4100-121">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a4100-121">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="a4100-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4100-122">See also</span></span>

[<span data-ttu-id="a4100-123">MSDelta</span><span class="sxs-lookup"><span data-stu-id="a4100-123">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="a4100-124">CreateDeltaB</span><span class="sxs-lookup"><span data-stu-id="a4100-124">CreateDeltaB</span></span>](msdelta-createdeltab.md)

[<span data-ttu-id="a4100-125">ApplyDeltaB</span><span class="sxs-lookup"><span data-stu-id="a4100-125">ApplyDeltaB</span></span>](msdelta-applydeltab.md)
