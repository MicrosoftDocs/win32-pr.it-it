---
description: Indica il periodo di tempo, in minuti, in cui verrà mantenuta una cache PMK.
ms.assetid: d9e3b839-48f6-490c-ab83-067368cdcca2
title: Elemento PMKCacheTTL (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheTTL
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bdfe0edb163dc2bc9766ba8562defb026bbe21fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306486"
---
# <a name="pmkcachettl-security-element"></a><span data-ttu-id="1b4a1-103">Elemento PMKCacheTTL (Security)</span><span class="sxs-lookup"><span data-stu-id="1b4a1-103">PMKCacheTTL (security) Element</span></span>

<span data-ttu-id="1b4a1-104">L'elemento PMKCacheTTL (Security) indica il periodo di tempo, in minuti, in cui verrà mantenuta una cache di PMK.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-104">The PMKCacheTTL (security) element indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="1b4a1-105">Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "Enabled".</span><span class="sxs-lookup"><span data-stu-id="1b4a1-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span>

<span data-ttu-id="1b4a1-106">La memorizzazione nella cache PMK è descritta nella specifica [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="1b4a1-106">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="1b4a1-107">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheTTL"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="5"
             />
            <xs:maxInclusive
                value="1440"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="1b4a1-108">L'elemento è definito dall'elemento di [**sicurezza**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1b4a1-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b4a1-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b4a1-109">Requirements</span></span>



| <span data-ttu-id="1b4a1-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b4a1-110">Requirement</span></span> | <span data-ttu-id="1b4a1-111">Valore</span><span class="sxs-lookup"><span data-stu-id="1b4a1-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1b4a1-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b4a1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1b4a1-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b4a1-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1b4a1-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b4a1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1b4a1-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1b4a1-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b4a1-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b4a1-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="1b4a1-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="1b4a1-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1b4a1-118">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="1b4a1-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="1b4a1-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="1b4a1-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1b4a1-120">**sicurezza (MSM)**</span><span class="sxs-lookup"><span data-stu-id="1b4a1-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




