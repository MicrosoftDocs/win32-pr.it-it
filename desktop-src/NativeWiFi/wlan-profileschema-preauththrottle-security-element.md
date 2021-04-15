---
description: Specifica il numero di tentativi di pre-autenticazione da provare negli APs adiacenti.
ms.assetid: 7e89e962-7544-4efb-9e3c-c108bee22aea
title: Elemento preAuthThrottle (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthThrottle
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 499401affb264238a065c0861f1230f23936206e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525753"
---
# <a name="preauththrottle-security-element"></a><span data-ttu-id="ae475-103">Elemento preAuthThrottle (Security)</span><span class="sxs-lookup"><span data-stu-id="ae475-103">preAuthThrottle (security) Element</span></span>

<span data-ttu-id="ae475-104">L'elemento preAuthThrottle (Security) specifica il numero di tentativi di pre-autenticazione da provare negli APs adiacenti.</span><span class="sxs-lookup"><span data-stu-id="ae475-104">The preAuthThrottle (security) element specifies the number pre-authentication attempts to try on neighboring APs.</span></span> <span data-ttu-id="ae475-105">Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "Enabled".</span><span class="sxs-lookup"><span data-stu-id="ae475-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="ae475-106">Se **PMKCacheMode** è abilitato e questo elemento è assente, il numero di tentativi predefinito è 3.</span><span class="sxs-lookup"><span data-stu-id="ae475-106">If **PMKCacheMode** is enabled, and this element is absent, the number of tries defaults to 3.</span></span>

<span data-ttu-id="ae475-107">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ae475-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="preAuthThrottle"
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
                value="16"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="ae475-108">L'elemento è definito dall'elemento di [**sicurezza**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ae475-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae475-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae475-109">Requirements</span></span>



| <span data-ttu-id="ae475-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae475-110">Requirement</span></span> | <span data-ttu-id="ae475-111">Valore</span><span class="sxs-lookup"><span data-stu-id="ae475-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ae475-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae475-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ae475-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae475-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ae475-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae475-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ae475-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ae475-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ae475-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae475-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="ae475-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="ae475-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ae475-118">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="ae475-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="ae475-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="ae475-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ae475-120">**sicurezza (MSM)**</span><span class="sxs-lookup"><span data-stu-id="ae475-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




