---
description: La funzione CompareFrameDestAddress confronta un indirizzo con l'indirizzo di destinazione di un frame.
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: Funzione CompareFrameDestAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: a9ce0ff776588c06b8fddc34240e9c2170ceca69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881441"
---
# <a name="compareframedestaddress-function"></a><span data-ttu-id="f7e33-103">CompareFrameDestAddress (funzione)</span><span class="sxs-lookup"><span data-stu-id="f7e33-103">CompareFrameDestAddress function</span></span>

<span data-ttu-id="f7e33-104">La funzione **CompareFrameDestAddress** confronta un indirizzo con l'indirizzo di destinazione di un frame.</span><span class="sxs-lookup"><span data-stu-id="f7e33-104">The **CompareFrameDestAddress** function compares an address to the destination address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7e33-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7e33-105">Syntax</span></span>


```C++
BOOL WINAPI CompareFrameDestAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="f7e33-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7e33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7e33-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7e33-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7e33-108">Handle per un frame.</span><span class="sxs-lookup"><span data-stu-id="f7e33-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="f7e33-109">*lpAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7e33-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7e33-110">Puntatore a un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="f7e33-110">Pointer to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7e33-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7e33-111">Return value</span></span>

<span data-ttu-id="f7e33-112">Se gli indirizzi sono uguali, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="f7e33-112">If the addresses are the same, the return value is **TRUE**.</span></span>

<span data-ttu-id="f7e33-113">Se gli indirizzi non sono uguali, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="f7e33-113">If the addresses are not the same, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7e33-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7e33-114">Remarks</span></span>

<span data-ttu-id="f7e33-115">Affinché la funzione **CompareFrameDestAddress** venga restituita correttamente, il tipo di indirizzo di destinazione deve corrispondere al tipo di indirizzo specificato nel parametro *lpAddress* .</span><span class="sxs-lookup"><span data-stu-id="f7e33-115">For the **CompareFrameDestAddress** function to return successfully, the destination address type must match the type of address specified in the *lpAddress* parameter.</span></span>

<span data-ttu-id="f7e33-116">In Network Monitor sono disponibili altre due funzioni, [CompareFrameSourceAddress](compareframesourceaddress.md) e [CompareAddresses](compareaddresses.md), che è possibile utilizzare per confrontare gli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="f7e33-116">Network Monitor provides two other functions, [CompareFrameSourceAddress](compareframesourceaddress.md) and [CompareAddresses](compareaddresses.md), which you can use to compare addresses.</span></span> <span data-ttu-id="f7e33-117">La funzione **CompareFrameSourceAddress** confronta un determinato indirizzo con l'indirizzo di origine del frame e la funzione **CompareAddress** Confronta due indirizzi specificati.</span><span class="sxs-lookup"><span data-stu-id="f7e33-117">The **CompareFrameSourceAddress** function compares a given address to the frame's source address, and the **CompareAddress** function compares two given addresses.</span></span>

<span data-ttu-id="f7e33-118">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **CompareFrameDestAddress** .</span><span class="sxs-lookup"><span data-stu-id="f7e33-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **CompareFrameDestAddress** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7e33-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7e33-119">Requirements</span></span>



| <span data-ttu-id="f7e33-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7e33-120">Requirement</span></span> | <span data-ttu-id="f7e33-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f7e33-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7e33-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7e33-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f7e33-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7e33-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f7e33-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7e33-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f7e33-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7e33-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f7e33-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7e33-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7e33-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7e33-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f7e33-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="f7e33-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="f7e33-129"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7e33-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f7e33-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f7e33-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7e33-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7e33-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7e33-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7e33-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7e33-133">CompareAddresses</span><span class="sxs-lookup"><span data-stu-id="f7e33-133">CompareAddresses</span></span>](compareaddresses.md)
</dt> <dt>

[<span data-ttu-id="f7e33-134">CompareFrameSourceAddress</span><span class="sxs-lookup"><span data-stu-id="f7e33-134">CompareFrameSourceAddress</span></span>](compareframesourceaddress.md)
</dt> </dl>

 

 




