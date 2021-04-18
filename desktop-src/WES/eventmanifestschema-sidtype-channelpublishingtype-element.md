---
title: Elemento sidType (ChannelPublishingType)
description: Determina se includere un ID di sicurezza (SID) dell'entità con ogni evento scritto nel canale.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- EventLog elemento sidType
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d65e1ade4ded95b070b45de9462f6aee2c60ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301842"
---
# <a name="sidtype-channelpublishingtype-element"></a><span data-ttu-id="88dc3-104">Elemento sidType (ChannelPublishingType)</span><span class="sxs-lookup"><span data-stu-id="88dc3-104">sidType (ChannelPublishingType) Element</span></span>

<span data-ttu-id="88dc3-105">Determina se includere un ID di sicurezza (SID) dell'entità con ogni evento scritto nel canale.</span><span class="sxs-lookup"><span data-stu-id="88dc3-105">Determines whether to include a security identifier (SID) of the principal with each event written to the channel.</span></span>

``` syntax
<xs:element name="sidType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="None"
             />
            <xs:enumeration
                value="Publishing"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="88dc3-106">L'elemento **SIDType** è definito dal tipo complesso [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="88dc3-106">The **sidType** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="88dc3-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88dc3-107">Requirements</span></span>



| <span data-ttu-id="88dc3-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="88dc3-108">Requirement</span></span> | <span data-ttu-id="88dc3-109">Valore</span><span class="sxs-lookup"><span data-stu-id="88dc3-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="88dc3-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88dc3-110">Minimum supported client</span></span><br/> | <span data-ttu-id="88dc3-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="88dc3-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="88dc3-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88dc3-112">Minimum supported server</span></span><br/> | <span data-ttu-id="88dc3-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="88dc3-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88dc3-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88dc3-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="88dc3-115">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="88dc3-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="88dc3-116">**pubblicazione (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="88dc3-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





