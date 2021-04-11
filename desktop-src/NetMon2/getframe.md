---
description: La funzione GetFrame restituisce un handle per un frame specificato all'interno di un'acquisizione.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: Funzione GetFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f79e7fa6fc4e79f4dea804769cc9d51b8096860
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128342"
---
# <a name="getframe-function"></a><span data-ttu-id="a9a9a-103">Funzione GetFrame</span><span class="sxs-lookup"><span data-stu-id="a9a9a-103">GetFrame function</span></span>

<span data-ttu-id="a9a9a-104">La funzione **GetFrame** restituisce un handle per un frame specificato all'interno di un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a9a9a-104">The **GetFrame** function returns a handle to a given frame within a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a9a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9a9a-105">Syntax</span></span>


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a><span data-ttu-id="a9a9a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9a9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9a9a-107">*hCapture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9a9a-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9a9a-108">Handle per un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a9a9a-108">Handle to a capture.</span></span> <span data-ttu-id="a9a9a-109">Per ottenere l'handle di acquisizione, chiamare la funzione [GetFrameCaptureHandle](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="a9a9a-109">To obtain the capture handle, call the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a9a9a-110">*NumeroFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9a9a-110">*FrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9a9a-111">Numero (in base zero) del frame.</span><span class="sxs-lookup"><span data-stu-id="a9a9a-111">Number (zero-based) of the frame.</span></span> <span data-ttu-id="a9a9a-112">Il numero del primo fotogramma in un'acquisizione è zero.</span><span class="sxs-lookup"><span data-stu-id="a9a9a-112">The number of the first frame in a capture is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9a9a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9a9a-113">Return value</span></span>

<span data-ttu-id="a9a9a-114">Se la funzione ha esito positivo, il valore restituito è un handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="a9a9a-114">If the function is successful, the return value is a handle to the frame.</span></span>

<span data-ttu-id="a9a9a-115">Se la funzione ha esito negativo, ovvero se *hCapture* non è valido o il numero di frame non è compreso nell'intervallo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="a9a9a-115">If the function is unsuccessful (that is, if *hCapture* is invalid, or the frame number is out of range), the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9a9a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9a9a-116">Remarks</span></span>

<span data-ttu-id="a9a9a-117">Usare la funzione **GetFrame** per ottenere l'handle di frame necessario per l'individuazione delle istanze di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="a9a9a-117">Use the **GetFrame** function to obtain the frame handle needed when locating instances of a property.</span></span> <span data-ttu-id="a9a9a-118">Le funzioni utilizzate per individuare le istanze di proprietà sono [FindPropertyInstance](findpropertyinstance.md) che individua la prima istanza e [FindPropertyInstanceRestart](findpropertyinstancerestart.md) che individua l'istanza successiva.</span><span class="sxs-lookup"><span data-stu-id="a9a9a-118">The functions used to locate property instances are [FindPropertyInstance](findpropertyinstance.md) which locates the first instance, and [FindPropertyInstanceRestart](findpropertyinstancerestart.md) which locates the next instance.</span></span>

<span data-ttu-id="a9a9a-119">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrame** .</span><span class="sxs-lookup"><span data-stu-id="a9a9a-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9a9a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9a9a-120">Requirements</span></span>



| <span data-ttu-id="a9a9a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9a9a-121">Requirement</span></span> | <span data-ttu-id="a9a9a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a9a9a-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a9a-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9a9a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a9a9a-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9a9a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a9a9a-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9a9a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a9a9a-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9a9a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a9a9a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9a9a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9a9a-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9a9a-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a9a9a-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="a9a9a-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9a9a-130"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9a9a-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a9a9a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a9a9a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9a9a-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9a9a-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9a9a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9a9a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a9a-134">FindPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="a9a9a-134">FindPropertyInstance</span></span>](findpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="a9a9a-135">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="a9a9a-135">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




