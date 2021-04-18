---
description: Contiene diverse impostazioni per i fornitori di hardware indipendenti.
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: Elemento IHV (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2d2902522c84ebe2939d42301a491521ac8a70f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308883"
---
# <a name="ihv-wlanprofile-element"></a><span data-ttu-id="66ba2-103">Elemento IHV (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="66ba2-103">IHV (WLANProfile) Element</span></span>

<span data-ttu-id="66ba2-104">L'elemento IHV (WLANProfile) contiene diverse impostazioni per i fornitori di hardware indipendenti.</span><span class="sxs-lookup"><span data-stu-id="66ba2-104">The IHV (WLANProfile) element contains various settings for independent hardware vendors.</span></span> <span data-ttu-id="66ba2-105">Se un profilo include le impostazioni di sicurezza di IHV, viene eseguito l'override di qualsiasi sicurezza definita da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="66ba2-105">If a profile includes IHV security settings, they override any Microsoft-defined security.</span></span>

<span data-ttu-id="66ba2-106">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="66ba2-106">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="IHV"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUIHeader">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUI">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="3"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="type">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="1"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="useMSOneX"
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

<span data-ttu-id="66ba2-107">L'elemento è definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="66ba2-107">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="66ba2-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="66ba2-108">Child elements</span></span>



| <span data-ttu-id="66ba2-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="66ba2-109">Element</span></span>                                                             | <span data-ttu-id="66ba2-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="66ba2-110">Type</span></span>                                                              | <span data-ttu-id="66ba2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66ba2-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66ba2-112">**connettività**</span><span class="sxs-lookup"><span data-stu-id="66ba2-112">**connectivity**</span></span>](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | <span data-ttu-id="66ba2-113">Contiene le impostazioni di connettività correlate a IHV.</span><span class="sxs-lookup"><span data-stu-id="66ba2-113">Contains IHV-related connectivity settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="66ba2-114">**OUI**</span><span class="sxs-lookup"><span data-stu-id="66ba2-114">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | <span data-ttu-id="66ba2-115">Contiene un hexBinary di 3 byte che identifica IHV.</span><span class="sxs-lookup"><span data-stu-id="66ba2-115">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="66ba2-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="66ba2-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | <span data-ttu-id="66ba2-117">Identifica IHV.</span><span class="sxs-lookup"><span data-stu-id="66ba2-117">Identifies the IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="66ba2-118">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="66ba2-118">**security**</span></span>](wlan-profileschema-security-ihv-element.md)         |                                                                   | <span data-ttu-id="66ba2-119">Contiene le impostazioni di sicurezza specifiche di IHV.</span><span class="sxs-lookup"><span data-stu-id="66ba2-119">Contains IHV-specific security settings.</span></span> <span data-ttu-id="66ba2-120">Le impostazioni di sicurezza di Microsoft e le impostazioni di sicurezza di IHV si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="66ba2-120">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="66ba2-121">L'intero profilo non è valido se sono presenti entrambe le impostazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="66ba2-121">The entire profile is invalid if both security settings are present.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="66ba2-122">**tipo**</span><span class="sxs-lookup"><span data-stu-id="66ba2-122">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | <span data-ttu-id="66ba2-123">Contiene un hexBinary di 1 byte usato per distinguere le schede di rete con lo stesso IHV.</span><span class="sxs-lookup"><span data-stu-id="66ba2-123">Contains a 1 byte hexBinary that is used to differentiate NICs by the same IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="66ba2-124">**useMSOneX**</span><span class="sxs-lookup"><span data-stu-id="66ba2-124">**useMSOneX**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)       | [<span data-ttu-id="66ba2-125">boolean</span><span class="sxs-lookup"><span data-stu-id="66ba2-125">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="66ba2-126">Specifica l'origine delle impostazioni di sicurezza 802.1 X utilizzate da un componente di sicurezza IHV.</span><span class="sxs-lookup"><span data-stu-id="66ba2-126">Specifies the origin of 802.1X security settings used by an IHV security component.</span></span> <span data-ttu-id="66ba2-127">Quando [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) è true, i componenti di sicurezza di IHV utilizzano le impostazioni 802.1 x definite da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="66ba2-127">When [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="66ba2-128">Quando **useMSOneX** è false, i componenti di sicurezza di IHV utilizzano le impostazioni 802.1 x fornite dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="66ba2-128">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span> <span data-ttu-id="66ba2-129">Per impostazione predefinita, **useMSOneX** è false.</span><span class="sxs-lookup"><span data-stu-id="66ba2-129">By default, **useMSOneX** is false.</span></span> <span data-ttu-id="66ba2-130">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="66ba2-130">This element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="66ba2-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66ba2-131">Requirements</span></span>



| <span data-ttu-id="66ba2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="66ba2-132">Requirement</span></span> | <span data-ttu-id="66ba2-133">Valore</span><span class="sxs-lookup"><span data-stu-id="66ba2-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="66ba2-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66ba2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="66ba2-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66ba2-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="66ba2-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66ba2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="66ba2-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66ba2-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66ba2-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66ba2-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="66ba2-139">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="66ba2-139">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="66ba2-140">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="66ba2-140">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="66ba2-141">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="66ba2-141">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="66ba2-142">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="66ba2-142">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
