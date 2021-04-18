---
description: La funzione ModifyFrame modifica un frame esistente con nuovi dati.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: Funzione ModifyFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ModifyFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: af3ef6c2c5ccae2b6410ac8fc81c815f790b17a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307714"
---
# <a name="modifyframe-function"></a><span data-ttu-id="2d46e-103">ModifyFrame (funzione)</span><span class="sxs-lookup"><span data-stu-id="2d46e-103">ModifyFrame function</span></span>

<span data-ttu-id="2d46e-104">La funzione **ModifyFrame** modifica un frame esistente con nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="2d46e-104">The **ModifyFrame** function alters an existing frame with new data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d46e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d46e-105">Syntax</span></span>


```C++
HFRAME WINAPI ModifyFrame(
  _In_  HCAPTURE hCapture,
  _In_  DWORD    FrameNumber,
  _In_  LPBYTE   FrameData,
  _In_  DWORD    FrameLength,
  _Out_ __int64  TimeStamp
);
```



## <a name="parameters"></a><span data-ttu-id="2d46e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d46e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d46e-107">*hCapture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d46e-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d46e-108">Handle per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="2d46e-108">Handle to the capture.</span></span> <span data-ttu-id="2d46e-109">Per informazioni sull'acquisizione dell'handle di acquisizione, vedere la sezione Osservazioni di questo argomento **ModifyFrame** .</span><span class="sxs-lookup"><span data-stu-id="2d46e-109">For information about obtaining the capture handle, see the Remarks section of this **ModifyFrame** topic.</span></span>

</dd> <dt>

<span data-ttu-id="2d46e-110">*NumeroFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d46e-110">*FrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d46e-111">Numero di indice del frame.</span><span class="sxs-lookup"><span data-stu-id="2d46e-111">Frame index number.</span></span>

</dd> <dt>

<span data-ttu-id="2d46e-112">*FrameData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d46e-112">*FrameData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d46e-113">Puntatore a una matrice di byte che contiene i nuovi dati del frame.</span><span class="sxs-lookup"><span data-stu-id="2d46e-113">Pointer to an array of bytes that contain the new frame data.</span></span>

</dd> <dt>

<span data-ttu-id="2d46e-114">*FrameLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d46e-114">*FrameLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d46e-115">Lunghezza dei nuovi dati, in byte.</span><span class="sxs-lookup"><span data-stu-id="2d46e-115">Length of the new data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2d46e-116">*Timestamp* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2d46e-116">*TimeStamp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d46e-117">Timestamp che indica il momento in cui è stato modificato il frame.</span><span class="sxs-lookup"><span data-stu-id="2d46e-117">Time stamp indicating when the frame was modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d46e-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d46e-118">Return value</span></span>

<span data-ttu-id="2d46e-119">Se la funzione ha esito positivo, il valore restituito è un handle per un nuovo frame.</span><span class="sxs-lookup"><span data-stu-id="2d46e-119">If the function is successful, the return value is a handle to a new frame.</span></span>

<span data-ttu-id="2d46e-120">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="2d46e-120">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d46e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d46e-121">Remarks</span></span>

<span data-ttu-id="2d46e-122">Se la chiamata ha esito positivo, la funzione **ModifyFrame** Elimina il frame originale.</span><span class="sxs-lookup"><span data-stu-id="2d46e-122">If the call is successful, the **ModifyFrame** function destroys the original frame.</span></span>

<span data-ttu-id="2d46e-123">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **ModifyFrame** .</span><span class="sxs-lookup"><span data-stu-id="2d46e-123">[*Experts*](e.md) and [*parsers*](p.md) can call the **ModifyFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d46e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d46e-124">Requirements</span></span>



| <span data-ttu-id="2d46e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d46e-125">Requirement</span></span> | <span data-ttu-id="2d46e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="2d46e-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2d46e-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d46e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2d46e-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d46e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2d46e-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d46e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2d46e-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d46e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2d46e-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d46e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d46e-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d46e-132"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2d46e-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="2d46e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="2d46e-134"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d46e-134"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2d46e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2d46e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d46e-136"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d46e-136"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




