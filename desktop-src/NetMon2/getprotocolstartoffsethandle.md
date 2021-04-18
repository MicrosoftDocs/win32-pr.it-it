---
description: La funzione GetProtocolStartOffsetHandle restituisce l'offset del frame di un protocollo specificato.
ms.assetid: b1e3a03b-f211-4c2c-8810-9e220c40136b
title: Funzione GetProtocolStartOffsetHandle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffsetHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: bac8a10e2a0d8be667f1448c523f208c0c3e1512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305894"
---
# <a name="getprotocolstartoffsethandle-function"></a><span data-ttu-id="14ba4-103">GetProtocolStartOffsetHandle (funzione)</span><span class="sxs-lookup"><span data-stu-id="14ba4-103">GetProtocolStartOffsetHandle function</span></span>

<span data-ttu-id="14ba4-104">La funzione **GetProtocolStartOffsetHandle** restituisce l'offset del frame di un protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="14ba4-104">The **GetProtocolStartOffsetHandle** function returns the frame offset of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ba4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14ba4-105">Syntax</span></span>


```C++
DWORD WINAPI GetProtocolStartOffsetHandle(
  _In_ HFRAME    hFrame,
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="14ba4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="14ba4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14ba4-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14ba4-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14ba4-108">Handle per un frame.</span><span class="sxs-lookup"><span data-stu-id="14ba4-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="14ba4-109">*hProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14ba4-109">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14ba4-110">Handle per un protocollo.</span><span class="sxs-lookup"><span data-stu-id="14ba4-110">Handle to a protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14ba4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14ba4-111">Return value</span></span>

<span data-ttu-id="14ba4-112">Se la funzione ha esito positivo, il valore restituito è l'offset del frame misurato in byte.</span><span class="sxs-lookup"><span data-stu-id="14ba4-112">If the function is successful, the return value is the offset of the frame   measured in bytes.</span></span>

<span data-ttu-id="14ba4-113">Se la funzione ha esito negativo, il valore restituito è uno (1).</span><span class="sxs-lookup"><span data-stu-id="14ba4-113">If the function is unsuccessful, the return value is one (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="14ba4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="14ba4-114">Remarks</span></span>

<span data-ttu-id="14ba4-115">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetProtocolStartOffsetHandle** .</span><span class="sxs-lookup"><span data-stu-id="14ba4-115">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolStartOffsetHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="14ba4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14ba4-116">Requirements</span></span>



| <span data-ttu-id="14ba4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="14ba4-117">Requirement</span></span> | <span data-ttu-id="14ba4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="14ba4-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="14ba4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14ba4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="14ba4-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="14ba4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="14ba4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14ba4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="14ba4-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="14ba4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="14ba4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14ba4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="14ba4-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="14ba4-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="14ba4-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="14ba4-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="14ba4-126"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14ba4-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="14ba4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="14ba4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14ba4-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14ba4-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




