---
description: La funzione GetCaptureTimeStamp restituisce l'ora e la data di inizio della registrazione dei frame dall'acquisizione.
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: Funzione GetCaptureTimeStamp (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 855aa8b5432fd06bb25571fcb48c091dcfe502f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525140"
---
# <a name="getcapturetimestamp-function"></a><span data-ttu-id="d48b4-103">GetCaptureTimeStamp (funzione)</span><span class="sxs-lookup"><span data-stu-id="d48b4-103">GetCaptureTimeStamp function</span></span>

<span data-ttu-id="d48b4-104">La funzione **GetCaptureTimeStamp** restituisce l'ora e la data di inizio della registrazione dei frame dall'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d48b4-104">The **GetCaptureTimeStamp** function returns the time and date when the capture started recording frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="d48b4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d48b4-105">Syntax</span></span>


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="d48b4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d48b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d48b4-107">*hCapture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d48b4-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d48b4-108">Handle per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d48b4-108">Handle to the capture.</span></span> <span data-ttu-id="d48b4-109">Per informazioni sull'acquisizione dell'handle di acquisizione, vedere la sezione Osservazioni di questo argomento **GetCaptureTimeStamp** .</span><span class="sxs-lookup"><span data-stu-id="d48b4-109">For information about obtaining the capture handle, see the Remarks section of this **GetCaptureTimeStamp** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d48b4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d48b4-110">Return value</span></span>

<span data-ttu-id="d48b4-111">Se la funzione ha esito positivo, il valore restituito è un puntatore a una struttura [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="d48b4-111">If the function is successful, the return value is a pointer to a [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

<span data-ttu-id="d48b4-112">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d48b4-112">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d48b4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d48b4-113">Remarks</span></span>

<span data-ttu-id="d48b4-114">La funzione **GetCaptureTimeStamp** restituisce l'ora in cui il provider di pacchetti di rete (NPP) inizia a raccogliere i dati, non quando l'esperto carica l'acquisizione per l'analisi.</span><span class="sxs-lookup"><span data-stu-id="d48b4-114">The **GetCaptureTimeStamp** function returns the time when the Network Packet Provider (NPP) starts collecting data, not when the expert loads the capture for analysis.</span></span>

<span data-ttu-id="d48b4-115">Non sovrascrivere i dati nella struttura **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="d48b4-115">Do not overwrite the data in the **SYSTEMTIME** structure.</span></span> <span data-ttu-id="d48b4-116">I dati fanno parte dell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d48b4-116">The data is part of the capture.</span></span> <span data-ttu-id="d48b4-117">Il tentativo di modificare i dati causa una violazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="d48b4-117">Trying to modify the data causes an access violation.</span></span>

<span data-ttu-id="d48b4-118">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetCaptureTimeStamp** .</span><span class="sxs-lookup"><span data-stu-id="d48b4-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureTimeStamp** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d48b4-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d48b4-119">Requirements</span></span>



| <span data-ttu-id="d48b4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d48b4-120">Requirement</span></span> | <span data-ttu-id="d48b4-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d48b4-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d48b4-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d48b4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d48b4-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d48b4-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d48b4-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d48b4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d48b4-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d48b4-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d48b4-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d48b4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d48b4-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d48b4-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d48b4-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="d48b4-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d48b4-129"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d48b4-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d48b4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d48b4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d48b4-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d48b4-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d48b4-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d48b4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48b4-133">SYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="d48b4-133">SYSTEMTIME</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

