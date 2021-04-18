---
description: Si verifica quando i dati della risposta sono completi.
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: 'Evento IWinHttpRequestEvents:: OnResponseFinished'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d3a596e23028cec0401a21a1ee866ef6e51d9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314108"
---
# <a name="iwinhttprequesteventsonresponsefinished-event"></a><span data-ttu-id="94230-103">Evento IWinHttpRequestEvents:: OnResponseFinished</span><span class="sxs-lookup"><span data-stu-id="94230-103">IWinHttpRequestEvents::OnResponseFinished event</span></span>

<span data-ttu-id="94230-104">L'evento **OnResponseFinished** si verifica quando i dati di risposta sono completi.</span><span class="sxs-lookup"><span data-stu-id="94230-104">The **OnResponseFinished** event occurs when the response data is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="94230-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94230-105">Syntax</span></span>


```C++
void OnResponseFinished();
```



## <a name="parameters"></a><span data-ttu-id="94230-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="94230-106">Parameters</span></span>

<span data-ttu-id="94230-107">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="94230-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="94230-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94230-108">Return value</span></span>

<span data-ttu-id="94230-109">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="94230-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94230-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="94230-110">Remarks</span></span>

<span data-ttu-id="94230-111">Questo evento segnala che sono stati ricevuti tutti i dati di risposta relativi alla richiesta più recente.</span><span class="sxs-lookup"><span data-stu-id="94230-111">This event signals that all of the response data that pertains to the most recent request has been received.</span></span> <span data-ttu-id="94230-112">[**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) non si ripete fino alla richiesta successiva.</span><span class="sxs-lookup"><span data-stu-id="94230-112">[**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) does not occur again until the next request.</span></span>

> [!Note]  
> <span data-ttu-id="94230-113">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="94230-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="94230-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94230-114">Requirements</span></span>



| <span data-ttu-id="94230-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="94230-115">Requirement</span></span> | <span data-ttu-id="94230-116">Valore</span><span class="sxs-lookup"><span data-stu-id="94230-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="94230-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94230-117">Minimum supported client</span></span><br/> | <span data-ttu-id="94230-118">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="94230-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="94230-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94230-119">Minimum supported server</span></span><br/> | <span data-ttu-id="94230-120">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="94230-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="94230-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="94230-121">Redistributable</span></span><br/>          | <span data-ttu-id="94230-122">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="94230-122">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="94230-123">IDL</span><span class="sxs-lookup"><span data-stu-id="94230-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="94230-124"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="94230-124"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94230-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94230-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94230-126">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="94230-126">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="94230-127">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="94230-127">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="94230-128">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="94230-128">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




