---
description: Contiene un hexBinary di 1 byte usato per distinguere le schede di rete eseguite dallo stesso IHV.
ms.assetid: fd6bae3d-27a8-4bff-9340-b444312b8216
title: Elemento Type (OUIHeader)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 12637e5a70409166e5a31aa0fc98f4df1b9f6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882673"
---
# <a name="type-ouiheader-element"></a><span data-ttu-id="e085f-103">Elemento Type (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="e085f-103">type (OUIHeader) Element</span></span>

<span data-ttu-id="e085f-104">L'elemento Type (OUIHeader) contiene un hexBinary a 1 byte usato per distinguere le schede di rete eseguite dallo stesso IHV.</span><span class="sxs-lookup"><span data-stu-id="e085f-104">The type (OUIHeader) element contains a 1-byte hexBinary that is used to differentiate between NICs made by the same IHV.</span></span>

<span data-ttu-id="e085f-105">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e085f-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
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
```

<span data-ttu-id="e085f-106">L'elemento è definito dall'elemento [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e085f-106">The element is defined by the [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="e085f-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e085f-107">Requirements</span></span>



| <span data-ttu-id="e085f-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="e085f-108">Requirement</span></span> | <span data-ttu-id="e085f-109">Valore</span><span class="sxs-lookup"><span data-stu-id="e085f-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e085f-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e085f-110">Minimum supported client</span></span><br/> | <span data-ttu-id="e085f-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e085f-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e085f-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e085f-112">Minimum supported server</span></span><br/> | <span data-ttu-id="e085f-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e085f-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e085f-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e085f-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="e085f-115">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="e085f-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e085f-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="e085f-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

<span data-ttu-id="e085f-117">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="e085f-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e085f-118">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="e085f-118">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




