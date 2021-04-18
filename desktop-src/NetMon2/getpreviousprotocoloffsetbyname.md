---
description: La funzione GetPreviousProtocolOffsetByName restituisce l'istanza precedente di un protocollo specificato.
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: Funzione GetPreviousProtocolOffsetByName (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPreviousProtocolOffsetByName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2720d309224def5f368babf4f9ace85955907347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305900"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a><span data-ttu-id="fc735-103">GetPreviousProtocolOffsetByName (funzione)</span><span class="sxs-lookup"><span data-stu-id="fc735-103">GetPreviousProtocolOffsetByName function</span></span>

<span data-ttu-id="fc735-104">La funzione **GetPreviousProtocolOffsetByName** restituisce l'istanza precedente di un protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="fc735-104">The **GetPreviousProtocolOffsetByName** function returns the previous instance of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc735-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc735-105">Syntax</span></span>


```C++
DWORD WINAPI GetPreviousProtocolOffsetByName(
  _In_  HFRAME hFrame,
  _In_  DWORD  dwStartOffset,
  _In_  LPSTR  szProtocolName,
  _Out_ DWORD  *pdwPreviousOffset
);
```



## <a name="parameters"></a><span data-ttu-id="fc735-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc735-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc735-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc735-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc735-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="fc735-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="fc735-109">*dwStartOffset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc735-109">*dwStartOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc735-110">Offset nel frame.</span><span class="sxs-lookup"><span data-stu-id="fc735-110">Offset in the frame.</span></span>

</dd> <dt>

<span data-ttu-id="fc735-111">*szProtocolName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc735-111">*szProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc735-112">Nome del protocollo che si desidera cercare.</span><span class="sxs-lookup"><span data-stu-id="fc735-112">Name of the protocol you want to search for.</span></span>

</dd> <dt>

<span data-ttu-id="fc735-113">*pdwPreviousOffset* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fc735-113">*pdwPreviousOffset* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc735-114">Puntatore a un **valore DWORD** che contiene l'offset al protocollo precedente (se la funzione ha esito positivo).</span><span class="sxs-lookup"><span data-stu-id="fc735-114">Pointer to a **DWORD** that contains the offset to the previous protocol (if the function succeeds).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc735-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc735-115">Return value</span></span>

<span data-ttu-id="fc735-116">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="fc735-116">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="fc735-117">Se la funzione ha esito negativo, il valore restituito è il \_ protocollo NMERR \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="fc735-117">If the function is unsuccessful, the return value is NMERR\_PROTOCOL\_NOT\_FOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc735-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc735-118">Remarks</span></span>

<span data-ttu-id="fc735-119">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare **GetPreviousProtocolOffsetByName**.</span><span class="sxs-lookup"><span data-stu-id="fc735-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPreviousProtocolOffsetByName**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc735-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc735-120">Requirements</span></span>



| <span data-ttu-id="fc735-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc735-121">Requirement</span></span> | <span data-ttu-id="fc735-122">Valore</span><span class="sxs-lookup"><span data-stu-id="fc735-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fc735-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc735-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fc735-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fc735-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fc735-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc735-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fc735-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fc735-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fc735-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc735-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc735-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc735-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="fc735-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="fc735-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc735-130"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc735-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="fc735-131">DLL</span><span class="sxs-lookup"><span data-stu-id="fc735-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc735-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc735-132"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




