---
title: RoFailFastWithErrorContextInternal2 (funzione)
description: Genera un'eccezione non continuabile nel processo corrente e consente anche di includere un contesto di errore aggiuntivo non ancora acquisito dal sistema operativo.
ms.localizationpriority: low
ms.topic: reference
ms.date: 03/13/2020
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ComBase.dll
api_name:
- RoFailFastWithErrorContextInternal2
targetos: Windows
ms.openlocfilehash: 84584c339851ecbf8df5d6dbda2aaa575ca6487b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300596"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a><span data-ttu-id="e018d-103">RoFailFastWithErrorContextInternal2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="e018d-103">RoFailFastWithErrorContextInternal2 function</span></span>

<span data-ttu-id="e018d-104">Genera un'eccezione non continuabile nel processo corrente e consente anche di includere un contesto di errore aggiuntivo non ancora acquisito dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e018d-104">Raises a non-continuable exception in the current process, and also allows you to include additional error context not already captured by the operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="e018d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e018d-105">Syntax</span></span>

```cpp
void WINAPI RoFailFastWithErrorContextInternal2(
  HRESULT hrError,
  ULONG cStowedExceptions,
  _In_reads_opt_(cStowedExceptions) PSTOWED_EXCEPTION_INFORMATION_V2 aStowedExceptionPointers[]
);
```

## <a name="parameters"></a><span data-ttu-id="e018d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e018d-106">Parameters</span></span>

`hrError`

<span data-ttu-id="e018d-107">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="e018d-107">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="e018d-108">**HRESULT** associato all'errore corrente.</span><span class="sxs-lookup"><span data-stu-id="e018d-108">The **HRESULT** associated with the current error.</span></span> <span data-ttu-id="e018d-109">L'eccezione viene generata per qualsiasi valore di *hrError*.</span><span class="sxs-lookup"><span data-stu-id="e018d-109">The exception is raised for any value of *hrError*.</span></span>

`cStowedExceptions`

<span data-ttu-id="e018d-110">Tipo: **[ULONG](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e018d-110">Type: **[ULONG](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e018d-111">Numero di elementi nella matrice *aStowedExceptionPointers* .</span><span class="sxs-lookup"><span data-stu-id="e018d-111">The number of elements in the *aStowedExceptionPointers* array.</span></span>

`aStowedExceptionPointers`

<span data-ttu-id="e018d-112">Tipo: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**</span><span class="sxs-lookup"><span data-stu-id="e018d-112">Type: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**</span></span>

<span data-ttu-id="e018d-113">Matrice di puntatori a strutture di [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) .</span><span class="sxs-lookup"><span data-stu-id="e018d-113">An array of pointers to [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) structures.</span></span> <span data-ttu-id="e018d-114">Ogni struttura contiene informazioni che descrivono un'eccezione riposta.</span><span class="sxs-lookup"><span data-stu-id="e018d-114">Each structure contains info describing a stowed exception.</span></span> <span data-ttu-id="e018d-115">Le informazioni contenute in queste strutture vengono quindi inviate a Segnalazione errori Windows (WER) insieme alle informazioni rilevate sulle eccezioni acquisite dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="e018d-115">The info in these structures is then submitted to Windows Error Reporting (WER) along with the stowed exception information that was captured by the platform.</span></span>

## <a name="return-value"></a><span data-ttu-id="e018d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e018d-116">Return value</span></span>

<span data-ttu-id="e018d-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e018d-117">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e018d-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="e018d-118">Remarks</span></span>

<span data-ttu-id="e018d-119">**RoFailFastWithErrorContextInternal2** non è associato a una libreria di importazione né a un file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="e018d-119">**RoFailFastWithErrorContextInternal2** isn't associated with an import library nor a header file.</span></span> <span data-ttu-id="e018d-120">È possibile chiamare il metodo usando prima la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) (per caricare `ComBase.dll` ), quindi chiamando la funzione [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per recuperare l'indirizzo di **RoFailFastWithErrorContextInternal2**.</span><span class="sxs-lookup"><span data-stu-id="e018d-120">You can call it by first using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) function (to load `ComBase.dll`), and then by calling the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve the address of **RoFailFastWithErrorContextInternal2**.</span></span>

<span data-ttu-id="e018d-121">Per altre informazioni, vedere [funzione RoFailFastWithErrorContext](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).</span><span class="sxs-lookup"><span data-stu-id="e018d-121">For more info, see [RoFailFastWithErrorContext function](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).</span></span>

## <a name="requirements"></a><span data-ttu-id="e018d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e018d-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e018d-123">**Piattaforma di destinazione**</span><span class="sxs-lookup"><span data-stu-id="e018d-123">**Target Platform**</span></span> | <span data-ttu-id="e018d-124">Windows</span><span class="sxs-lookup"><span data-stu-id="e018d-124">Windows</span></span> |
| <span data-ttu-id="e018d-125">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="e018d-125">**Header**</span></span> | <span data-ttu-id="e018d-126">N/D</span><span class="sxs-lookup"><span data-stu-id="e018d-126">N/A</span></span> |
| <span data-ttu-id="e018d-127">**Libreria**</span><span class="sxs-lookup"><span data-stu-id="e018d-127">**Library**</span></span> | <span data-ttu-id="e018d-128">N/D</span><span class="sxs-lookup"><span data-stu-id="e018d-128">N/A</span></span> |
| <span data-ttu-id="e018d-129">**DLL**</span><span class="sxs-lookup"><span data-stu-id="e018d-129">**DLL**</span></span> | <span data-ttu-id="e018d-130">ComBase.dll</span><span class="sxs-lookup"><span data-stu-id="e018d-130">ComBase.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="e018d-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e018d-131">See also</span></span>

* [<span data-ttu-id="e018d-132">RoFailFastWithErrorContext (funzione)</span><span class="sxs-lookup"><span data-stu-id="e018d-132">RoFailFastWithErrorContext function</span></span>](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)