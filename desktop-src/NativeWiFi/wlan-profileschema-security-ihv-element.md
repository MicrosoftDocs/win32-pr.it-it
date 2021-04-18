---
description: Contiene diverse impostazioni di sicurezza utilizzate dai fornitori di hardware indipendenti.
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: Security (IHV)-elemento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ace1bb0ca31f40fdc9d10fba13832797d8d4306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313323"
---
# <a name="security-ihv-element"></a><span data-ttu-id="201b6-103">Security (IHV)-elemento</span><span class="sxs-lookup"><span data-stu-id="201b6-103">security (IHV) Element</span></span>

<span data-ttu-id="201b6-104">L'elemento Security (IHV) contiene diverse impostazioni di sicurezza utilizzate dai fornitori di hardware indipendenti.</span><span class="sxs-lookup"><span data-stu-id="201b6-104">The security (IHV) element contains various security settings used by independent hardware vendors.</span></span>

<span data-ttu-id="201b6-105">Le impostazioni di sicurezza di Microsoft e le impostazioni di sicurezza di IHV si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="201b6-105">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="201b6-106">Se entrambi i set di impostazioni di sicurezza sono presenti nello stesso profilo, il profilo non è valido.</span><span class="sxs-lookup"><span data-stu-id="201b6-106">If both sets of security settings are present in the same profile, the profile is invalid.</span></span>

<span data-ttu-id="201b6-107">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="201b6-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="201b6-108">L'elemento **Security** è definito dall'elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="201b6-108">The **security** element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="201b6-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="201b6-109">Requirements</span></span>



| <span data-ttu-id="201b6-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="201b6-110">Requirement</span></span> | <span data-ttu-id="201b6-111">Valore</span><span class="sxs-lookup"><span data-stu-id="201b6-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="201b6-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="201b6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="201b6-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="201b6-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="201b6-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="201b6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="201b6-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="201b6-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="201b6-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="201b6-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="201b6-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="201b6-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="201b6-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="201b6-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="201b6-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="201b6-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="201b6-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="201b6-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




