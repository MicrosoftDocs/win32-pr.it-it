---
description: La funzione GetFrameTimeStamp restituisce il timestamp di un frame specificato.
ms.assetid: 4ac50400-6674-40fa-9a69-9c0ccb55b92c
title: Funzione GetFrameTimeStamp (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 37a75f946a5fc0ddb2b32d99334368a272fdf2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312835"
---
# <a name="getframetimestamp-function"></a><span data-ttu-id="49ae8-103">GetFrameTimeStamp (funzione)</span><span class="sxs-lookup"><span data-stu-id="49ae8-103">GetFrameTimeStamp function</span></span>

<span data-ttu-id="49ae8-104">La funzione **GetFrameTimeStamp** restituisce il timestamp di un frame specificato.</span><span class="sxs-lookup"><span data-stu-id="49ae8-104">The **GetFrameTimeStamp** function returns the time stamp of a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="49ae8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49ae8-105">Syntax</span></span>


```C++
__int64 WINAPI GetFrameTimeStamp(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="49ae8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="49ae8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49ae8-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49ae8-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ae8-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="49ae8-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49ae8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49ae8-109">Return value</span></span>

<span data-ttu-id="49ae8-110">Se la funzione ha esito positivo, il valore restituito è il timestamp del frame in microsecondi.</span><span class="sxs-lookup"><span data-stu-id="49ae8-110">If the function is successful, the return value is the time stamp of the frame   in microseconds.</span></span>

<span data-ttu-id="49ae8-111">Se la funzione ha esito negativo, il valore restituito è meno uno (-1).</span><span class="sxs-lookup"><span data-stu-id="49ae8-111">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="49ae8-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="49ae8-112">Remarks</span></span>

<span data-ttu-id="49ae8-113">La funzione **GetFrameTimeStamp** restituisce un timestamp che mostra il tempo trascorso tra l'inizio del processo di acquisizione e la registrazione del frame.</span><span class="sxs-lookup"><span data-stu-id="49ae8-113">The **GetFrameTimeStamp** function returns a time stamp that shows the elapsed time between the start of the capture process, and the recording of the frame.</span></span>

<span data-ttu-id="49ae8-114">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameTimeStamp** .</span><span class="sxs-lookup"><span data-stu-id="49ae8-114">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameTimeStamp** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="49ae8-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49ae8-115">Requirements</span></span>



| <span data-ttu-id="49ae8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="49ae8-116">Requirement</span></span> | <span data-ttu-id="49ae8-117">Valore</span><span class="sxs-lookup"><span data-stu-id="49ae8-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="49ae8-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49ae8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="49ae8-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="49ae8-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="49ae8-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49ae8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="49ae8-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="49ae8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="49ae8-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49ae8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="49ae8-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="49ae8-123"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="49ae8-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="49ae8-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="49ae8-125"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49ae8-125"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="49ae8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="49ae8-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49ae8-127"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49ae8-127"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




