---
description: Recupera il corpo dell'entità della risposta come matrice di byte senza segno.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: 'Proprietà IWinHttpRequest:: ResponseBody'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseBody
- IWinHttpRequest.get_ResponseBody
- WinHttpRequest.ResponseBody
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5a608f2744ad2880ecf7c4862b03821afcef9630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318196"
---
# <a name="iwinhttprequestresponsebody-property"></a><span data-ttu-id="55bb1-103">Proprietà IWinHttpRequest:: ResponseBody</span><span class="sxs-lookup"><span data-stu-id="55bb1-103">IWinHttpRequest::ResponseBody property</span></span>

<span data-ttu-id="55bb1-104">La proprietà **responseBody** Recupera il corpo dell'entità della risposta come matrice di byte senza segno.</span><span class="sxs-lookup"><span data-stu-id="55bb1-104">The **ResponseBody** property retrieves the response entity body as an array of unsigned bytes.</span></span>

<span data-ttu-id="55bb1-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="55bb1-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="55bb1-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55bb1-106">Syntax</span></span>


```C++
HRESULT get_ResponseBody(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseBody = WinHttpRequest.ResponseBody
```





## <a name="property-value"></a><span data-ttu-id="55bb1-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="55bb1-107">Property value</span></span>

<span data-ttu-id="55bb1-108">Valore **Variant** che riceve il corpo dell'entità della risposta come matrice di byte senza segno.</span><span class="sxs-lookup"><span data-stu-id="55bb1-108">A **Variant** value that receives the response entity body as an array of unsigned bytes.</span></span> <span data-ttu-id="55bb1-109">Questa matrice contiene i dati non elaborati ricevuti direttamente dal server.</span><span class="sxs-lookup"><span data-stu-id="55bb1-109">This array contains the raw data as received directly from the server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="55bb1-110">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="55bb1-110">Error codes</span></span>

<span data-ttu-id="55bb1-111">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="55bb1-111">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="55bb1-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="55bb1-112">Remarks</span></span>

<span data-ttu-id="55bb1-113">Questa proprietà restituisce i dati di risposta in una matrice di byte senza segno.</span><span class="sxs-lookup"><span data-stu-id="55bb1-113">This property returns the response data in an array of unsigned bytes.</span></span> <span data-ttu-id="55bb1-114">Se la risposta non ha un corpo della risposta, viene restituita una variante vuota.</span><span class="sxs-lookup"><span data-stu-id="55bb1-114">If the response does not have a response body, an empty variant is returned.</span></span> <span data-ttu-id="55bb1-115">Questa proprietà può essere richiamata solo dopo la chiamata del metodo [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="55bb1-115">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="55bb1-116">Per ulteriori informazioni sull'implementazione per Windows XP e Windows 2000, vedere [requisiti di run-time](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="55bb1-116">For more information about implementation for Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="55bb1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55bb1-117">Requirements</span></span>



| <span data-ttu-id="55bb1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="55bb1-118">Requirement</span></span> | <span data-ttu-id="55bb1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="55bb1-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="55bb1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55bb1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="55bb1-121">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="55bb1-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="55bb1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55bb1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="55bb1-123">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="55bb1-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="55bb1-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="55bb1-124">Redistributable</span></span><br/>          | <span data-ttu-id="55bb1-125">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="55bb1-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="55bb1-126">IDL</span><span class="sxs-lookup"><span data-stu-id="55bb1-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55bb1-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="55bb1-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="55bb1-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="55bb1-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="55bb1-129"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55bb1-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="55bb1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="55bb1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55bb1-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55bb1-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="55bb1-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55bb1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55bb1-133">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="55bb1-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="55bb1-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="55bb1-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="55bb1-135">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="55bb1-135">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)
</dt> <dt>

[<span data-ttu-id="55bb1-136">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="55bb1-136">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)
</dt> <dt>

[<span data-ttu-id="55bb1-137">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="55bb1-137">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




