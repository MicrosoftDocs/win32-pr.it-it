---
description: La funzione GetFrameLength restituisce la lunghezza del frame.
ms.assetid: 30be1f5c-9b13-42ad-944a-92b1aee8a6bc
title: Funzione GetFrameLength (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 29a2a08ac105414a914e14a9ce8e69976725700c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305906"
---
# <a name="getframelength-function"></a><span data-ttu-id="5f845-103">GetFrameLength (funzione)</span><span class="sxs-lookup"><span data-stu-id="5f845-103">GetFrameLength function</span></span>

<span data-ttu-id="5f845-104">La funzione **GetFrameLength** restituisce la lunghezza del frame.</span><span class="sxs-lookup"><span data-stu-id="5f845-104">The **GetFrameLength** function returns the length of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f845-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f845-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="5f845-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f845-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f845-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f845-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f845-108">Handle per un frame.</span><span class="sxs-lookup"><span data-stu-id="5f845-108">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f845-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f845-109">Return value</span></span>

<span data-ttu-id="5f845-110">Se la funzione ha esito positivo, il valore restituito è la lunghezza del frame in byte.</span><span class="sxs-lookup"><span data-stu-id="5f845-110">If the function is successful, the return value is the length of the frame   in bytes.</span></span>

<span data-ttu-id="5f845-111">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="5f845-111">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f845-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f845-112">Remarks</span></span>

<span data-ttu-id="5f845-113">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameLength** .</span><span class="sxs-lookup"><span data-stu-id="5f845-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f845-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f845-114">Requirements</span></span>



| <span data-ttu-id="5f845-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f845-115">Requirement</span></span> | <span data-ttu-id="5f845-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5f845-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5f845-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f845-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5f845-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f845-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5f845-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f845-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5f845-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f845-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5f845-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f845-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f845-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f845-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="5f845-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="5f845-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f845-124"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f845-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5f845-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5f845-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f845-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f845-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




