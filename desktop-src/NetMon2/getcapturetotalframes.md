---
description: La funzione GetCaptureTotalFrames restituisce il numero totale di frame nell'acquisizione.
ms.assetid: a2b7902c-b80f-4a0a-b12a-2a139df30fca
title: Funzione GetCaptureTotalFrames (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTotalFrames
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: aa7c81e690e9f7eab258c832ae374f18f9b7afc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878658"
---
# <a name="getcapturetotalframes-function"></a><span data-ttu-id="1afb3-103">GetCaptureTotalFrames (funzione)</span><span class="sxs-lookup"><span data-stu-id="1afb3-103">GetCaptureTotalFrames function</span></span>

<span data-ttu-id="1afb3-104">La funzione **GetCaptureTotalFrames** restituisce il numero totale di frame nell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="1afb3-104">The **GetCaptureTotalFrames** function returns the total number of frames in the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="1afb3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1afb3-105">Syntax</span></span>


```C++
DWORD WINAPI GetCaptureTotalFrames(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="1afb3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1afb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1afb3-107">*hCapture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1afb3-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1afb3-108">Handle per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="1afb3-108">Handle to the capture.</span></span> <span data-ttu-id="1afb3-109">Per informazioni sull'acquisizione dell'handle di acquisizione, vedere la sezione Osservazioni di questo argomento **GetCaptureTotalFrames** .</span><span class="sxs-lookup"><span data-stu-id="1afb3-109">For information about obtaining the capture handle, see the Remarks section of this **GetCaptureTotalFrames** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1afb3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1afb3-110">Return value</span></span>

<span data-ttu-id="1afb3-111">Se la funzione ha esito positivo, il valore restituito è il numero totale di frame nell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="1afb3-111">If the function is successful, the return value is the total number of frames in the capture.</span></span>

<span data-ttu-id="1afb3-112">Se la funzione ha esito negativo, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="1afb3-112">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="1afb3-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1afb3-113">Remarks</span></span>

<span data-ttu-id="1afb3-114">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetCaptureTotalFrames** .</span><span class="sxs-lookup"><span data-stu-id="1afb3-114">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureTotalFrames** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1afb3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1afb3-115">Requirements</span></span>



| <span data-ttu-id="1afb3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1afb3-116">Requirement</span></span> | <span data-ttu-id="1afb3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1afb3-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1afb3-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1afb3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1afb3-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1afb3-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1afb3-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1afb3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1afb3-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1afb3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1afb3-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1afb3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1afb3-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1afb3-123"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1afb3-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="1afb3-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="1afb3-125"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1afb3-125"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1afb3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1afb3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1afb3-127"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1afb3-127"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




