---
description: La funzione CompareAddresses Confronta due indirizzi, a indicare che uno degli indirizzi è maggiore di, minore o uguale all'altro indirizzo.
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: Funzione CompareAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fd72ef0281615c0b56176e86ee9bb3659b498a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314179"
---
# <a name="compareaddresses-function"></a><span data-ttu-id="00a88-103">CompareAddresses (funzione)</span><span class="sxs-lookup"><span data-stu-id="00a88-103">CompareAddresses function</span></span>

<span data-ttu-id="00a88-104">La funzione **CompareAddresses** Confronta due indirizzi, a indicare che uno degli indirizzi è maggiore di, minore o uguale all'altro indirizzo.</span><span class="sxs-lookup"><span data-stu-id="00a88-104">The **CompareAddresses** function compares two addresses, indicating that one of the addresses is greater than, less than, or equal to the other address.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a88-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00a88-105">Syntax</span></span>


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a><span data-ttu-id="00a88-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="00a88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00a88-107">*lpAddress1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00a88-107">*lpAddress1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00a88-108">Puntatore al primo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="00a88-108">Pointer to the first address.</span></span>

</dd> <dt>

<span data-ttu-id="00a88-109">*lpAddress2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00a88-109">*lpAddress2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00a88-110">Puntatore al secondo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="00a88-110">Pointer to the second address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00a88-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00a88-111">Return value</span></span>

<span data-ttu-id="00a88-112">Se gli indirizzi sono uguali, la funzione restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="00a88-112">If the addresses are the same, the function returns zero.</span></span>

<span data-ttu-id="00a88-113">Se il parametro *lpAddress1* specifica un indirizzo minore dell'indirizzo specificato dal parametro *lpAddress2* , il valore restituito è un numero negativo.</span><span class="sxs-lookup"><span data-stu-id="00a88-113">If the *lpAddress1* parameter specifies an address that is less than the address that the *lpAddress2* parameter specifies, the return value is a negative number.</span></span>

<span data-ttu-id="00a88-114">Se il parametro *lpAddress1* specifica un indirizzo maggiore dell'indirizzo specificato dal parametro *lpAddress2* , il valore restituito è un numero positivo.</span><span class="sxs-lookup"><span data-stu-id="00a88-114">If the *lpAddress1* parameter specifies an address that is greater than the address that the *lpAddress2* parameter specifies, the return value is a positive number.</span></span>

## <a name="remarks"></a><span data-ttu-id="00a88-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="00a88-115">Remarks</span></span>

<span data-ttu-id="00a88-116">Un indirizzo minore di un altro indirizzo indica un frame precedente.</span><span class="sxs-lookup"><span data-stu-id="00a88-116">An address that is less than another address indicates a previous frame.</span></span> <span data-ttu-id="00a88-117">Un indirizzo maggiore di un altro indirizzo indica un frame successivo.</span><span class="sxs-lookup"><span data-stu-id="00a88-117">An address that is greater than another address indicates a later frame.</span></span>

<span data-ttu-id="00a88-118">In Network Monitor sono disponibili altre due funzioni, [CompareFrameDestAddress](compareframedestaddress.md) e [CompareFrameSourceAddress](compareframesourceaddress.md), che è possibile utilizzare per confrontare gli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="00a88-118">Network Monitor provides two other functions, [CompareFrameDestAddress](compareframedestaddress.md) and [CompareFrameSourceAddress](compareframesourceaddress.md), which you can use to compare addresses.</span></span> <span data-ttu-id="00a88-119">La funzione **CompareFrameDestAddress** confronta un determinato indirizzo con l'indirizzo di destinazione del frame e la funzione **CompareFrameSourceAddress** confronta un determinato indirizzo con l'indirizzo di origine del frame.</span><span class="sxs-lookup"><span data-stu-id="00a88-119">The **CompareFrameDestAddress** function compares a given address to the frame's destination address, and the **CompareFrameSourceAddress** function compares a given address to the frame's source address.</span></span>

## <a name="requirements"></a><span data-ttu-id="00a88-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00a88-120">Requirements</span></span>



| <span data-ttu-id="00a88-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="00a88-121">Requirement</span></span> | <span data-ttu-id="00a88-122">Valore</span><span class="sxs-lookup"><span data-stu-id="00a88-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="00a88-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00a88-123">Minimum supported client</span></span><br/> | <span data-ttu-id="00a88-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00a88-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="00a88-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00a88-125">Minimum supported server</span></span><br/> | <span data-ttu-id="00a88-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00a88-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="00a88-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00a88-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="00a88-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="00a88-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="00a88-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="00a88-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="00a88-130"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00a88-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="00a88-131">DLL</span><span class="sxs-lookup"><span data-stu-id="00a88-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00a88-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00a88-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00a88-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00a88-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a88-134">CompareFrameDestAddress</span><span class="sxs-lookup"><span data-stu-id="00a88-134">CompareFrameDestAddress</span></span>](compareframedestaddress.md)
</dt> <dt>

[<span data-ttu-id="00a88-135">CompareFrameSourceAddress</span><span class="sxs-lookup"><span data-stu-id="00a88-135">CompareFrameSourceAddress</span></span>](compareframesourceaddress.md)
</dt> </dl>

 

 




