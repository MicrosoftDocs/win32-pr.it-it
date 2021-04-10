---
description: Schemi Internet supportati da WinHTTP.
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: INTERNET_SCHEME (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7b73dcc13b2623e3a6f28d2d49d1965464070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884437"
---
# <a name="internet_scheme"></a><span data-ttu-id="c77dc-103">\_schema Internet</span><span class="sxs-lookup"><span data-stu-id="c77dc-103">INTERNET\_SCHEME</span></span>

<span data-ttu-id="c77dc-104">Schemi Internet supportati da WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c77dc-104">Internet schemes supported by WinHTTP.</span></span>

<dl> <dt>

<span data-ttu-id="c77dc-105"><span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**INTERNET \_ schema \_ http**</span><span class="sxs-lookup"><span data-stu-id="c77dc-105"><span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**INTERNET\_SCHEME\_HTTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c77dc-106">1</span><span class="sxs-lookup"><span data-stu-id="c77dc-106">1</span></span>
</dt> <dt>



<span data-ttu-id="c77dc-107">Uno schema Internet HTTP.</span><span class="sxs-lookup"><span data-stu-id="c77dc-107">An HTTP internet scheme.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c77dc-108"><span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**INTERNET \_ Scheme \_ https**</span><span class="sxs-lookup"><span data-stu-id="c77dc-108"><span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**INTERNET\_SCHEME\_HTTPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c77dc-109">2</span><span class="sxs-lookup"><span data-stu-id="c77dc-109">2</span></span>
</dt> <dt>



<span data-ttu-id="c77dc-110">Schema Internet HTTPS (SSL).</span><span class="sxs-lookup"><span data-stu-id="c77dc-110">An HTTPS (SSL) internet scheme.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c77dc-111"><span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**INTERNET \_ Scheme \_ FTP**</span><span class="sxs-lookup"><span data-stu-id="c77dc-111"><span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**INTERNET\_SCHEME\_FTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c77dc-112">3</span><span class="sxs-lookup"><span data-stu-id="c77dc-112">3</span></span>
</dt> <dt>



<span data-ttu-id="c77dc-113">Uno schema Internet FTP.</span><span class="sxs-lookup"><span data-stu-id="c77dc-113">An FTP internet scheme.</span></span> <span data-ttu-id="c77dc-114">Questo schema è supportato solo per l'uso in [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) e [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="c77dc-114">This scheme is only supported for use in [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) and [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c77dc-115"><span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**INTERNET \_ Scheme \_ Socks**</span><span class="sxs-lookup"><span data-stu-id="c77dc-115"><span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**INTERNET\_SCHEME\_SOCKS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c77dc-116">4</span><span class="sxs-lookup"><span data-stu-id="c77dc-116">4</span></span>
</dt> <dt>



<span data-ttu-id="c77dc-117">Uno schema SOCKS Internet.</span><span class="sxs-lookup"><span data-stu-id="c77dc-117">A SOCKS internet scheme.</span></span> <span data-ttu-id="c77dc-118">Questo schema è supportato solo per l'utilizzo [**nella \_ \_ \_ voce dei risultati del proxy WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).</span><span class="sxs-lookup"><span data-stu-id="c77dc-118">This scheme is only supported for use in [**WINHTTP\_PROXY\_RESULT\_ENTRY**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c77dc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c77dc-119">Requirements</span></span>



| <span data-ttu-id="c77dc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c77dc-120">Requirement</span></span> | <span data-ttu-id="c77dc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c77dc-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c77dc-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c77dc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c77dc-123">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="c77dc-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="c77dc-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c77dc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c77dc-125">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="c77dc-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="c77dc-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c77dc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c77dc-127"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="c77dc-127"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c77dc-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c77dc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c77dc-129">**\_voce di \_ risultato del proxy WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="c77dc-129">**WINHTTP\_PROXY\_RESULT\_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 




