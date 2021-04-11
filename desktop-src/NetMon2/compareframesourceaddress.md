---
description: La funzione CompareFrameSourceAddress confronta un indirizzo con l'indirizzo di origine di un frame.
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: Funzione CompareFrameSourceAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a100273c37e25a7b1deba86ed2704886dbfccc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232843"
---
# <a name="compareframesourceaddress-function"></a><span data-ttu-id="82054-103">CompareFrameSourceAddress (funzione)</span><span class="sxs-lookup"><span data-stu-id="82054-103">CompareFrameSourceAddress function</span></span>

<span data-ttu-id="82054-104">La funzione **CompareFrameSourceAddress** confronta un indirizzo con l'indirizzo di origine di un frame.</span><span class="sxs-lookup"><span data-stu-id="82054-104">The **CompareFrameSourceAddress** function compares an address to the source address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="82054-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82054-105">Syntax</span></span>


```C++
BOOL WINAPI CompareFrameSourceAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="82054-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="82054-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82054-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82054-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82054-108">Handle per un frame.</span><span class="sxs-lookup"><span data-stu-id="82054-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="82054-109">*lpAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82054-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82054-110">Puntatore a un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="82054-110">Pointer to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82054-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82054-111">Return value</span></span>

<span data-ttu-id="82054-112">Se gli indirizzi sono uguali, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="82054-112">If the addresses are the same, the return value is **TRUE**.</span></span>

<span data-ttu-id="82054-113">Se gli indirizzi non sono uguali, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="82054-113">If the addresses are not the same, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="82054-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="82054-114">Remarks</span></span>

<span data-ttu-id="82054-115">Affinché la funzione **CompareFrameSourceAddress** abbia esito positivo, il tipo di indirizzo di origine deve corrispondere al tipo di indirizzo specificato nel parametro *lpAddress* .</span><span class="sxs-lookup"><span data-stu-id="82054-115">For the **CompareFrameSourceAddress** function to succeed, the source address type must match the type of address specified in the *lpAddress* parameter.</span></span>

<span data-ttu-id="82054-116">Network Monitor offre altre due funzioni per il confronto di indirizzi: [CompareFrameDestAddress](compareframedestaddress.md) e [CompareAddresses](compareaddresses.md).</span><span class="sxs-lookup"><span data-stu-id="82054-116">Network Monitor provides two other functions for comparing addresses: [CompareFrameDestAddress](compareframedestaddress.md) and [CompareAddresses](compareaddresses.md).</span></span> <span data-ttu-id="82054-117">La funzione **CompareFrameDestAddress** confronta un determinato indirizzo con l'indirizzo di destinazione del frame e la funzione **CompareAddress** Confronta due indirizzi specificati.</span><span class="sxs-lookup"><span data-stu-id="82054-117">The **CompareFrameDestAddress** function compares a given address to the frame's destination address, and the **CompareAddress** function compares two given addresses.</span></span>

<span data-ttu-id="82054-118">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **CompareFrameSourceAddress** .</span><span class="sxs-lookup"><span data-stu-id="82054-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **CompareFrameSourceAddress** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="82054-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82054-119">Requirements</span></span>



| <span data-ttu-id="82054-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="82054-120">Requirement</span></span> | <span data-ttu-id="82054-121">Valore</span><span class="sxs-lookup"><span data-stu-id="82054-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="82054-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82054-122">Minimum supported client</span></span><br/> | <span data-ttu-id="82054-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="82054-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="82054-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82054-124">Minimum supported server</span></span><br/> | <span data-ttu-id="82054-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="82054-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="82054-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82054-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="82054-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="82054-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="82054-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="82054-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="82054-129"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82054-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="82054-130">DLL</span><span class="sxs-lookup"><span data-stu-id="82054-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82054-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82054-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82054-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82054-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82054-133">CompareAddresses</span><span class="sxs-lookup"><span data-stu-id="82054-133">CompareAddresses</span></span>](compareaddresses.md)
</dt> <dt>

[<span data-ttu-id="82054-134">CompareFrameDestAddress</span><span class="sxs-lookup"><span data-stu-id="82054-134">CompareFrameDestAddress</span></span>](compareframedestaddress.md)
</dt> </dl>

 

 




