---
description: Contiene le impostazioni globali per la configurazione automatica delle reti cablate.
ms.assetid: 172cf15c-cd51-43d4-ae5d-f9460c2a40e2
title: Elemento globalFlags (LANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c9a244fbbc616e3092e2293fe187da1d7be0fa53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232431"
---
# <a name="globalflags-lanpolicy-element"></a><span data-ttu-id="593cd-103">Elemento globalFlags (LANPolicy)</span><span class="sxs-lookup"><span data-stu-id="593cd-103">globalFlags (LANPolicy) Element</span></span>

<span data-ttu-id="593cd-104">L'elemento globalFlags (LANPolicy) contiene le impostazioni globali per la configurazione automatica delle reti cablate.</span><span class="sxs-lookup"><span data-stu-id="593cd-104">The globalFlags (LANPolicy) element contains the global settings for the automatic configuration of wired networks.</span></span>

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
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

<span data-ttu-id="593cd-105">L'elemento **globalFlags** è definito dall'elemento [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="593cd-105">The **globalFlags** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="593cd-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="593cd-106">Child elements</span></span>



| <span data-ttu-id="593cd-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="593cd-107">Element</span></span>                                                                           | <span data-ttu-id="593cd-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="593cd-108">Type</span></span>    | <span data-ttu-id="593cd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="593cd-109">Description</span></span>                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="593cd-110">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="593cd-110">**enableAutoConfig**</span></span>](lan-policyschema-enableautoconfig-globalflags-element.md) | <span data-ttu-id="593cd-111">boolean</span><span class="sxs-lookup"><span data-stu-id="593cd-111">boolean</span></span> | <span data-ttu-id="593cd-112">Specifica se i computer utilizzano il servizio di configurazione automatica incorporato per gestire le connessioni a reti cablate che richiedono l'autenticazione di livello 2, ad esempio 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="593cd-112">Specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="593cd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="593cd-113">Requirements</span></span>



| <span data-ttu-id="593cd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="593cd-114">Requirement</span></span> | <span data-ttu-id="593cd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="593cd-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="593cd-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="593cd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="593cd-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="593cd-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="593cd-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="593cd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="593cd-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="593cd-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="593cd-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="593cd-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="593cd-121">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="593cd-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="593cd-122">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="593cd-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="593cd-123">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="593cd-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="593cd-124">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="593cd-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




