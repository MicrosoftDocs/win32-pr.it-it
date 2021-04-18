---
title: Elemento DifferentUsername (EapType)
description: Informazioni sull'elemento DifferentUsername (EapType). Questo elemento determina il nome utente EAP-TLS da usare.
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- Elemento DifferentUsername EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 505e23c74d4c1c8c74a50906809d0acc9ce06c42
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300476"
---
# <a name="differentusername-eaptype-element"></a><span data-ttu-id="c1fbc-105">Elemento DifferentUsername (EapType)</span><span class="sxs-lookup"><span data-stu-id="c1fbc-105">DifferentUsername (EapType) Element</span></span>

<span data-ttu-id="c1fbc-106">L'elemento **DifferentUsername (EapType)** determina il nome utente EAP-TLS da usare.</span><span class="sxs-lookup"><span data-stu-id="c1fbc-106">The **DifferentUsername (EapType)** element determines which user name EAP-TLS is to use.</span></span>

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

<span data-ttu-id="c1fbc-107">L'elemento **DifferentUsername** è definito dall'elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c1fbc-107">The **DifferentUsername** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1fbc-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1fbc-108">Remarks</span></span>

<span data-ttu-id="c1fbc-109">Se l'elemento **DifferentUserName** è true, EAP-TLS deve usare un nome utente diverso dal nome visualizzato nel certificato.</span><span class="sxs-lookup"><span data-stu-id="c1fbc-109">If the **DifferentUserName** element is TRUE, EAP-TLS should use a user name other than the name that appears on the certificate.</span></span> <span data-ttu-id="c1fbc-110">Se l'elemento **DifferentUserName** è false, EAP-TLS usa il nome utente visualizzato nel certificato.</span><span class="sxs-lookup"><span data-stu-id="c1fbc-110">If the **DifferentUserName** element is FALSE, EAP-TLS uses the user name that appears on the certificate.</span></span>

<span data-ttu-id="c1fbc-111">L'elemento **DifferentUserName** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c1fbc-111">The **DifferentUserName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1fbc-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1fbc-112">Requirements</span></span>



| <span data-ttu-id="c1fbc-113">Ruolo</span><span class="sxs-lookup"><span data-stu-id="c1fbc-113">Role</span></span> | <span data-ttu-id="c1fbc-114">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="c1fbc-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="c1fbc-115">Client</span><span class="sxs-lookup"><span data-stu-id="c1fbc-115">Client</span></span><br/> | <span data-ttu-id="c1fbc-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1fbc-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c1fbc-117">Server</span><span class="sxs-lookup"><span data-stu-id="c1fbc-117">Server</span></span><br/> | <span data-ttu-id="c1fbc-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1fbc-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1fbc-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1fbc-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1fbc-120">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="c1fbc-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c1fbc-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="c1fbc-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="c1fbc-122">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="c1fbc-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c1fbc-123">**EapType**</span><span class="sxs-lookup"><span data-stu-id="c1fbc-123">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="c1fbc-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c1fbc-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="c1fbc-125">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="c1fbc-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="c1fbc-126">Schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c1fbc-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="c1fbc-127">Elementi dello schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c1fbc-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





