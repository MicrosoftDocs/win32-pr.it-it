---
description: La funzione GetEnabledProtocols restituisce una tabella di tutti i protocolli contrassegnati come Enabled.
ms.assetid: 11feac64-c770-47b2-a740-fc372e97b8ed
title: Funzione GetEnabledProtocols (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetEnabledProtocols
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 284d6c87bf5a3b26d6c3f379a710966be21006d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305912"
---
# <a name="getenabledprotocols-function"></a><span data-ttu-id="180db-103">GetEnabledProtocols (funzione)</span><span class="sxs-lookup"><span data-stu-id="180db-103">GetEnabledProtocols function</span></span>

<span data-ttu-id="180db-104">La funzione **GetEnabledProtocols** restituisce una tabella di tutti i protocolli contrassegnati come Enabled.</span><span class="sxs-lookup"><span data-stu-id="180db-104">The **GetEnabledProtocols** function returns a table of all protocols that are marked Enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="180db-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="180db-105">Syntax</span></span>


```C++
LPPROTOCOLTABLE WINAPI GetEnabledProtocols(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="180db-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="180db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="180db-107">*hCapture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="180db-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="180db-108">Handle per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="180db-108">Handle to the capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="180db-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="180db-109">Return value</span></span>

<span data-ttu-id="180db-110">Se la funzione ha esito positivo, il valore restituito è un puntatore a una struttura [PROTOCOLTABLE](protocoltable.md) che elenca tutti i protocolli abilitati nell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="180db-110">If the function is successful, the return value is a pointer to a [PROTOCOLTABLE](protocoltable.md) structure that lists all the enabled protocols in the capture.</span></span>

<span data-ttu-id="180db-111">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="180db-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="180db-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="180db-112">Remarks</span></span>

<span data-ttu-id="180db-113">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetEnabledProtocols** .</span><span class="sxs-lookup"><span data-stu-id="180db-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetEnabledProtocols** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="180db-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="180db-114">Requirements</span></span>



| <span data-ttu-id="180db-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="180db-115">Requirement</span></span> | <span data-ttu-id="180db-116">Valore</span><span class="sxs-lookup"><span data-stu-id="180db-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="180db-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="180db-117">Minimum supported client</span></span><br/> | <span data-ttu-id="180db-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="180db-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="180db-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="180db-119">Minimum supported server</span></span><br/> | <span data-ttu-id="180db-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="180db-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="180db-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="180db-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="180db-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="180db-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="180db-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="180db-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="180db-124"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="180db-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="180db-125">DLL</span><span class="sxs-lookup"><span data-stu-id="180db-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="180db-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="180db-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="180db-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="180db-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="180db-128">PROTOCOLTABLE</span><span class="sxs-lookup"><span data-stu-id="180db-128">PROTOCOLTABLE</span></span>](protocoltable.md)
</dt> </dl>

 

 




