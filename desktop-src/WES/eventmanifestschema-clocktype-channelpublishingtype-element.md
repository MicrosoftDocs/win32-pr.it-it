---
title: Elemento clockType (ChannelPublishingType)
description: Risoluzione del clock da usare quando si registra il timestamp per ogni evento.
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- EventLog elemento clockType
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6b85537ec209f39da87e74db6881abdf60e488b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400309"
---
# <a name="clocktype-channelpublishingtype-element"></a><span data-ttu-id="0b6a3-104">Elemento clockType (ChannelPublishingType)</span><span class="sxs-lookup"><span data-stu-id="0b6a3-104">clockType (ChannelPublishingType) Element</span></span>

<span data-ttu-id="0b6a3-105">Risoluzione del clock da usare quando si registra il timestamp per ogni evento.</span><span class="sxs-lookup"><span data-stu-id="0b6a3-105">The clock resolution to use when logging the time stamp for each event.</span></span>

``` syntax
<xs:element name="clockType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="SystemTime"
             />
            <xs:enumeration
                value="QPC"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="0b6a3-106">L'elemento **clockType** è definito dal tipo complesso [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0b6a3-106">The **clockType** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b6a3-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b6a3-107">Requirements</span></span>



| <span data-ttu-id="0b6a3-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b6a3-108">Requirement</span></span> | <span data-ttu-id="0b6a3-109">Valore</span><span class="sxs-lookup"><span data-stu-id="0b6a3-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0b6a3-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b6a3-110">Minimum supported client</span></span><br/> | <span data-ttu-id="0b6a3-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b6a3-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0b6a3-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b6a3-112">Minimum supported server</span></span><br/> | <span data-ttu-id="0b6a3-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0b6a3-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b6a3-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b6a3-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="0b6a3-115">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="0b6a3-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="0b6a3-116">**pubblicazione (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="0b6a3-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





