---
description: Contiene un hexBinary di 3 byte che identifica IHV.
ms.assetid: 0b2e73fb-df3a-48c4-b38d-970c37de46eb
title: Elemento OUI (OUIHeader)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUI
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 49a9cceffb308c64c8d1addf7c257b422751661f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306490"
---
# <a name="oui-ouiheader-element"></a><span data-ttu-id="28d9f-103">Elemento OUI (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="28d9f-103">OUI (OUIHeader) Element</span></span>

<span data-ttu-id="28d9f-104">L'elemento OUI (OUIHeader) contiene un hexBinary di 3 byte che identifica IHV.</span><span class="sxs-lookup"><span data-stu-id="28d9f-104">The OUI (OUIHeader) element contains a 3 byte hexBinary that identifies the IHV.</span></span>

<span data-ttu-id="28d9f-105">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="28d9f-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
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
```

<span data-ttu-id="28d9f-106">L'elemento è definito dall'elemento [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) .</span><span class="sxs-lookup"><span data-stu-id="28d9f-106">The element is defined by the [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="28d9f-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28d9f-107">Requirements</span></span>



| <span data-ttu-id="28d9f-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="28d9f-108">Requirement</span></span> | <span data-ttu-id="28d9f-109">Valore</span><span class="sxs-lookup"><span data-stu-id="28d9f-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="28d9f-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28d9f-110">Minimum supported client</span></span><br/> | <span data-ttu-id="28d9f-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28d9f-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="28d9f-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28d9f-112">Minimum supported server</span></span><br/> | <span data-ttu-id="28d9f-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28d9f-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28d9f-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28d9f-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="28d9f-115">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="28d9f-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="28d9f-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="28d9f-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

<span data-ttu-id="28d9f-117">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="28d9f-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="28d9f-118">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="28d9f-118">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




