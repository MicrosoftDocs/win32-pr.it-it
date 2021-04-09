---
description: La funzione GetFrameRecognizeData restituisce una tabella di strutture RECOGNIZEDATA. Ognuna di queste strutture contiene un identificatore di protocollo e un offset che punta all'inizio del protocollo specificato nei dati.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: Funzione GetFrameRecognizeData (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameRecognizeData
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 627ba046b3adead0291239f5d94f4e56958e6a80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966467"
---
# <a name="getframerecognizedata-function"></a><span data-ttu-id="b6bb3-104">GetFrameRecognizeData (funzione)</span><span class="sxs-lookup"><span data-stu-id="b6bb3-104">GetFrameRecognizeData function</span></span>

<span data-ttu-id="b6bb3-105">La funzione **GetFrameRecognizeData** restituisce una tabella di strutture **RECOGNIZEDATA** .</span><span class="sxs-lookup"><span data-stu-id="b6bb3-105">The **GetFrameRecognizeData** function returns a table of **RECOGNIZEDATA** structures.</span></span> <span data-ttu-id="b6bb3-106">Ognuna di queste strutture contiene un identificatore di protocollo e un offset che punta all'inizio del protocollo specificato nei dati.</span><span class="sxs-lookup"><span data-stu-id="b6bb3-106">Each of these structures contains a protocol identifier and an offset that points to the start of the specified protocol in the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6bb3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6bb3-107">Syntax</span></span>


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="b6bb3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6bb3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6bb3-109">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6bb3-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6bb3-110">Handle per un frame.</span><span class="sxs-lookup"><span data-stu-id="b6bb3-110">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6bb3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6bb3-111">Return value</span></span>

<span data-ttu-id="b6bb3-112">Se la funzione ha esito positivo, il valore restituito è un puntatore a una struttura **RECOGNIZEDATATABLE** .</span><span class="sxs-lookup"><span data-stu-id="b6bb3-112">If the function is successful, the return value is a pointer to a **RECOGNIZEDATATABLE** structure.</span></span>

<span data-ttu-id="b6bb3-113">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="b6bb3-113">If the function is not successful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6bb3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6bb3-114">Remarks</span></span>

<span data-ttu-id="b6bb3-115">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameRecognizeData** .</span><span class="sxs-lookup"><span data-stu-id="b6bb3-115">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameRecognizeData** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6bb3-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6bb3-116">Requirements</span></span>



| <span data-ttu-id="b6bb3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6bb3-117">Requirement</span></span> | <span data-ttu-id="b6bb3-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b6bb3-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b6bb3-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6bb3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b6bb3-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b6bb3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b6bb3-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6bb3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b6bb3-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b6bb3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b6bb3-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6bb3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6bb3-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6bb3-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b6bb3-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="b6bb3-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6bb3-126"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6bb3-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b6bb3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b6bb3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6bb3-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6bb3-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




