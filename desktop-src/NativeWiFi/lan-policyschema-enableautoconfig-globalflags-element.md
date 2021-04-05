---
description: Specifica se i computer utilizzano il servizio di configurazione automatica incorporato per gestire le connessioni a reti cablate che richiedono l'autenticazione di livello 2, ad esempio 802.1 X.
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: Elemento enableAutoConfig (globalFlags) (LAN_policy)
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
ms.openlocfilehash: af1ca32f177140bbfc6563f74df5afc519ee0c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757799"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a><span data-ttu-id="d6693-103">Elemento enableAutoConfig (globalFlags) (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="d6693-103">enableAutoConfig (globalFlags) Element (LAN_policy)</span></span>

<span data-ttu-id="d6693-104">L'elemento **enableAutoConfig** (globalFlags) specifica se i computer utilizzano il servizio di configurazione automatica incorporato per gestire le connessioni a reti cablate che richiedono l'autenticazione di livello 2, ad esempio 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="d6693-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span>

<span data-ttu-id="d6693-105">Se il valore di **enableAutoConfig** è false, i computer non devono usare il servizio di configurazione automatica incorporato per gestire le connessioni che richiedono l'autenticazione di livello 2.</span><span class="sxs-lookup"><span data-stu-id="d6693-105">When **enableAutoConfig** has a value of FALSE, machines must not use built-in automatic configuration service to manage connections that require layer 2 authentication.</span></span> <span data-ttu-id="d6693-106">La rete specificata nell'elemento [**Profiler**](lan-policyschema-profilelist-lanpolicy-element.md) è invece l'unica rete disponibile per la connessione.</span><span class="sxs-lookup"><span data-stu-id="d6693-106">Instead, the network specified in the [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md) element is the only network available for connection.</span></span> <span data-ttu-id="d6693-107">Il servizio di configurazione automatica risponderà solo alle richieste di abilitazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="d6693-107">The automatic configuration service will only respond to requests to enable the service.</span></span>

<span data-ttu-id="d6693-108">Quando **enableAutoConfig** ha il valore true, i computer possono usare il servizio di configurazione automatica incorporato per connettersi alle reti cablate che richiedono l'autenticazione di livello 2.</span><span class="sxs-lookup"><span data-stu-id="d6693-108">When **enableAutoConfig** has a value of TRUE, machines may use the built-in automatic configuration service to connect to wired networks that require layer 2 authentication.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="d6693-109">L'elemento **enableAutoConfig** è definito dall'elemento [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d6693-109">The **enableAutoConfig** element is defined by the [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6693-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6693-110">Requirements</span></span>



| <span data-ttu-id="d6693-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6693-111">Requirement</span></span> | <span data-ttu-id="d6693-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d6693-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d6693-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6693-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d6693-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6693-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d6693-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6693-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d6693-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6693-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6693-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6693-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6693-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="d6693-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d6693-119">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="d6693-119">**globalFlags**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="d6693-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="d6693-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d6693-121">**globalFlags (LANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="d6693-121">**globalFlags (LANPolicy)**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 




