---
description: Indica se verrà utilizzata la memorizzazione nella cache PMK.
ms.assetid: 5650c893-6047-4e99-a2be-22722d6a809a
title: Elemento PMKCacheMode (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 609660d6f3161cbaaa5e0505daf9c6b9180b6c32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128847"
---
# <a name="pmkcachemode-security-element"></a><span data-ttu-id="dfd71-103">Elemento PMKCacheMode (Security)</span><span class="sxs-lookup"><span data-stu-id="dfd71-103">PMKCacheMode (security) Element</span></span>

<span data-ttu-id="dfd71-104">L'elemento PMKCacheMode (Security) indica se verrà utilizzata la memorizzazione nella cache di PMK.</span><span class="sxs-lookup"><span data-stu-id="dfd71-104">The PMKCacheMode (security) element indicates whether PMK caching will be used.</span></span> <span data-ttu-id="dfd71-105">Questo elemento è valido solo per le reti definite da WPA2.</span><span class="sxs-lookup"><span data-stu-id="dfd71-105">This element is valid only for WPA2-defined networks.</span></span> <span data-ttu-id="dfd71-106">La memorizzazione nella cache PMK è descritta nella specifica [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="dfd71-106">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="dfd71-107">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="dfd71-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheMode"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="disabled"
             />
            <xs:enumeration
                value="enabled"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="dfd71-108">L'elemento è definito dall'elemento di [**sicurezza**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="dfd71-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfd71-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfd71-109">Requirements</span></span>



| <span data-ttu-id="dfd71-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfd71-110">Requirement</span></span> | <span data-ttu-id="dfd71-111">Valore</span><span class="sxs-lookup"><span data-stu-id="dfd71-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dfd71-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfd71-112">Minimum supported client</span></span><br/> | <span data-ttu-id="dfd71-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dfd71-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dfd71-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfd71-114">Minimum supported server</span></span><br/> | <span data-ttu-id="dfd71-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dfd71-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dfd71-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfd71-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="dfd71-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="dfd71-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="dfd71-118">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="dfd71-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="dfd71-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="dfd71-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="dfd71-120">**sicurezza (MSM)**</span><span class="sxs-lookup"><span data-stu-id="dfd71-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




