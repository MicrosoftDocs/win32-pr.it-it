---
description: Specifica l'elenco di reti LAN wireless a cui deve essere consentita la connessione di qualsiasi computer.
ms.assetid: e24557d8-dedf-4381-bba0-cdb7ea26083b
title: Elemento allow (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5488f962a1ba526b34ca2d10144a150d7c1417d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305620"
---
# <a name="allowlist-networkfilter-element"></a><span data-ttu-id="947a2-103">Elemento allow (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="947a2-103">allowList (networkFilter) Element</span></span>

<span data-ttu-id="947a2-104">L'elemento allow (networkFilter) specifica l'elenco di reti LAN wireless a cui deve essere consentita la connessione a qualsiasi computer.</span><span class="sxs-lookup"><span data-stu-id="947a2-104">The allowList (networkFilter) element specifies the list of wireless LAN networks to which any machine must be allowed to connect.</span></span>

``` syntax
<xs:element name="allowList">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="network"
                type="networkItemType"
                maxOccurs="unbounded"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="947a2-105">L'elemento **Allow** è definito dall'elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="947a2-105">The **allowList** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="947a2-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="947a2-106">Child elements</span></span>



| <span data-ttu-id="947a2-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="947a2-107">Element</span></span>                                                        | <span data-ttu-id="947a2-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="947a2-108">Type</span></span>                                                                     | <span data-ttu-id="947a2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="947a2-109">Description</span></span>                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="947a2-110">**network**</span><span class="sxs-lookup"><span data-stu-id="947a2-110">**network**</span></span>](wlan-policyschema-network-allowlist-element.md) | [<span data-ttu-id="947a2-111">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="947a2-111">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="947a2-112">Rete a cui la macchina virtuale è in grado di connettersi.</span><span class="sxs-lookup"><span data-stu-id="947a2-112">The network to which the machine can connect.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="947a2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="947a2-113">Requirements</span></span>



| <span data-ttu-id="947a2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="947a2-114">Requirement</span></span> | <span data-ttu-id="947a2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="947a2-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="947a2-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="947a2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="947a2-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="947a2-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="947a2-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="947a2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="947a2-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="947a2-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="947a2-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="947a2-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="947a2-121">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="947a2-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="947a2-122">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="947a2-122">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="947a2-123">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="947a2-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="947a2-124">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="947a2-124">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




