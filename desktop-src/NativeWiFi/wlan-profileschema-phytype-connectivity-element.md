---
description: Specifica lo standard LAN wireless 802,11 usato in una LAN wireless.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: Elemento phyType (Connectivity)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- phyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 71a58e464528136244cec745aed2e59c6fea737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306487"
---
# <a name="phytype-connectivity-element"></a><span data-ttu-id="83cb0-103">Elemento phyType (Connectivity)</span><span class="sxs-lookup"><span data-stu-id="83cb0-103">phyType (connectivity) Element</span></span>

<span data-ttu-id="83cb0-104">L'elemento phyType (Connectivity) specifica lo standard della LAN wireless 802,11 usato in una LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="83cb0-104">The phyType (connectivity) element specifies the 802.11 wireless LAN standard used on a wireless LAN.</span></span>

<span data-ttu-id="83cb0-105">È possibile specificare più **phyType** s.</span><span class="sxs-lookup"><span data-stu-id="83cb0-105">You can specify multiple **phyType** s.</span></span> <span data-ttu-id="83cb0-106">Se non viene specificato alcun **phyType** , il profilo può essere usato per connettersi a qualsiasi **phyType**.</span><span class="sxs-lookup"><span data-stu-id="83cb0-106">If no **phyType** is specified, the profile can be used to connect to any **phyType**.</span></span> <span data-ttu-id="83cb0-107">Il valore "n" è supportato solo in Windows Vista con Service Pack 1 (SP1) e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="83cb0-107">The value "n" is only supported on Windows Vista with Service Pack 1 (SP1) and later versions of the operating system.</span></span>

<span data-ttu-id="83cb0-108">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="83cb0-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="phyType"
    minOccurs="0"
    maxOccurs="4"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="a"
             />
            <xs:enumeration
                value="b"
             />
            <xs:enumeration
                value="g"
             />
            <xs:enumeration
                value="n"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="83cb0-109">L'elemento è definito dall'elemento [**Connectivity**](wlan-profileschema-connectivity-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="83cb0-109">The element is defined by the [**connectivity**](wlan-profileschema-connectivity-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="83cb0-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83cb0-110">Requirements</span></span>



| <span data-ttu-id="83cb0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="83cb0-111">Requirement</span></span> | <span data-ttu-id="83cb0-112">Valore</span><span class="sxs-lookup"><span data-stu-id="83cb0-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="83cb0-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83cb0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="83cb0-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83cb0-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="83cb0-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83cb0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="83cb0-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="83cb0-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83cb0-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83cb0-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="83cb0-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="83cb0-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="83cb0-119">**connettività**</span><span class="sxs-lookup"><span data-stu-id="83cb0-119">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

<span data-ttu-id="83cb0-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="83cb0-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="83cb0-121">**connettività (MSM)**</span><span class="sxs-lookup"><span data-stu-id="83cb0-121">**connectivity (MSM)**</span></span>](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




