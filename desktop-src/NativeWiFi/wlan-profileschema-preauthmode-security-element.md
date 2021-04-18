---
description: Indica se la pre-autenticazione verrà utilizzata dal client.
ms.assetid: 305d77b6-fe2d-45c6-ac91-5769f91de152
title: Elemento preAuthMode (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ac74f193fb89c260b1a121b673f239147658865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306485"
---
# <a name="preauthmode-security-element"></a><span data-ttu-id="a95b7-103">Elemento preAuthMode (Security)</span><span class="sxs-lookup"><span data-stu-id="a95b7-103">preAuthMode (security) Element</span></span>

<span data-ttu-id="a95b7-104">L'elemento preAuthMode (Security) indica se la preautenticazione verrà utilizzata dal client.</span><span class="sxs-lookup"><span data-stu-id="a95b7-104">The preAuthMode (security) element indicates whether pre-authentication will be used by the client.</span></span> <span data-ttu-id="a95b7-105">La pre-autenticazione è necessaria per il roaming veloce sicuro di WPA2.</span><span class="sxs-lookup"><span data-stu-id="a95b7-105">Pre-authentication is necessary for WPA2 secure fast roaming.</span></span> <span data-ttu-id="a95b7-106">Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "Enabled".</span><span class="sxs-lookup"><span data-stu-id="a95b7-106">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="a95b7-107">Se **PMKCacheMode** è abilitato e questo elemento è assente, il valore predefinito è "disabled".</span><span class="sxs-lookup"><span data-stu-id="a95b7-107">If **PMKCacheMode** is enabled, and this element is absent, the default value is "disabled".</span></span>

<span data-ttu-id="a95b7-108">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a95b7-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="preAuthMode"
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

<span data-ttu-id="a95b7-109">L'elemento è definito dall'elemento di [**sicurezza**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a95b7-109">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a95b7-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a95b7-110">Requirements</span></span>



| <span data-ttu-id="a95b7-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a95b7-111">Requirement</span></span> | <span data-ttu-id="a95b7-112">Valore</span><span class="sxs-lookup"><span data-stu-id="a95b7-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a95b7-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a95b7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a95b7-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a95b7-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a95b7-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a95b7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a95b7-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a95b7-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a95b7-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a95b7-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="a95b7-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="a95b7-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a95b7-119">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="a95b7-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="a95b7-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="a95b7-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a95b7-121">**sicurezza (MSM)**</span><span class="sxs-lookup"><span data-stu-id="a95b7-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




