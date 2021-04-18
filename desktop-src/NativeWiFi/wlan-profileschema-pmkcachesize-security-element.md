---
description: Specifica il numero di voci nella cache PMK nel client.
ms.assetid: 3a53f7fd-7f12-43d3-94e6-a11bec389a34
title: Elemento PMKCacheSize (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheSize
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b21054ddc97c51212ea3a06207617ad85228270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306488"
---
# <a name="pmkcachesize-security-element"></a><span data-ttu-id="749de-103">Elemento PMKCacheSize (Security)</span><span class="sxs-lookup"><span data-stu-id="749de-103">PMKCacheSize (security) Element</span></span>

<span data-ttu-id="749de-104">L'elemento PMKCacheSize (Security) specifica il numero di voci nella cache PMK nel client.</span><span class="sxs-lookup"><span data-stu-id="749de-104">The PMKCacheSize (security) element specifies the number of entries in the PMK cache on the client.</span></span> <span data-ttu-id="749de-105">Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "Enabled".</span><span class="sxs-lookup"><span data-stu-id="749de-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="749de-106">Se **PMKCacheMode** è abilitato e questo elemento è assente, per impostazione predefinita la dimensione della cache corrisponde a 128 voci.</span><span class="sxs-lookup"><span data-stu-id="749de-106">If **PMKCacheMode** is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span>

<span data-ttu-id="749de-107">La memorizzazione nella cache PMK è descritta nella specifica [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="749de-107">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="749de-108">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="749de-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheSize"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="255"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="749de-109">L'elemento è definito dall'elemento di [**sicurezza**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="749de-109">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="749de-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="749de-110">Requirements</span></span>



| <span data-ttu-id="749de-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="749de-111">Requirement</span></span> | <span data-ttu-id="749de-112">Valore</span><span class="sxs-lookup"><span data-stu-id="749de-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="749de-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="749de-113">Minimum supported client</span></span><br/> | <span data-ttu-id="749de-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="749de-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="749de-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="749de-115">Minimum supported server</span></span><br/> | <span data-ttu-id="749de-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="749de-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="749de-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="749de-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="749de-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="749de-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="749de-119">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="749de-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="749de-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="749de-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="749de-121">**sicurezza (MSM)**</span><span class="sxs-lookup"><span data-stu-id="749de-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




