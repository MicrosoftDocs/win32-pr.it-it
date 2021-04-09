---
description: Si verifica in presenza di un errore di run-time nell'applicazione.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: 'Evento IWinHttpRequestEvents:: OnError'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8582deec90eb6bfc2985460f3127d5c7ee9c01b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968443"
---
# <a name="iwinhttprequesteventsonerror-event"></a><span data-ttu-id="c424d-103">Evento IWinHttpRequestEvents:: OnError</span><span class="sxs-lookup"><span data-stu-id="c424d-103">IWinHttpRequestEvents::OnError event</span></span>

<span data-ttu-id="c424d-104">L'evento **OnError** si verifica in presenza di un errore di run-time nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c424d-104">The **OnError** event occurs when there is a run-time error in the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="c424d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c424d-105">Syntax</span></span>


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a><span data-ttu-id="c424d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c424d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c424d-107">*Numero errore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c424d-107">*ErrorNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c424d-108">Riceve il valore numerico dell'errore.</span><span class="sxs-lookup"><span data-stu-id="c424d-108">Receives the numerical value of the error.</span></span> <span data-ttu-id="c424d-109">I 16 bit inferiori di questo numero di errore corrispondono a uno degli errori elencati nei [**messaggi di errore**](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="c424d-109">The lower 16 bits of this error number corresponds to one of the errors listed in [**Error Messages**](error-messages.md).</span></span>

</dd> <dt>

<span data-ttu-id="c424d-110">*ErrorDescription* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c424d-110">*ErrorDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c424d-111">Specifica una breve descrizione dell'errore che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="c424d-111">Specifies a short description of the error which occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c424d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c424d-112">Return value</span></span>

<span data-ttu-id="c424d-113">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c424d-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c424d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c424d-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c424d-115">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c424d-115">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c424d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c424d-116">Requirements</span></span>



| <span data-ttu-id="c424d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c424d-117">Requirement</span></span> | <span data-ttu-id="c424d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c424d-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c424d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c424d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c424d-120">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="c424d-120">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="c424d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c424d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c424d-122">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="c424d-122">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="c424d-123">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c424d-123">Redistributable</span></span><br/>          | <span data-ttu-id="c424d-124">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c424d-124">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="c424d-125">IDL</span><span class="sxs-lookup"><span data-stu-id="c424d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c424d-126"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c424d-126"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c424d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c424d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c424d-128">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="c424d-128">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="c424d-129">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="c424d-129">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="c424d-130">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c424d-130">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




