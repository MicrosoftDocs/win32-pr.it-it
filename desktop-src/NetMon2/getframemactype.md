---
description: La funzione GetFrameMacType restituisce il tipo MAC del frame.
ms.assetid: 8d3da770-1392-4638-a267-32c2dae289b0
title: Funzione GetFrameMacType (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b85accc64a6e29424e3f65d070bafcf29bb3ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966469"
---
# <a name="getframemactype-function"></a><span data-ttu-id="f2dd5-103">GetFrameMacType (funzione)</span><span class="sxs-lookup"><span data-stu-id="f2dd5-103">GetFrameMacType function</span></span>

<span data-ttu-id="f2dd5-104">La funzione **GetFrameMacType** restituisce il tipo Mac del frame.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-104">The **GetFrameMacType** function returns the MAC type of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2dd5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2dd5-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameMacType(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="f2dd5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2dd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2dd5-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2dd5-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2dd5-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2dd5-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2dd5-109">Return value</span></span>

<span data-ttu-id="f2dd5-110">La funzione restituisce il tipo MAC del frame, che può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-110">The function returns the MAC type of the frame, which can have one of the following values.</span></span>

-   <span data-ttu-id="f2dd5-111">\_tipo Mac \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="f2dd5-111">MAC\_TYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="f2dd5-112">\_Ethernet di tipo Mac \_</span><span class="sxs-lookup"><span data-stu-id="f2dd5-112">MAC\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="f2dd5-113">\_Tokenring di tipo Mac \_</span><span class="sxs-lookup"><span data-stu-id="f2dd5-113">MAC\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="f2dd5-114">\_FDDI di tipo Mac \_</span><span class="sxs-lookup"><span data-stu-id="f2dd5-114">MAC\_TYPE\_FDDI</span></span>

## <a name="remarks"></a><span data-ttu-id="f2dd5-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2dd5-115">Remarks</span></span>

<span data-ttu-id="f2dd5-116">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameMacType** .</span><span class="sxs-lookup"><span data-stu-id="f2dd5-116">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameMacType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2dd5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2dd5-117">Requirements</span></span>



| <span data-ttu-id="f2dd5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2dd5-118">Requirement</span></span> | <span data-ttu-id="f2dd5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f2dd5-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f2dd5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2dd5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f2dd5-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f2dd5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f2dd5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2dd5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f2dd5-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f2dd5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f2dd5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2dd5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2dd5-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2dd5-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f2dd5-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="f2dd5-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2dd5-127"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2dd5-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f2dd5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f2dd5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2dd5-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2dd5-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




