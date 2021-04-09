---
description: La funzione GetFrameNumber restituisce il numero di un frame.
ms.assetid: 97d343a3-2a1e-47d7-bfc2-b63f8d84b29d
title: Funzione GetFrameNumber (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameNumber
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: de04fa513fab98b1a82d036f6f40a6c67cdda3ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966468"
---
# <a name="getframenumber-function"></a><span data-ttu-id="ebccd-103">GetFrameNumber (funzione)</span><span class="sxs-lookup"><span data-stu-id="ebccd-103">GetFrameNumber function</span></span>

<span data-ttu-id="ebccd-104">La funzione **GetFrameNumber** restituisce il numero di un frame.</span><span class="sxs-lookup"><span data-stu-id="ebccd-104">The **GetFrameNumber** function returns the number of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebccd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebccd-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameNumber(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="ebccd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebccd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebccd-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebccd-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebccd-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="ebccd-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebccd-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebccd-109">Return value</span></span>

<span data-ttu-id="ebccd-110">Se la funzione ha esito positivo, il valore restituito è un numero di frame in base zero.</span><span class="sxs-lookup"><span data-stu-id="ebccd-110">If the function is successful, the return value is a zero-based frame number.</span></span>

<span data-ttu-id="ebccd-111">Se la funzione non ha esito positivo, il valore restituito è meno uno (-1).</span><span class="sxs-lookup"><span data-stu-id="ebccd-111">If the function is not successful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="ebccd-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebccd-112">Remarks</span></span>

<span data-ttu-id="ebccd-113">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameNumber** .</span><span class="sxs-lookup"><span data-stu-id="ebccd-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameNumber** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebccd-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebccd-114">Requirements</span></span>



| <span data-ttu-id="ebccd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebccd-115">Requirement</span></span> | <span data-ttu-id="ebccd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ebccd-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ebccd-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebccd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ebccd-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ebccd-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ebccd-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebccd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ebccd-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ebccd-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ebccd-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ebccd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebccd-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebccd-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ebccd-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="ebccd-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="ebccd-124"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebccd-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ebccd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ebccd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebccd-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebccd-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




