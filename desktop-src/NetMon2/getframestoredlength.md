---
description: La funzione GetFrameStoredLength restituisce la lunghezza del frame.
ms.assetid: 7ac0e528-a45a-4c36-a99d-647347bdd143
title: Funzione GetFrameStoredLength (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameStoredLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e48f1d357645a9f50a85da4aba79d72baba4e4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315462"
---
# <a name="getframestoredlength-function"></a><span data-ttu-id="973b9-103">GetFrameStoredLength (funzione)</span><span class="sxs-lookup"><span data-stu-id="973b9-103">GetFrameStoredLength function</span></span>

<span data-ttu-id="973b9-104">La funzione **GetFrameStoredLength** restituisce la lunghezza del frame.</span><span class="sxs-lookup"><span data-stu-id="973b9-104">The **GetFrameStoredLength** function returns the length of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="973b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="973b9-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameStoredLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="973b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="973b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="973b9-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="973b9-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="973b9-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="973b9-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="973b9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="973b9-109">Return value</span></span>

<span data-ttu-id="973b9-110">Se la funzione ha esito positivo, il valore restituito è la lunghezza del frame archiviato.</span><span class="sxs-lookup"><span data-stu-id="973b9-110">If the function is successful, the return value is the length of the frame as stored.</span></span>

<span data-ttu-id="973b9-111">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="973b9-111">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="973b9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="973b9-112">Remarks</span></span>

<span data-ttu-id="973b9-113">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameStoredLength** .</span><span class="sxs-lookup"><span data-stu-id="973b9-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameStoredLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="973b9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="973b9-114">Requirements</span></span>



| <span data-ttu-id="973b9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="973b9-115">Requirement</span></span> | <span data-ttu-id="973b9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="973b9-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="973b9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="973b9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="973b9-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="973b9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="973b9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="973b9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="973b9-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="973b9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="973b9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="973b9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="973b9-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="973b9-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="973b9-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="973b9-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="973b9-124"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="973b9-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="973b9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="973b9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="973b9-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="973b9-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="973b9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="973b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="973b9-128">GetFrameLength</span><span class="sxs-lookup"><span data-stu-id="973b9-128">GetFrameLength</span></span>](getframelength.md)
</dt> </dl>

 

 




