---
description: Contiene diverse impostazioni di connettività.
ms.assetid: 2938f607-47a1-49eb-bf3f-247cab8637ec
title: connettività (MSM)-elemento
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
ms.openlocfilehash: 938e5b19ffab490066fbbe299bd250191d9226a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319408"
---
# <a name="connectivity-msm-element"></a><span data-ttu-id="a9aa7-103">connettività (MSM)-elemento</span><span class="sxs-lookup"><span data-stu-id="a9aa7-103">connectivity (MSM) Element</span></span>

<span data-ttu-id="a9aa7-104">L'elemento Connectivity (MSM) contiene diverse impostazioni di connettività.</span><span class="sxs-lookup"><span data-stu-id="a9aa7-104">The connectivity (MSM) element contains various connectivity settings.</span></span>

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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

<span data-ttu-id="a9aa7-105">L'elemento è definito dall'elemento [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a9aa7-105">The element is defined by the [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a9aa7-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a9aa7-106">Child elements</span></span>



| <span data-ttu-id="a9aa7-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a9aa7-107">Element</span></span>                                                            | <span data-ttu-id="a9aa7-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9aa7-108">Type</span></span> |
|--------------------------------------------------------------------|------|
| [<span data-ttu-id="a9aa7-109">**phyType**</span><span class="sxs-lookup"><span data-stu-id="a9aa7-109">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md) |      |



## <a name="examples"></a><span data-ttu-id="a9aa7-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="a9aa7-110">Examples</span></span>

<span data-ttu-id="a9aa7-111">Per visualizzare i profili di esempio che usano l'elemento **Connectivity** , vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="a9aa7-111">To view sample profiles that use the **connectivity** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9aa7-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9aa7-112">Requirements</span></span>



| <span data-ttu-id="a9aa7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9aa7-113">Requirement</span></span> | <span data-ttu-id="a9aa7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a9aa7-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a9aa7-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9aa7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a9aa7-116">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="a9aa7-116">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a9aa7-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9aa7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a9aa7-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a9aa7-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a9aa7-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a9aa7-119">Redistributable</span></span><br/>          | <span data-ttu-id="a9aa7-120">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="a9aa7-120">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a9aa7-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9aa7-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="a9aa7-122">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="a9aa7-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a9aa7-123">**MSM**</span><span class="sxs-lookup"><span data-stu-id="a9aa7-123">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="a9aa7-124">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="a9aa7-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a9aa7-125">**CSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="a9aa7-125">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 




