---
description: Specifica se le reti negate vengono visualizzate nella procedura guidata Connetti a una rete.
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: Elemento showDeniedNetwork (globalFlags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- showDeniedNetwork
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33049dad00e5fda22e3f739d3dc200a282481a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527799"
---
# <a name="showdeniednetwork-globalflags-element"></a><span data-ttu-id="d18a9-103">Elemento showDeniedNetwork (globalFlags)</span><span class="sxs-lookup"><span data-stu-id="d18a9-103">showDeniedNetwork (globalFlags) Element</span></span>

<span data-ttu-id="d18a9-104">L'elemento **showDeniedNetwork** (globalFlags) specifica se le reti negate vengono visualizzate nella procedura guidata **Connetti a una rete** .</span><span class="sxs-lookup"><span data-stu-id="d18a9-104">The **showDeniedNetwork** (globalFlags) element specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <span data-ttu-id="d18a9-105">Le reti possono essere negate da criteri di gruppo o da impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="d18a9-105">Networks may be denied by group policy or by user settings.</span></span> <span data-ttu-id="d18a9-106">Quando **showDeniedNetwork** ha il valore true, le reti negate vengono visualizzate nella procedura guidata **Connetti a rete** ; in caso contrario, le reti negate non vengono visualizzate nella procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="d18a9-106">When **showDeniedNetwork** has a value of TRUE, denied networks appear in the **Connect to a Network** wizard; otherwise, denied networks do not appear in the wizard.</span></span>

<span data-ttu-id="d18a9-107">Questo elemento è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d18a9-107">This element is mandatory.</span></span> <span data-ttu-id="d18a9-108">Quando un profilo viene creato dal servizio di configurazione automatica, questo elemento prenderà il valore predefinito FALSE.</span><span class="sxs-lookup"><span data-stu-id="d18a9-108">When a profile is created by the AutoConfig service, this element will take the default value of FALSE.</span></span>

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

<span data-ttu-id="d18a9-109">L'elemento **showDeniedNetwork** è definito dall'elemento [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d18a9-109">The **showDeniedNetwork** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d18a9-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d18a9-110">Requirements</span></span>



| <span data-ttu-id="d18a9-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d18a9-111">Requirement</span></span> | <span data-ttu-id="d18a9-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d18a9-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d18a9-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d18a9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d18a9-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d18a9-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d18a9-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d18a9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d18a9-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d18a9-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d18a9-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d18a9-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="d18a9-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="d18a9-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d18a9-119">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="d18a9-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="d18a9-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="d18a9-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d18a9-121">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="d18a9-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




