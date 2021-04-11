---
description: Specifica l'indice della chiave da usare per crittografare il traffico wireless. Viene usato solo quando il tipo di operazione è impostato su &\# 0034; networkKey&\# 0034;.
ms.assetid: 5629605d-4c23-4318-8f09-939e13302552
title: Elemento index (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyIndex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 43bb802d46abb3c4684b63206377d3464078e2c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131938"
---
# <a name="keyindex-security-element"></a><span data-ttu-id="e1689-104">Elemento index (Security)</span><span class="sxs-lookup"><span data-stu-id="e1689-104">keyIndex (security) Element</span></span>

<span data-ttu-id="e1689-105">L'elemento chiave index (Security) specifica quale indice della chiave deve essere usato per crittografare il traffico wireless.</span><span class="sxs-lookup"><span data-stu-id="e1689-105">The keyIndex (security) element specifies which key index should be used to encrypt wireless traffic.</span></span> <span data-ttu-id="e1689-106">Viene usato solo quando il [**tipo**](wlan-profileschema-keytype-sharedkey-element.md) di argomento è impostato su "networkKey".</span><span class="sxs-lookup"><span data-stu-id="e1689-106">This is only used when [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) is set to "networkKey".</span></span>

``` syntax
<xs:element name="keyIndex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="0"
             />
            <xs:maxInclusive
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="e1689-107">L'elemento è definito dall'elemento di [**sicurezza**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e1689-107">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1689-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1689-108">Requirements</span></span>



| <span data-ttu-id="e1689-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1689-109">Requirement</span></span> | <span data-ttu-id="e1689-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e1689-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e1689-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1689-111">Minimum supported client</span></span><br/> | <span data-ttu-id="e1689-112">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="e1689-112">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e1689-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1689-113">Minimum supported server</span></span><br/> | <span data-ttu-id="e1689-114">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e1689-114">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="e1689-115">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e1689-115">Redistributable</span></span><br/>          | <span data-ttu-id="e1689-116">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="e1689-116">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="e1689-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1689-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="e1689-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="e1689-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e1689-119">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="e1689-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="e1689-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="e1689-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e1689-121">**sicurezza (MSM)**</span><span class="sxs-lookup"><span data-stu-id="e1689-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




