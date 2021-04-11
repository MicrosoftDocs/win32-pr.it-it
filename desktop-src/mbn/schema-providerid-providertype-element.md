---
description: Specifica l'ID del provider della rete cellulare.
ms.assetid: 5528dfec-eb1b-4af3-8d7d-03b458e5ae75
title: Elemento ProviderID (providerType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderID
api_type:
- Schema
ms.openlocfilehash: 750e6c3f4397f710bb1ccbcea0286be68a89e145
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226191"
---
# <a name="providerid-providertype-element"></a><span data-ttu-id="147d5-103">Elemento ProviderID (providerType)</span><span class="sxs-lookup"><span data-stu-id="147d5-103">ProviderID (providerType) Element</span></span>

<span data-ttu-id="147d5-104">L'elemento **ProviderID (ProviderType)** specifica l'ID del provider della rete cellulare.</span><span class="sxs-lookup"><span data-stu-id="147d5-104">The **ProviderID (providerType)** element specifies the provider ID of the cellular network.</span></span>

<span data-ttu-id="147d5-105">L'elemento è una sequenza di cifre con un massimo di 6 cifre.</span><span class="sxs-lookup"><span data-stu-id="147d5-105">The element is a sequence of digits with a maximum of 6 digits.</span></span>

<span data-ttu-id="147d5-106">Questo elemento è obbligatorio nell'elemento [**provider**](schema-provider-dataroamingpartners-element.md) .</span><span class="sxs-lookup"><span data-stu-id="147d5-106">This element is required within the [**Provider**](schema-provider-dataroamingpartners-element.md) element.</span></span>

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

<span data-ttu-id="147d5-107">L'elemento **ProviderID** è definito dal tipo complesso [**ProviderType**](schema-providertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="147d5-107">The **ProviderID** element is defined by the [**providerType**](schema-providertype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="147d5-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="147d5-108">Requirements</span></span>



| <span data-ttu-id="147d5-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="147d5-109">Requirement</span></span> | <span data-ttu-id="147d5-110">Valore</span><span class="sxs-lookup"><span data-stu-id="147d5-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="147d5-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="147d5-111">Minimum supported client</span></span><br/> | <span data-ttu-id="147d5-112">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="147d5-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="147d5-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="147d5-113">Minimum supported server</span></span><br/> | <span data-ttu-id="147d5-114">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="147d5-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="147d5-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="147d5-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="147d5-116">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="147d5-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="147d5-117">**providerType**</span><span class="sxs-lookup"><span data-stu-id="147d5-117">**providerType**</span></span>](schema-providertype-complextype.md)
</dt> <dt>

<span data-ttu-id="147d5-118">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="147d5-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="147d5-119">**Provider (DataRoamingPartners)**</span><span class="sxs-lookup"><span data-stu-id="147d5-119">**Provider (DataRoamingPartners)**</span></span>](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




