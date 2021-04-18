---
description: Definisce l'elenco delle reti consentite e negate per i computer.
ms.assetid: 21502c97-36a4-4cd6-9dd0-ee44c4cc522f
title: Elemento networkFilter (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkFilter
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d78a23ba1a456f1ad45745fcc25580c27de148c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317121"
---
# <a name="networkfilter-wlanpolicy-element"></a><span data-ttu-id="382c9-103">Elemento networkFilter (WLANPolicy)</span><span class="sxs-lookup"><span data-stu-id="382c9-103">networkFilter (WLANPolicy) Element</span></span>

<span data-ttu-id="382c9-104">L'elemento networkFilter (WLANPolicy) definisce l'elenco delle reti consentite e negate per i computer.</span><span class="sxs-lookup"><span data-stu-id="382c9-104">The networkFilter (WLANPolicy) element defines the list of allowed and denied networks for machines.</span></span>

``` syntax
<xs:element name="networkFilter">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="allowList"
                minOccurs="0"
            >
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
            <xs:element name="blockList"
                minOccurs="0"
            >
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
            <xs:element name="denyAllIBSS"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="denyAllESS"
                type="boolean"
                minOccurs="0"
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

<span data-ttu-id="382c9-105">L'elemento **networkFilter** è definito dall'elemento [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="382c9-105">The **networkFilter** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="382c9-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="382c9-106">Child elements</span></span>



| <span data-ttu-id="382c9-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="382c9-107">Element</span></span>                                                                    | <span data-ttu-id="382c9-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="382c9-108">Type</span></span>                                                                     | <span data-ttu-id="382c9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="382c9-109">Description</span></span>                                                                                    |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="382c9-110">**Elenco serializzazione**</span><span class="sxs-lookup"><span data-stu-id="382c9-110">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)     |                                                                          | <span data-ttu-id="382c9-111">Elenco di reti LAN wireless a cui deve essere consentita la connessione di qualsiasi computer.</span><span class="sxs-lookup"><span data-stu-id="382c9-111">The list of wireless LAN networks to which any machine must be allowed to connect.</span></span> <br/> |
| [<span data-ttu-id="382c9-112">**blockList**</span><span class="sxs-lookup"><span data-stu-id="382c9-112">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)     |                                                                          | <span data-ttu-id="382c9-113">Elenco di reti LAN wireless a cui un computer non deve connettersi.</span><span class="sxs-lookup"><span data-stu-id="382c9-113">The list of wireless LAN networks to which a machine must not connect.</span></span><br/>              |
| [<span data-ttu-id="382c9-114">**denyAllESS**</span><span class="sxs-lookup"><span data-stu-id="382c9-114">**denyAllESS**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)   | <span data-ttu-id="382c9-115">boolean</span><span class="sxs-lookup"><span data-stu-id="382c9-115">boolean</span></span>                                                                  | <span data-ttu-id="382c9-116">Specifica se l'accesso a tutte le reti dell'infrastruttura è bloccato.</span><span class="sxs-lookup"><span data-stu-id="382c9-116">Specifies if access to all infrastructure networks is blocked.</span></span> <br/>                     |
| [<span data-ttu-id="382c9-117">**denyAllIBSS**</span><span class="sxs-lookup"><span data-stu-id="382c9-117">**denyAllIBSS**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md) | <span data-ttu-id="382c9-118">boolean</span><span class="sxs-lookup"><span data-stu-id="382c9-118">boolean</span></span>                                                                  | <span data-ttu-id="382c9-119">Specifica se l'accesso a tutte le reti ad hoc è bloccato.</span><span class="sxs-lookup"><span data-stu-id="382c9-119">Specifies if access to all ad-hoc networks is blocked.</span></span> <br/>                             |
| [<span data-ttu-id="382c9-120">**network**</span><span class="sxs-lookup"><span data-stu-id="382c9-120">**network**</span></span>](wlan-policyschema-network-allowlist-element.md)             | [<span data-ttu-id="382c9-121">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="382c9-121">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="382c9-122">Rete consentita.</span><span class="sxs-lookup"><span data-stu-id="382c9-122">An allowed network.</span></span> <br/>                                                                |
| [<span data-ttu-id="382c9-123">**network**</span><span class="sxs-lookup"><span data-stu-id="382c9-123">**network**</span></span>](wlan-policyschema-network-blocklist-element.md)             | [<span data-ttu-id="382c9-124">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="382c9-124">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="382c9-125">Rete bloccata.</span><span class="sxs-lookup"><span data-stu-id="382c9-125">A blocked network.</span></span> <br/>                                                                 |



## <a name="requirements"></a><span data-ttu-id="382c9-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="382c9-126">Requirements</span></span>



| <span data-ttu-id="382c9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="382c9-127">Requirement</span></span> | <span data-ttu-id="382c9-128">Valore</span><span class="sxs-lookup"><span data-stu-id="382c9-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="382c9-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="382c9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="382c9-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="382c9-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="382c9-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="382c9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="382c9-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="382c9-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="382c9-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="382c9-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="382c9-134">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="382c9-134">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="382c9-135">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="382c9-135">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="382c9-136">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="382c9-136">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="382c9-137">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="382c9-137">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




