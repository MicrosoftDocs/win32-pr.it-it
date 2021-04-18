---
UID: ''
title: CaptureStackBackTrace (funzione)
description: Acquisisce una traccia dello stack indietro facendo scorrere lo stack.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: RtlCaptureStackBackTrace
ms.topic: reference
req.header: WinBase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-rtlsupport-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-rtlsupport-l1-1-0.dll
api_name:
- CaptureStackBackTrace
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 3c9edc9184000d513b82ad4131e3ac05c2ed22d6
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2020
ms.locfileid: "106299329"
---
# <a name="capturestackbacktrace-function"></a><span data-ttu-id="15d08-103">CaptureStackBackTrace (funzione)</span><span class="sxs-lookup"><span data-stu-id="15d08-103">CaptureStackBackTrace function</span></span>

## <a name="description"></a><span data-ttu-id="15d08-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15d08-104">Description</span></span>

<span data-ttu-id="15d08-105">Acquisisce una traccia dello stack indietro scorrendo lo stack e registrando le informazioni per ogni fotogramma.</span><span class="sxs-lookup"><span data-stu-id="15d08-105">Captures a stack back trace by walking up the stack and recording the information for each frame.</span></span>

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a><span data-ttu-id="15d08-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="15d08-106">Parameters</span></span>

### <a name="framestoskip-in"></a><span data-ttu-id="15d08-107">FramesToSkip [in]</span><span class="sxs-lookup"><span data-stu-id="15d08-107">FramesToSkip [in]</span></span>

<span data-ttu-id="15d08-108">Numero di frame da ignorare dall'inizio della traccia indietro.</span><span class="sxs-lookup"><span data-stu-id="15d08-108">The number of frames to skip from the start of the back trace.</span></span>

### <a name="framestocapture-in"></a><span data-ttu-id="15d08-109">FramesToCapture [in]</span><span class="sxs-lookup"><span data-stu-id="15d08-109">FramesToCapture [in]</span></span>

<span data-ttu-id="15d08-110">Numero di frame da acquisire.</span><span class="sxs-lookup"><span data-stu-id="15d08-110">The number of frames to be captured.</span></span>
<span data-ttu-id="15d08-111">È possibile acquisire fino a **MAXUSHORT** frame.</span><span class="sxs-lookup"><span data-stu-id="15d08-111">You can capture up to **MAXUSHORT** frames.</span></span>

<span data-ttu-id="15d08-112">**Windows Server 2003 e Windows XP:**  La somma dei parametri *FramesToSkip* e *FramesToCapture* deve essere minore di 63.</span><span class="sxs-lookup"><span data-stu-id="15d08-112">**Windows Server 2003 and Windows XP:**  The sum of the *FramesToSkip* and *FramesToCapture* parameters must be less than 63.</span></span>

### <a name="backtrace-out"></a><span data-ttu-id="15d08-113">Backtrace [out]</span><span class="sxs-lookup"><span data-stu-id="15d08-113">BackTrace [out]</span></span>

<span data-ttu-id="15d08-114">Matrice di puntatori acquisiti dalla traccia dello stack corrente.</span><span class="sxs-lookup"><span data-stu-id="15d08-114">An array of pointers captured from the current stack trace.</span></span>

### <a name="backtracehash-out-optional"></a><span data-ttu-id="15d08-115">BackTraceHash [out, optional]</span><span class="sxs-lookup"><span data-stu-id="15d08-115">BackTraceHash [out, optional]</span></span>

<span data-ttu-id="15d08-116">Valore che può essere utilizzato per organizzare le tabelle hash.</span><span class="sxs-lookup"><span data-stu-id="15d08-116">A value that can be used to organize hash tables.</span></span>
<span data-ttu-id="15d08-117">Se questo parametro è **null**, non viene calcolato alcun valore hash.</span><span class="sxs-lookup"><span data-stu-id="15d08-117">If this parameter is **NULL**, then no hash value is computed.</span></span>

<span data-ttu-id="15d08-118">Questo valore viene calcolato in base ai valori dei puntatori restituiti nella matrice di backtrace.</span><span class="sxs-lookup"><span data-stu-id="15d08-118">This value is calculated based on the values of the pointers returned in the BackTrace array.</span></span>
<span data-ttu-id="15d08-119">Due tracce dello stack identiche genereranno valori hash identici.</span><span class="sxs-lookup"><span data-stu-id="15d08-119">Two identical stack traces will generate identical hash values.</span></span>

## <a name="returns"></a><span data-ttu-id="15d08-120">Restituisce</span><span class="sxs-lookup"><span data-stu-id="15d08-120">Returns</span></span>

<span data-ttu-id="15d08-121">Numero di frame acquisiti.</span><span class="sxs-lookup"><span data-stu-id="15d08-121">The number of captured frames.</span></span>

## <a name="remarks"></a><span data-ttu-id="15d08-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="15d08-122">Remarks</span></span>

<span data-ttu-id="15d08-123">La funzione **CaptureStackBackTrace** è definita come funzione **RtlCaptureStackBackTrace** (la definizione è inclusa nella Windows SDK a partire da Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="15d08-123">The **CaptureStackBackTrace** function is defined as the **RtlCaptureStackBackTrace** function (the definition is included in the Windows SDK beginning with Windows Vista).</span></span>
<span data-ttu-id="15d08-124">Per ulteriori informazioni, vedere WinBase. h e WinNT. h.</span><span class="sxs-lookup"><span data-stu-id="15d08-124">For more information, see WinBase.h and WinNT.h.</span></span>

## <a name="see-also"></a><span data-ttu-id="15d08-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="15d08-125">See also</span></span>
