---
description: Determina il comportamento di roaming di una rete connessa automaticamente quando una rete più preferita è compresa nell'intervallo.
ms.assetid: 095dc797-1249-43aa-a8b7-5fa6eaee2a74
title: Elemento autoswitch (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- autoSwitch
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7ae05b18f58927e05c952edbbfc1b6a6190cec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879990"
---
# <a name="autoswitch-wlanprofile-element"></a><span data-ttu-id="5c628-103">Elemento autoswitch (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="5c628-103">autoSwitch (WLANProfile) Element</span></span>

<span data-ttu-id="5c628-104">L'elemento autoswitch (WLANProfile) determina il comportamento di roaming di una rete connessa automaticamente quando una rete più preferita è compresa nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="5c628-104">The autoSwitch (WLANProfile) element determines the roaming behavior of an auto-connected network when a more preferred network is in range.</span></span> <span data-ttu-id="5c628-105">.</span><span class="sxs-lookup"><span data-stu-id="5c628-105">.</span></span> <span data-ttu-id="5c628-106">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5c628-106">This element is optional.</span></span>

<span data-ttu-id="5c628-107">Se autoswitch è "true" e [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) è impostato su "auto", è necessario tentare una connessione a una rete più preferita ogni volta che una rete preferita entra in campo.</span><span class="sxs-lookup"><span data-stu-id="5c628-107">If autoSwitch is "true" and [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "auto", a connection to a more preferred network must be attempted whenever a more preferred network comes into range.</span></span> <span data-ttu-id="5c628-108">Una rete più preferita è quella che viene ordinata più in alto nell'elenco delle reti wireless preferite.</span><span class="sxs-lookup"><span data-stu-id="5c628-108">A more preferred network is one that is ordered higher in the list of preferred wireless networks.</span></span> <span data-ttu-id="5c628-109">Questo tentativo di connessione viene eseguito quando si è connessi a un'altra rete.</span><span class="sxs-lookup"><span data-stu-id="5c628-109">This connection attempt occurs when connected to another network.</span></span>

<span data-ttu-id="5c628-110">Se [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) è impostato su "auto", questo valore può essere "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="5c628-110">If [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "auto", this value can be either "true" or "false".</span></span>

<span data-ttu-id="5c628-111">Se [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) è impostato su "Manual", questo valore deve essere impostato su "false".</span><span class="sxs-lookup"><span data-stu-id="5c628-111">If [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "manual", this value must be set to "false".</span></span> <span data-ttu-id="5c628-112">Questo elemento non ha alcun effetto su una rete connessa manualmente.</span><span class="sxs-lookup"><span data-stu-id="5c628-112">This element has no effect on a manually connected network.</span></span>

<span data-ttu-id="5c628-113">Un valore di autoswitch impostato su "true" comporta una frequenza maggiore di analisi periodica per le nuove reti.</span><span class="sxs-lookup"><span data-stu-id="5c628-113">An autoSwitch value set to "true" results in a higher frequency of periodic scanning for new networks.</span></span> <span data-ttu-id="5c628-114">Questo può comportare un aumento dell'inquinamento della frequenza radio da queste analisi periodiche e un maggiore consumo di energia usato dalla scheda di rete wireless.</span><span class="sxs-lookup"><span data-stu-id="5c628-114">This may result in increased radio frequency pollution from these periodic scans and increased power consumption used by the wireless network adapter.</span></span>

<span data-ttu-id="5c628-115">**Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato:** Le modifiche sono implementate in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato per ottimizzare le prestazioni di rete wireless.</span><span class="sxs-lookup"><span data-stu-id="5c628-115">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="5c628-116">Queste modifiche sono progettate per ridurre l'inquinamento della frequenza radio, il consumo di energia e l'interruzione del traffico in tempo reale su reti wireless.</span><span class="sxs-lookup"><span data-stu-id="5c628-116">These changes are designed to reduce radio frequency pollution, power consumption, and disruption to real-time traffic over wireless networks.</span></span> <span data-ttu-id="5c628-117">L'impostazione predefinita per il **commutatore autoswitch** quando questo elemento non è impostato in un profilo LAN wireless è cambiata.</span><span class="sxs-lookup"><span data-stu-id="5c628-117">The default setting for **autoSwitch** when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="5c628-118">L'impostazione predefinita viene modificata in "false" in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato.</span><span class="sxs-lookup"><span data-stu-id="5c628-118">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="5c628-119">L'impostazione predefinita è "true" in Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5c628-119">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="5c628-120">È consigliabile che il valore dell'elemento **autoswitch** utilizzato da un'applicazione in un profilo LAN wireless sia impostato su "false" per ridurre la frequenza di analisi periodica per le nuove reti, a meno che non sia assolutamente necessario che un'applicazione imposti questo valore su "true".</span><span class="sxs-lookup"><span data-stu-id="5c628-120">It is recommended that the value of the **autoSwitch** element used by an application in a wireless LAN profile be set to "false" to reduce the frequency of periodic scanning for new networks, unless it is absolutely necessary for an application to set this value to "true".</span></span>

<span data-ttu-id="5c628-121">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5c628-121">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="autoSwitch"
    type="boolean"
 />
```

<span data-ttu-id="5c628-122">L'elemento **autoswitch** viene definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5c628-122">The **autoSwitch** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="5c628-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c628-123">Examples</span></span>

<span data-ttu-id="5c628-124">Per visualizzare i profili di esempio che usano l'elemento **autoswitch** , vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="5c628-124">To view sample profiles that use the **autoSwitch** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c628-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c628-125">Requirements</span></span>



| <span data-ttu-id="5c628-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c628-126">Requirement</span></span> | <span data-ttu-id="5c628-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5c628-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c628-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c628-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5c628-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c628-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5c628-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c628-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5c628-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c628-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c628-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c628-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="5c628-133">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="5c628-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5c628-134">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="5c628-134">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="5c628-135">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="5c628-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5c628-136">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="5c628-136">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




