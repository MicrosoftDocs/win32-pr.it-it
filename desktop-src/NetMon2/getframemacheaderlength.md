---
description: La funzione GetFrameMacHeaderLength restituisce la lunghezza, in byte, dell'intestazione MAC del frame.
ms.assetid: 4a0f6a8c-04e0-47cb-abd1-b4011cd2d062
title: Funzione GetFrameMacHeaderLength (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacHeaderLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4d11a0efac2086884e984edae986720ef704cf81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305905"
---
# <a name="getframemacheaderlength-function"></a><span data-ttu-id="00ea8-103">GetFrameMacHeaderLength (funzione)</span><span class="sxs-lookup"><span data-stu-id="00ea8-103">GetFrameMacHeaderLength function</span></span>

<span data-ttu-id="00ea8-104">La funzione **GetFrameMacHeaderLength** restituisce la lunghezza, in byte, dell'intestazione MAC del frame.</span><span class="sxs-lookup"><span data-stu-id="00ea8-104">The **GetFrameMacHeaderLength** function returns the length, in bytes, of the MAC header of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="00ea8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00ea8-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameMacHeaderLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="00ea8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="00ea8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00ea8-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00ea8-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00ea8-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="00ea8-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00ea8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00ea8-109">Return value</span></span>

<span data-ttu-id="00ea8-110">Se la funzione ha esito positivo, il valore restituito è la lunghezza in byte dell'intestazione MAC.</span><span class="sxs-lookup"><span data-stu-id="00ea8-110">If the function is successful, the return value is the length   in bytes   of the MAC header.</span></span>

<span data-ttu-id="00ea8-111">Se la funzione ha esito negativo o viene rilevato un tipo MAC sconosciuto, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="00ea8-111">If the function is not successful, or an unknown MAC type is encountered, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="00ea8-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="00ea8-112">Remarks</span></span>

<span data-ttu-id="00ea8-113">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameMacHeaderLength** .</span><span class="sxs-lookup"><span data-stu-id="00ea8-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameMacHeaderLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="00ea8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00ea8-114">Requirements</span></span>



| <span data-ttu-id="00ea8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="00ea8-115">Requirement</span></span> | <span data-ttu-id="00ea8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="00ea8-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="00ea8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00ea8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="00ea8-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00ea8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="00ea8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00ea8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="00ea8-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00ea8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="00ea8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00ea8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="00ea8-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="00ea8-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="00ea8-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="00ea8-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="00ea8-124"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00ea8-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="00ea8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="00ea8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00ea8-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00ea8-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




