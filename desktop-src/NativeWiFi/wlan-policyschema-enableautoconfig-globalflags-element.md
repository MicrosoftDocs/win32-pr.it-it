---
description: Specifica se i computer utilizzano il servizio di configurazione automatica (AutoConfig) incorporato per gestire le connessioni wireless.
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
title: Elemento enableAutoConfig (globalFlags) (LAN_policy) per WLAN
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5105b8e634aa5affa8648b763a82bbd60cbaec17
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334399"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a><span data-ttu-id="7ff40-103">Elemento enableAutoConfig (globalFlags) (LAN_policy) per WLAN</span><span class="sxs-lookup"><span data-stu-id="7ff40-103">enableAutoConfig (globalFlags) Element (LAN_policy) for WLAN</span></span> 

<span data-ttu-id="7ff40-104">L'elemento **enableAutoConfig** (globalFlags) specifica se i computer utilizzano il servizio di configurazione automatica (AutoConfig) incorporato per gestire le connessioni wireless.</span><span class="sxs-lookup"><span data-stu-id="7ff40-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <span data-ttu-id="7ff40-105">Quando **enableAutoConfig** ha il valore false, i computer non devono usare la configurazione automatica per gestire le connessioni wireless e il servizio di configurazione automatica risponde solo alle richieste per abilitare il servizio.</span><span class="sxs-lookup"><span data-stu-id="7ff40-105">When **enableAutoConfig** has a value of FALSE, machines must not use AutoConfig to manage wireless connections, and the AutoConfig service only responds to requests to enable the service.</span></span> <span data-ttu-id="7ff40-106">Quando **enableAutoConfig** ha il valore true, i computer possono usare il servizio di configurazione automatica.</span><span class="sxs-lookup"><span data-stu-id="7ff40-106">When **enableAutoConfig** has a value of TRUE, machines may use the AutoConfig service.</span></span>

<span data-ttu-id="7ff40-107">Questo elemento è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7ff40-107">This element is mandatory.</span></span> <span data-ttu-id="7ff40-108">Quando un profilo viene creato dal servizio di configurazione automatica, questo elemento avrà il valore predefinito TRUE.</span><span class="sxs-lookup"><span data-stu-id="7ff40-108">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="7ff40-109">L'elemento **enableAutoConfig** è definito dall'elemento [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff40-109">The **enableAutoConfig** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ff40-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ff40-110">Requirements</span></span>



| <span data-ttu-id="7ff40-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ff40-111">Requirement</span></span> | <span data-ttu-id="7ff40-112">Valore</span><span class="sxs-lookup"><span data-stu-id="7ff40-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ff40-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ff40-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff40-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ff40-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7ff40-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ff40-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff40-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ff40-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ff40-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ff40-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="7ff40-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="7ff40-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7ff40-119">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="7ff40-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="7ff40-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="7ff40-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7ff40-121">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="7ff40-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




