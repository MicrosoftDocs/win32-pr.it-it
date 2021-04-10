---
description: Il metodo Abort interrompe un metodo di invio WinHTTP.
ms.assetid: 8326feef-8611-4441-b52d-74855e6acfff
title: 'Metodo IWinHttpRequest:: Abort'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Abort
- WinHttpRequest.Abort
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56290dfc16f9986cb7d7596c098bb53c207efebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968284"
---
# <a name="iwinhttprequestabort-method"></a><span data-ttu-id="e1b24-103">Metodo IWinHttpRequest:: Abort</span><span class="sxs-lookup"><span data-stu-id="e1b24-103">IWinHttpRequest::Abort method</span></span>

<span data-ttu-id="e1b24-104">Il metodo **Abort** interrompe un metodo di [**invio**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="e1b24-104">The **Abort** method aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b24-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1b24-105">Syntax</span></span>


```C++
HRESULT Abort();
```



## <a name="parameters"></a><span data-ttu-id="e1b24-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1b24-106">Parameters</span></span>

<span data-ttu-id="e1b24-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e1b24-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1b24-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1b24-108">Return value</span></span>

<span data-ttu-id="e1b24-109">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="e1b24-109">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1b24-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1b24-110">Remarks</span></span>

<span data-ttu-id="e1b24-111">È possibile interrompere i metodi di [**invio**](iwinhttprequest-send.md) sincroni e asincroni.</span><span class="sxs-lookup"><span data-stu-id="e1b24-111">You can abort both asynchronous and synchronous [**Send**](iwinhttprequest-send.md) methods.</span></span> <span data-ttu-id="e1b24-112">Per interrompere un metodo di [**invio**](iwinhttprequest-send.md) sincrono, è necessario chiamare **Abort** dall'interno di un evento [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="e1b24-112">To abort a synchronous [**Send**](iwinhttprequest-send.md) method, you must call **Abort** from within an [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) event.</span></span>

> [!Note]  
> <span data-ttu-id="e1b24-113">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="e1b24-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e1b24-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1b24-114">Requirements</span></span>



| <span data-ttu-id="e1b24-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1b24-115">Requirement</span></span> | <span data-ttu-id="e1b24-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e1b24-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b24-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1b24-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b24-118">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="e1b24-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="e1b24-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1b24-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b24-120">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="e1b24-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="e1b24-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e1b24-121">Redistributable</span></span><br/>          | <span data-ttu-id="e1b24-122">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e1b24-122">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="e1b24-123">IDL</span><span class="sxs-lookup"><span data-stu-id="e1b24-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e1b24-124"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e1b24-124"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="e1b24-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="e1b24-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="e1b24-126"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1b24-126"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="e1b24-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e1b24-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1b24-128"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1b24-128"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e1b24-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1b24-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b24-130">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="e1b24-130">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="e1b24-131">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="e1b24-131">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="e1b24-132">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="e1b24-132">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




