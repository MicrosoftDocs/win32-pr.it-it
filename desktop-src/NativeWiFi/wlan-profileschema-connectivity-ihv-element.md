---
description: Contiene le impostazioni di connettività correlate a IHV. Non è attualmente implementato.
ms.assetid: d943e82a-8660-4df7-8f5c-42ed83f17313
title: Connectivity (IHV)-elemento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 257addbcbd721e5930405e3954dcb348f367af93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753751"
---
# <a name="connectivity-ihv-element"></a><span data-ttu-id="73422-104">Connectivity (IHV)-elemento</span><span class="sxs-lookup"><span data-stu-id="73422-104">connectivity (IHV) Element</span></span>

<span data-ttu-id="73422-105">L'elemento Connectivity (IHV) contiene le impostazioni di connettività correlate a IHV.</span><span class="sxs-lookup"><span data-stu-id="73422-105">The connectivity (IHV) element contains IHV-related connectivity settings.</span></span> <span data-ttu-id="73422-106">Non è attualmente implementato.</span><span class="sxs-lookup"><span data-stu-id="73422-106">It is not currently implemented.</span></span>

<span data-ttu-id="73422-107">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="73422-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
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
```

<span data-ttu-id="73422-108">L'elemento è definito dall'elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="73422-108">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="73422-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73422-109">Requirements</span></span>



| <span data-ttu-id="73422-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="73422-110">Requirement</span></span> | <span data-ttu-id="73422-111">Valore</span><span class="sxs-lookup"><span data-stu-id="73422-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="73422-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73422-112">Minimum supported client</span></span><br/> | <span data-ttu-id="73422-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73422-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="73422-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73422-114">Minimum supported server</span></span><br/> | <span data-ttu-id="73422-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="73422-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73422-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73422-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="73422-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="73422-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="73422-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="73422-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="73422-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="73422-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="73422-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="73422-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




