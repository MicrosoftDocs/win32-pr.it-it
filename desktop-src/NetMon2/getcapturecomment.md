---
description: Restituisce un puntatore al commento di un'acquisizione.
ms.assetid: 3ef5c5b3-5586-469f-8975-049713715403
title: Funzione GetCaptureComment (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureComment
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ca2d3dd3fdc91c54c49b12119a56180396df5ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305917"
---
# <a name="getcapturecomment-function"></a><span data-ttu-id="d178e-103">GetCaptureComment (funzione)</span><span class="sxs-lookup"><span data-stu-id="d178e-103">GetCaptureComment function</span></span>

<span data-ttu-id="d178e-104">La funzione **GetCaptureComment** restituisce un puntatore al commento di un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d178e-104">The **GetCaptureComment** function returns a pointer to the comment of a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="d178e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d178e-105">Syntax</span></span>


```C++
LPSTR WINAPI GetCaptureComment(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="d178e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d178e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d178e-107">*hCapture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d178e-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d178e-108">Handle per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d178e-108">A handle to the capture.</span></span> <span data-ttu-id="d178e-109">Per ulteriori informazioni su come ottenere l'handle di acquisizione, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d178e-109">For more information about obtaining the capture handle, see the Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d178e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d178e-110">Return value</span></span>

<span data-ttu-id="d178e-111">Se la funzione ha esito positivo, ovvero se l'acquisizione contiene un commento, il valore restituito è un puntatore alla stringa di commento.</span><span class="sxs-lookup"><span data-stu-id="d178e-111">If the function is successful (that is, if the capture contains a comment), the return value is a pointer to the comment string.</span></span>

<span data-ttu-id="d178e-112">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d178e-112">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d178e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d178e-113">Remarks</span></span>

<span data-ttu-id="d178e-114">Non modificare la stringa di commento restituita che corrisponde alla stringa di commento effettiva presente nell'acquisizione caricata.</span><span class="sxs-lookup"><span data-stu-id="d178e-114">Do not alter the returned comment string which is the actual comment string that is in the loaded capture.</span></span> <span data-ttu-id="d178e-115">Qualsiasi modifica può danneggiare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d178e-115">Any changes can corrupt the capture.</span></span> <span data-ttu-id="d178e-116">Il tentativo di modificare la stringa genera una violazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="d178e-116">Attempts to modify the string result in an access violation.</span></span>

<span data-ttu-id="d178e-117">L'handle dell'acquisizione può essere ottenuto in diversi modi, a seconda se la chiamata viene eseguita da un esperto o da un parser.</span><span class="sxs-lookup"><span data-stu-id="d178e-117">The handle of the capture can be obtained in several ways, depending if the call is made by an expert or parser.</span></span> <span data-ttu-id="d178e-118">Per gli esperti, l'handle viene specificato nel membro **hCapture** della struttura [EXPERTSTARTUPINFO](expertstartupinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="d178e-118">For experts, the handle is specified in the **hCapture** member of the [EXPERTSTARTUPINFO](expertstartupinfo.md) structure.</span></span> <span data-ttu-id="d178e-119">Per i parser, è possibile ottenere l'handle di acquisizione chiamando la funzione [GetFrameCaptureHandle](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="d178e-119">For parsers, the capture handle can be obtained by calling the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

<span data-ttu-id="d178e-120">Per recuperare il commento di un'acquisizione dal relativo file di acquisizione, chiamare la funzione [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) .</span><span class="sxs-lookup"><span data-stu-id="d178e-120">To retrieve the comment of a capture from its capture file, call the [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) function.</span></span>

<span data-ttu-id="d178e-121">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetCaptureComment** .</span><span class="sxs-lookup"><span data-stu-id="d178e-121">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureComment** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d178e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d178e-122">Requirements</span></span>



| <span data-ttu-id="d178e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d178e-123">Requirement</span></span> | <span data-ttu-id="d178e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d178e-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d178e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d178e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d178e-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d178e-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d178e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d178e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d178e-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d178e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d178e-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d178e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d178e-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d178e-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d178e-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="d178e-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="d178e-132"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d178e-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d178e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d178e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d178e-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d178e-134"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d178e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d178e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d178e-136">EXPERTSTARTUPINFO</span><span class="sxs-lookup"><span data-stu-id="d178e-136">EXPERTSTARTUPINFO</span></span>](expertstartupinfo.md)
</dt> <dt>

[<span data-ttu-id="d178e-137">GetCaptureCommentFromFilename</span><span class="sxs-lookup"><span data-stu-id="d178e-137">GetCaptureCommentFromFilename</span></span>](getcapturecommentfromfilename.md)
</dt> <dt>

[<span data-ttu-id="d178e-138">GetFrameCaptureHandle</span><span class="sxs-lookup"><span data-stu-id="d178e-138">GetFrameCaptureHandle</span></span>](getframecapturehandle.md)
</dt> </dl>

 

 




