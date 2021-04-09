---
description: La funzione GetFrameCaptureHandle restituisce un handle per l'acquisizione in base a un frame specificato.
ms.assetid: 71b32799-194c-40f8-8438-36aebaba31c7
title: Funzione GetFrameCaptureHandle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameCaptureHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3770ad0fd3db7d1c076b5d1f286c1fdbdc2707a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878654"
---
# <a name="getframecapturehandle-function"></a><span data-ttu-id="86d9c-103">GetFrameCaptureHandle (funzione)</span><span class="sxs-lookup"><span data-stu-id="86d9c-103">GetFrameCaptureHandle function</span></span>

<span data-ttu-id="86d9c-104">La funzione **GetFrameCaptureHandle** restituisce un handle per l'acquisizione in base a un frame specificato.</span><span class="sxs-lookup"><span data-stu-id="86d9c-104">The **GetFrameCaptureHandle** function returns a handle to the capture based on a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="86d9c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86d9c-105">Syntax</span></span>


```C++
HCAPTURE WINAPI GetFrameCaptureHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="86d9c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="86d9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86d9c-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86d9c-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86d9c-108">Handle per un frame.</span><span class="sxs-lookup"><span data-stu-id="86d9c-108">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86d9c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86d9c-109">Return value</span></span>

<span data-ttu-id="86d9c-110">Se la funzione ha esito positivo, il valore restituito è un handle per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="86d9c-110">If the function is successful, the return value is a handle to the capture.</span></span>

<span data-ttu-id="86d9c-111">Se la funzione ha esito negativo, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="86d9c-111">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="86d9c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="86d9c-112">Remarks</span></span>

<span data-ttu-id="86d9c-113">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameCaptureHandle** .</span><span class="sxs-lookup"><span data-stu-id="86d9c-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameCaptureHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="86d9c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86d9c-114">Requirements</span></span>



| <span data-ttu-id="86d9c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="86d9c-115">Requirement</span></span> | <span data-ttu-id="86d9c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="86d9c-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="86d9c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86d9c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="86d9c-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="86d9c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="86d9c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86d9c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="86d9c-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="86d9c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="86d9c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86d9c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="86d9c-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="86d9c-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="86d9c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="86d9c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="86d9c-124"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86d9c-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="86d9c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="86d9c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86d9c-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86d9c-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




