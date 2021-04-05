---
title: Tipo di privacy (WinInet. h)
description: Specifica che le impostazioni di privacy sono per cookie di terze parti o di terze parti.
ms.assetid: 7d0846d4-fd81-4af9-b7e6-05c4c1438770
topic_type:
- apiref
api_name:
- PRIVACY_TYPE_FIRST_PARTY
- PRIVACY_TYPE_THIRD_PARTY
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38583d5f0c5cee148353f98f5d2be2d4f1a50216
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874602"
---
# <a name="privacy-type"></a><span data-ttu-id="410e6-103">Tipo di privacy</span><span class="sxs-lookup"><span data-stu-id="410e6-103">Privacy Type</span></span>

<span data-ttu-id="410e6-104">Specifica che le impostazioni di privacy sono per cookie di terze parti o di terze parti.</span><span class="sxs-lookup"><span data-stu-id="410e6-104">Specifies that privacy settings are for either first-party or third-party cookies.</span></span>

<dl> <dt>

<span data-ttu-id="410e6-105"><span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**tipo di PRIVACY \_ \_ prima \_ parte**</span><span class="sxs-lookup"><span data-stu-id="410e6-105"><span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**PRIVACY\_TYPE\_FIRST\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410e6-106">0</span><span class="sxs-lookup"><span data-stu-id="410e6-106">0</span></span>
</dt> <dt>



<span data-ttu-id="410e6-107">Fa riferimento alle impostazioni di privacy per i cookie di terze parti.</span><span class="sxs-lookup"><span data-stu-id="410e6-107">Refers to privacy settings for first party cookies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="410e6-108"><span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**tipo di PRIVACY di \_ \_ terze \_ parti**</span><span class="sxs-lookup"><span data-stu-id="410e6-108"><span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**PRIVACY\_TYPE\_THIRD\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410e6-109">1</span><span class="sxs-lookup"><span data-stu-id="410e6-109">1</span></span>
</dt> <dt>



<span data-ttu-id="410e6-110">Fa riferimento alle impostazioni di privacy per i cookie di terze parti.</span><span class="sxs-lookup"><span data-stu-id="410e6-110">Refers to privacy settings for third party cookies.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="410e6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="410e6-111">Remarks</span></span>

<span data-ttu-id="410e6-112">I cookie sono suddivisi in categorie come la prima e la terza parte.</span><span class="sxs-lookup"><span data-stu-id="410e6-112">Cookies are categorized as first-party and third-party.</span></span> <span data-ttu-id="410e6-113">Un cookie di prima entità è quello che ha origine dal dominio host.</span><span class="sxs-lookup"><span data-stu-id="410e6-113">A first-party cookie is one that originates from the host domain.</span></span> <span data-ttu-id="410e6-114">Se " https://www.blueyonderairlines.com " si trova nella barra degli indirizzi di Microsoft Internet Explorer, "www.blueyonderairlines.com" è il dominio host.</span><span class="sxs-lookup"><span data-stu-id="410e6-114">If "https://www.blueyonderairlines.com" is found in the Microsoft Internet Explorer address bar, "www.blueyonderairlines.com" is the host domain.</span></span> <span data-ttu-id="410e6-115">Quando si visita questa pagina, se un cookie viene impostato da un dominio diverso da "www.blueyonderairlines.com", ad esempio "www.fourthcoffee.com", il cookie viene considerato un cookie di terze parti.</span><span class="sxs-lookup"><span data-stu-id="410e6-115">While visiting this page, if a cookie is set from a domain other than "www.blueyonderairlines.com", such as "www.fourthcoffee.com", this cookie is considered a third-party cookie.</span></span>

> [!Note]  
> <span data-ttu-id="410e6-116">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="410e6-116">WinINet does not support server implementations.</span></span> <span data-ttu-id="410e6-117">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="410e6-117">In addition, it should not be used from a service.</span></span> <span data-ttu-id="410e6-118">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="410e6-118">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="410e6-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="410e6-119">Requirements</span></span>



| <span data-ttu-id="410e6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="410e6-120">Requirement</span></span> | <span data-ttu-id="410e6-121">Valore</span><span class="sxs-lookup"><span data-stu-id="410e6-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="410e6-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="410e6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="410e6-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="410e6-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="410e6-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="410e6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="410e6-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="410e6-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="410e6-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="410e6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="410e6-127"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="410e6-127"><dt>Wininet.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="410e6-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="410e6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="410e6-129">**PrivacyGetZonePreferenceW**</span><span class="sxs-lookup"><span data-stu-id="410e6-129">**PrivacyGetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[<span data-ttu-id="410e6-130">**PrivacySetZonePreferenceW**</span><span class="sxs-lookup"><span data-stu-id="410e6-130">**PrivacySetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

