---
description: Si verifica quando i dati di risposta iniziano a essere ricevuti.
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: 'Evento IWinHttpRequestEvents:: OnResponseStart'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a299c535dd854bff07f2c24989096f7b9e49fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314105"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a><span data-ttu-id="e78df-103">Evento IWinHttpRequestEvents:: OnResponseStart</span><span class="sxs-lookup"><span data-stu-id="e78df-103">IWinHttpRequestEvents::OnResponseStart event</span></span>

<span data-ttu-id="e78df-104">L'evento **OnResponseStart** si verifica quando i dati di risposta iniziano a essere ricevuti.</span><span class="sxs-lookup"><span data-stu-id="e78df-104">The **OnResponseStart** event occurs when the response data starts to be received.</span></span>

## <a name="syntax"></a><span data-ttu-id="e78df-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e78df-105">Syntax</span></span>


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a><span data-ttu-id="e78df-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e78df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e78df-107">*Stato* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="e78df-107">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e78df-108">Riceve il codice di stato standard restituito con i dati di risposta.</span><span class="sxs-lookup"><span data-stu-id="e78df-108">Receives the standard status code returned with the response data.</span></span> <span data-ttu-id="e78df-109">I codici di stato sono definiti nella [specifica RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="e78df-109">Status codes are defined in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="e78df-110">*ContentType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e78df-110">*ContentType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e78df-111">Specifica il tipo di contenuto ricevuto, ad esempio "text/html" o "image/gif".</span><span class="sxs-lookup"><span data-stu-id="e78df-111">Specifies the type of content received, such as "text/html" or "image/gif".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e78df-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e78df-112">Return value</span></span>

<span data-ttu-id="e78df-113">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e78df-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e78df-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e78df-114">Remarks</span></span>

<span data-ttu-id="e78df-115">Per questo evento, utilizzare [**Open**](iwinhttprequest-open.md) per inviare una connessione HTTP in modalità asincrona e utilizzare [**Send**](iwinhttprequest-send.md) per inviare una richiesta di dati a un server Internet.</span><span class="sxs-lookup"><span data-stu-id="e78df-115">For this event to occur, use [**Open**](iwinhttprequest-open.md) to send an HTTP connection in asynchronous mode and use [**Send**](iwinhttprequest-send.md) to send a data request to an Internet server.</span></span>

<span data-ttu-id="e78df-116">Questo è il primo evento WinHTTP che si verifica dopo l' [**invio**](iwinhttprequest-send.md).</span><span class="sxs-lookup"><span data-stu-id="e78df-116">This is the first WinHTTP event to occur after the [**Send**](iwinhttprequest-send.md).</span></span>

> [!Note]  
> <span data-ttu-id="e78df-117">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="e78df-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e78df-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e78df-118">Requirements</span></span>



| <span data-ttu-id="e78df-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e78df-119">Requirement</span></span> | <span data-ttu-id="e78df-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e78df-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e78df-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e78df-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e78df-122">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="e78df-122">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="e78df-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e78df-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e78df-124">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="e78df-124">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="e78df-125">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e78df-125">Redistributable</span></span><br/>          | <span data-ttu-id="e78df-126">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e78df-126">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="e78df-127">IDL</span><span class="sxs-lookup"><span data-stu-id="e78df-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e78df-128"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e78df-128"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e78df-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e78df-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e78df-130">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="e78df-130">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="e78df-131">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="e78df-131">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="e78df-132">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="e78df-132">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




