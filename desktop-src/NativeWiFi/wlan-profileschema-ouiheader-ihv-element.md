---
description: Identifica IHV.
ms.assetid: a99c231c-afd7-44e6-81af-3d49ffef8714
title: Elemento OUIHeader (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUIHeader
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a31feb123e31489c751b7844e06d5c344278778e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306491"
---
# <a name="ouiheader-ihv-element"></a><span data-ttu-id="fbf99-103">Elemento OUIHeader (IHV)</span><span class="sxs-lookup"><span data-stu-id="fbf99-103">OUIHeader (IHV) Element</span></span>

<span data-ttu-id="fbf99-104">L'elemento OUIHeader (IHV) identifica IHV.</span><span class="sxs-lookup"><span data-stu-id="fbf99-104">The OUIHeader (IHV) element identifies the IHV.</span></span>

<span data-ttu-id="fbf99-105">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="fbf99-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
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
```

<span data-ttu-id="fbf99-106">L'elemento è definito dall'elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf99-106">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fbf99-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="fbf99-107">Child elements</span></span>



| <span data-ttu-id="fbf99-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="fbf99-108">Element</span></span>                                                   | <span data-ttu-id="fbf99-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="fbf99-109">Type</span></span> | <span data-ttu-id="fbf99-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbf99-110">Description</span></span>                                                                                |
|-----------------------------------------------------------|------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fbf99-111">**OUI**</span><span class="sxs-lookup"><span data-stu-id="fbf99-111">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)   |      | <span data-ttu-id="fbf99-112">Contiene un hexBinary di 3 byte che identifica IHV.</span><span class="sxs-lookup"><span data-stu-id="fbf99-112">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/>                            |
| [<span data-ttu-id="fbf99-113">**tipo**</span><span class="sxs-lookup"><span data-stu-id="fbf99-113">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md) |      | <span data-ttu-id="fbf99-114">Contiene un hexBinary di 1 byte usato per distinguere le schede di rete con lo stesso IHV.</span><span class="sxs-lookup"><span data-stu-id="fbf99-114">Contains a 1 byte hexBinary that is used to differentiate NICs by the same IHV.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fbf99-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbf99-115">Requirements</span></span>



| <span data-ttu-id="fbf99-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbf99-116">Requirement</span></span> | <span data-ttu-id="fbf99-117">Valore</span><span class="sxs-lookup"><span data-stu-id="fbf99-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fbf99-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fbf99-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf99-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fbf99-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fbf99-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fbf99-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf99-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fbf99-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbf99-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fbf99-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="fbf99-123">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="fbf99-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fbf99-124">**IHV**</span><span class="sxs-lookup"><span data-stu-id="fbf99-124">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="fbf99-125">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="fbf99-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fbf99-126">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="fbf99-126">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




