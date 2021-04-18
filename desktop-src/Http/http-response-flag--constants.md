---
title: Costanti HTTP_RESPONSE_FLAG_ (http. h)
description: Definire le opzioni per configurare le risposte nell'API del server HTTP.
ms.assetid: bcb59457-fd22-4166-8a72-ba85209ec8c7
topic_type:
- apiref
api_name:
- HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96b7c34d453c1b9bbe45cf2c85ad268b414f3439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301378"
---
# <a name="http_response_flag_-constants"></a><span data-ttu-id="79ad8-103">\_Costanti del \_ flag di risposta http \_</span><span class="sxs-lookup"><span data-stu-id="79ad8-103">HTTP\_RESPONSE\_FLAG\_ Constants</span></span>

<span data-ttu-id="79ad8-104">Le costanti del **\_ \_ flag \_ di risposta http** definiscono le opzioni per la configurazione delle risposte nell'API del server http.</span><span class="sxs-lookup"><span data-stu-id="79ad8-104">The **HTTP\_RESPONSE\_FLAG\_** constants define options to configure responses in the HTTP Server API.</span></span>

<span data-ttu-id="79ad8-105">Queste costanti vengono usate nel membro dei **flag** della struttura della [**\_ risposta http \_ V1**](/windows/desktop/api/Http/ns-http-http_response_v1) .</span><span class="sxs-lookup"><span data-stu-id="79ad8-105">These constants are used in the **Flags** member of the [**HTTP\_RESPONSE\_V1**](/windows/desktop/api/Http/ns-http-http_response_v1) structure.</span></span>

<dl> <dt>

<span data-ttu-id="79ad8-106"><span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**\_flag di risposta http \_ \_ più \_ codifiche \_ disponibili**</span><span class="sxs-lookup"><span data-stu-id="79ad8-106"><span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**HTTP\_RESPONSE\_FLAG\_MULTIPLE\_ENCODINGS\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="79ad8-107">Per questa risorsa sono disponibili codifiche diverse dal formato Identity.</span><span class="sxs-lookup"><span data-stu-id="79ad8-107">Encodings other than identity form are available for this resource.</span></span> <span data-ttu-id="79ad8-108">Questo flag viene ignorato se all'applicazione non è stata richiesta la memorizzazione della risposta nella cache.</span><span class="sxs-lookup"><span data-stu-id="79ad8-108">This flag is ignored if the application has not asked for the response to be cached.</span></span> <span data-ttu-id="79ad8-109">Viene usato come suggerimento per l'API del server HTTP per la negoziazione del contenuto quando serve dalla cache di risposta del kernel.</span><span class="sxs-lookup"><span data-stu-id="79ad8-109">It's used as a hint to the HTTP Server API for content negotiation when serving from the kernel response cache.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79ad8-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79ad8-110">Requirements</span></span>



| <span data-ttu-id="79ad8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="79ad8-111">Requirement</span></span> | <span data-ttu-id="79ad8-112">Valore</span><span class="sxs-lookup"><span data-stu-id="79ad8-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="79ad8-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79ad8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="79ad8-114">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="79ad8-114">Windows 7 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79ad8-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79ad8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="79ad8-116">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="79ad8-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="79ad8-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79ad8-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="79ad8-118"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="79ad8-118"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79ad8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79ad8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79ad8-120">Costanti API server HTTP versione 2,0</span><span class="sxs-lookup"><span data-stu-id="79ad8-120">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="79ad8-121">**\_Risposta http \_ V1**</span><span class="sxs-lookup"><span data-stu-id="79ad8-121">**HTTP\_RESPONSE\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 





