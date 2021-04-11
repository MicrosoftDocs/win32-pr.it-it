---
description: Identifica il nome e l'ID del provider per una rete cellulare.
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: Elemento provider (DataRoamingPartners)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: b5b36c973bf44175b90e25fd2a141fed3624d8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129010"
---
# <a name="provider-dataroamingpartners-element"></a><span data-ttu-id="7af0c-103">Elemento provider (DataRoamingPartners)</span><span class="sxs-lookup"><span data-stu-id="7af0c-103">Provider (DataRoamingPartners) Element</span></span>

<span data-ttu-id="7af0c-104">L'elemento **provider (DataRoamingPartners)** identifica il nome e l'ID provider per una rete cellulare.</span><span class="sxs-lookup"><span data-stu-id="7af0c-104">The **Provider (DataRoamingPartners)** element identifies the name and provider ID for a cellular network.</span></span>

<span data-ttu-id="7af0c-105">Questo elemento ha gli elementi figlio seguenti.</span><span class="sxs-lookup"><span data-stu-id="7af0c-105">This element has the following child elements.</span></span>

-   [<span data-ttu-id="7af0c-106">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="7af0c-106">**ProviderID**</span></span>](schema-providerid-providertype-element.md)
-   [<span data-ttu-id="7af0c-107">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="7af0c-107">**ProviderName**</span></span>](schema-providername-providertype-element.md)

<span data-ttu-id="7af0c-108">Questo elemento può essere definito più volte all'interno dell'elemento [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7af0c-108">This element can be defined multiple times within the [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) element.</span></span> <span data-ttu-id="7af0c-109">Deve essere definito almeno una volta.</span><span class="sxs-lookup"><span data-stu-id="7af0c-109">It must be defined at least once.</span></span>

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

<span data-ttu-id="7af0c-110">L'elemento **provider** è definito dall'elemento [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7af0c-110">The **Provider** element is defined by the [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="7af0c-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7af0c-111">Requirements</span></span>



| <span data-ttu-id="7af0c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7af0c-112">Requirement</span></span> | <span data-ttu-id="7af0c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7af0c-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="7af0c-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7af0c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7af0c-115">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7af0c-115">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="7af0c-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7af0c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7af0c-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7af0c-117">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="7af0c-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7af0c-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="7af0c-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="7af0c-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7af0c-120">**DataRoamingPartners**</span><span class="sxs-lookup"><span data-stu-id="7af0c-120">**DataRoamingPartners**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="7af0c-121">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="7af0c-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7af0c-122">**DataRoamingPartners (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="7af0c-122">**DataRoamingPartners (MBNProfile)**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




