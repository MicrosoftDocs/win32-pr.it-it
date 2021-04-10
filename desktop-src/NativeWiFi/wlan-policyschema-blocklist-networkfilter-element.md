---
description: Specifica l'elenco di reti LAN wireless a cui un computer non deve connettersi.
ms.assetid: 01db3f7e-1e27-4378-9c42-bc38192f9507
title: Elemento Blocker (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- blockList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e852286d00d93904bd185fef6c2f3444bb5987f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966431"
---
# <a name="blocklist-networkfilter-element"></a><span data-ttu-id="0a225-103">Elemento Blocker (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="0a225-103">blockList (networkFilter) Element</span></span>

<span data-ttu-id="0a225-104">L'elemento Blocker (networkFilter) specifica l'elenco di reti LAN wireless a cui un computer non deve connettersi.</span><span class="sxs-lookup"><span data-stu-id="0a225-104">The blockList (networkFilter) element specifies the list of wireless LAN networks to which a machine must not connect.</span></span>

``` syntax
<xs:element name="blockList">
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

<span data-ttu-id="0a225-105">L'elemento **Blocker** è definito dall'elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0a225-105">The **blockList** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0a225-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0a225-106">Child elements</span></span>



| <span data-ttu-id="0a225-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="0a225-107">Element</span></span>                                                        | <span data-ttu-id="0a225-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a225-108">Type</span></span>                                                                     | <span data-ttu-id="0a225-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a225-109">Description</span></span>                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="0a225-110">**network**</span><span class="sxs-lookup"><span data-stu-id="0a225-110">**network**</span></span>](wlan-policyschema-network-blocklist-element.md) | [<span data-ttu-id="0a225-111">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="0a225-111">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="0a225-112">Rete bloccata.</span><span class="sxs-lookup"><span data-stu-id="0a225-112">The blocked network.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="0a225-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a225-113">Requirements</span></span>



| <span data-ttu-id="0a225-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a225-114">Requirement</span></span> | <span data-ttu-id="0a225-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0a225-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0a225-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a225-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0a225-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a225-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0a225-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a225-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0a225-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0a225-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a225-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a225-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="0a225-121">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="0a225-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0a225-122">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="0a225-122">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="0a225-123">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="0a225-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0a225-124">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="0a225-124">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




