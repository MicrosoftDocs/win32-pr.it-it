---
description: Specifica l'elenco dei provider di rete preferiti al momento del roaming.
ms.assetid: 5873fcd7-8e89-4edd-8dc5-f43675919c55
title: Elemento DataRoamingPartners (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DataRoamingPartners
api_type:
- Schema
ms.openlocfilehash: 7f721abd608dd241c399f16eee90369ebcf19594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307541"
---
# <a name="dataroamingpartners-mbnprofile-element"></a><span data-ttu-id="fc7c8-103">Elemento DataRoamingPartners (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="fc7c8-103">DataRoamingPartners (MBNProfile) Element</span></span>

<span data-ttu-id="fc7c8-104">L'elemento **DataRoamingPartners (MBNProfile)** specifica l'elenco dei provider di rete preferiti al momento del roaming.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-104">The **DataRoamingPartners (MBNProfile)** element specifies the list of preferred network providers at the time of roaming.</span></span>

<span data-ttu-id="fc7c8-105">Il servizio Mobile Broadband usa questo elemento per selezionare la rete preferita da fornire durante il roaming.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-105">The Mobile Broadband service uses this element to select the preferred network provide while roaming.</span></span>

<span data-ttu-id="fc7c8-106">L'elemento ha l'elemento figlio seguente che deve essere definito almeno una volta, ma può essere definito più volte.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-106">The element has the following child element which must be defined at least once but can be defined multiple times.</span></span>

-   [<span data-ttu-id="fc7c8-107">**Provider**</span><span class="sxs-lookup"><span data-stu-id="fc7c8-107">**Provider**</span></span>](schema-provider-dataroamingpartners-element.md)

<span data-ttu-id="fc7c8-108">Questo elemento può avere un massimo di un'occorrenza.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-108">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="fc7c8-109">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-109">This element is optional.</span></span>

``` syntax
<xs:element name="DataRoamingPartners">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Provider"
                type="providerType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="fc7c8-110">L'elemento **DataRoamingPartners** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fc7c8-110">The **DataRoamingPartners** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fc7c8-111">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="fc7c8-111">Child elements</span></span>



| <span data-ttu-id="fc7c8-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="fc7c8-112">Element</span></span>                                                         | <span data-ttu-id="fc7c8-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc7c8-113">Type</span></span>                                                    | <span data-ttu-id="fc7c8-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc7c8-114">Description</span></span>                                            |
|-----------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="fc7c8-115">**Provider**</span><span class="sxs-lookup"><span data-stu-id="fc7c8-115">**Provider**</span></span>](schema-provider-dataroamingpartners-element.md) | [<span data-ttu-id="fc7c8-116">**providerType**</span><span class="sxs-lookup"><span data-stu-id="fc7c8-116">**providerType**</span></span>](schema-providertype-complextype.md) | <span data-ttu-id="fc7c8-117">Nome e ID del provider di una rete cellulare.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-117">Name and provider ID of a cellular network.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fc7c8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc7c8-118">Requirements</span></span>



| <span data-ttu-id="fc7c8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc7c8-119">Requirement</span></span> | <span data-ttu-id="fc7c8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fc7c8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="fc7c8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc7c8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fc7c8-122">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fc7c8-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="fc7c8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc7c8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fc7c8-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fc7c8-124">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="fc7c8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc7c8-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="fc7c8-126">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="fc7c8-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fc7c8-127">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="fc7c8-127">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="fc7c8-128">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="fc7c8-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fc7c8-129">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="fc7c8-129">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




