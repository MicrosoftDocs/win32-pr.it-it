---
description: Contiene le impostazioni globali per il modulo di configurazione automatica (ACM).
ms.assetid: fb2b96d0-38cc-44fe-a82a-97e73b6a8f2a
title: Elemento globalFlags (WLANPolicy)
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
ms.openlocfilehash: 97d0b8ee90407efd94ac46cc1df6b084b9dcc54d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530091"
---
# <a name="globalflags-wlanpolicy-element"></a><span data-ttu-id="c6414-103">Elemento globalFlags (WLANPolicy)</span><span class="sxs-lookup"><span data-stu-id="c6414-103">globalFlags (WLANPolicy) Element</span></span>

<span data-ttu-id="c6414-104">L'elemento globalFlags (WLANPolicy) contiene le impostazioni globali per il modulo di configurazione automatica (ACM).</span><span class="sxs-lookup"><span data-stu-id="c6414-104">The globalFlags (WLANPolicy) element contains the global settings for the Auto Configuration Module (ACM).</span></span> <span data-ttu-id="c6414-105">Questo elemento è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c6414-105">This element is mandatory.</span></span>

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
            <xs:element name="showDeniedNetwork"
                type="boolean"
             />
            <xs:element name="allowEveryoneToCreateAllUserProfiles"
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

<span data-ttu-id="c6414-106">L'elemento **globalFlags** è definito dall'elemento [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c6414-106">The **globalFlags** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c6414-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c6414-107">Child elements</span></span>



| <span data-ttu-id="c6414-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c6414-108">Element</span></span>                                                                                                                    | <span data-ttu-id="c6414-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6414-109">Type</span></span>    | <span data-ttu-id="c6414-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6414-110">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6414-111">**allowEveryoneToCreateAllUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="c6414-111">**allowEveryoneToCreateAllUserProfiles**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | <span data-ttu-id="c6414-112">boolean</span><span class="sxs-lookup"><span data-stu-id="c6414-112">boolean</span></span> | <span data-ttu-id="c6414-113">Specifica se un utente può creare un profilo per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="c6414-113">Specifies whether any user can create an all-user profile.</span></span> <br/>                                                               |
| [<span data-ttu-id="c6414-114">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="c6414-114">**enableAutoConfig**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | <span data-ttu-id="c6414-115">boolean</span><span class="sxs-lookup"><span data-stu-id="c6414-115">boolean</span></span> | <span data-ttu-id="c6414-116">Specifica se i computer utilizzano il servizio di configurazione automatica (AutoConfig) incorporato per gestire le connessioni wireless.</span><span class="sxs-lookup"><span data-stu-id="c6414-116">Specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <br/> |
| [<span data-ttu-id="c6414-117">**showDeniedNetwork**</span><span class="sxs-lookup"><span data-stu-id="c6414-117">**showDeniedNetwork**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | <span data-ttu-id="c6414-118">boolean</span><span class="sxs-lookup"><span data-stu-id="c6414-118">boolean</span></span> | <span data-ttu-id="c6414-119">Specifica se le reti negate vengono visualizzate nella procedura guidata **Connetti a una rete** .</span><span class="sxs-lookup"><span data-stu-id="c6414-119">Specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <br/>                                         |



## <a name="requirements"></a><span data-ttu-id="c6414-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6414-120">Requirements</span></span>



| <span data-ttu-id="c6414-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6414-121">Requirement</span></span> | <span data-ttu-id="c6414-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c6414-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c6414-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6414-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c6414-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6414-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c6414-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6414-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c6414-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c6414-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6414-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6414-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="c6414-128">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="c6414-128">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c6414-129">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="c6414-129">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="c6414-130">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="c6414-130">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c6414-131">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="c6414-131">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




