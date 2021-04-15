---
title: HTTP_RESPONSE (http. h)
description: La versione della struttura di \_ risposta HTTP dipende dalla versione della coda di richieste utilizzata come segue la coda di richieste dell'API del server http versione 1,0. si tratta di una \_ struttura di richiesta HTTP \_ V1. HTTP Server API versione 2,0 coda di richieste questa è una \_ struttura richiesta HTTP \_ v2.
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400494"
---
# <a name="http_response"></a><span data-ttu-id="a21df-106">\_risposta http</span><span class="sxs-lookup"><span data-stu-id="a21df-106">HTTP\_RESPONSE</span></span>

<span data-ttu-id="a21df-107">La versione della struttura **di \_ risposta http** dipende dalla versione della coda di richieste utilizzata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="a21df-107">The version of the **HTTP\_RESPONSE** structure is dependent on the version of the request queue used as follows:</span></span>

-   <span data-ttu-id="a21df-108">HTTP Server API versione 1,0 coda richieste: si tratta di una struttura [**\_ richiesta HTTP \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) .</span><span class="sxs-lookup"><span data-stu-id="a21df-108">HTTP Server API Version 1.0 request queue: This is an [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) structure.</span></span>
-   <span data-ttu-id="a21df-109">HTTP Server API versione 2,0 coda richieste: si tratta di una struttura [**\_ richiesta HTTP \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) .</span><span class="sxs-lookup"><span data-stu-id="a21df-109">HTTP Server API Version 2.0 request queue: This is an [**HTTP\_REQUEST\_V2**](/windows/desktop/api/Http/ns-http-http_request_v2) structure.</span></span>

<span data-ttu-id="a21df-110">Non usare la [**\_ richiesta HTTP \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) e [**la \_ richiesta HTTP \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) direttamente nel codice. l'uso della **\_ risposta http** garantisce invece la corretta versione della struttura in base alla versione della coda di richieste.</span><span class="sxs-lookup"><span data-stu-id="a21df-110">Do not use [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) and [**HTTP\_REQUEST\_V2**](/windows/desktop/api/Http/ns-http-http_request_v2) directly in your code; using **HTTP\_RESPONSE** instead ensures the proper version of the structure is used based on the version of the request queue.</span></span>


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

<span data-ttu-id="a21df-111">**\_risposta http**</span><span class="sxs-lookup"><span data-stu-id="a21df-111">**HTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="a21df-112">Richiesta proveniva da una coda di richieste V1.</span><span class="sxs-lookup"><span data-stu-id="a21df-112">Request was from a v1 request queue.</span></span>

</dd> <dt>

<span data-ttu-id="a21df-113">**\_risposta http**</span><span class="sxs-lookup"><span data-stu-id="a21df-113">**HTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="a21df-114">Richiesta proveniva da una coda di richieste V2.</span><span class="sxs-lookup"><span data-stu-id="a21df-114">Request was from a v2 request queue.</span></span>

</dd> <dt>

<span data-ttu-id="a21df-115">**\_risposta PHTTP**</span><span class="sxs-lookup"><span data-stu-id="a21df-115">**PHTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="a21df-116">Puntatore a una struttura di **\_ risposta http** .</span><span class="sxs-lookup"><span data-stu-id="a21df-116">Pointer to an **HTTP\_RESPONSE** structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a21df-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a21df-117">Requirements</span></span>



| <span data-ttu-id="a21df-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a21df-118">Requirement</span></span> | <span data-ttu-id="a21df-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a21df-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a21df-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a21df-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a21df-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a21df-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a21df-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a21df-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a21df-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a21df-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a21df-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a21df-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a21df-125"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="a21df-125"><dt>Http.h</dt></span></span> </dl> |



 

 





