---
title: Annullamento della registrazione di un dispositivo
description: Usare il metodo IUPnPRegistrar UnregisterDevice per annullare la registrazione di un dispositivo.
ms.assetid: 4f7624e3-4d60-406d-8521-1dfc9aee4408
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c480433e3d8dbf4ff823728281018801ec35c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471667"
---
# <a name="unregistering-a-device"></a><span data-ttu-id="fa315-103">Annullamento della registrazione di un dispositivo</span><span class="sxs-lookup"><span data-stu-id="fa315-103">Unregistering a Device</span></span>

<span data-ttu-id="fa315-104">Usare il metodo [**IUPnPRegistrar:: UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice) per annullare la registrazione di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa315-104">Use the [**IUPnPRegistrar::UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice) method to unregister a device.</span></span> <span data-ttu-id="fa315-105">È possibile annullare la registrazione del dispositivo (rimosso dall'host del dispositivo) temporaneamente o in modo permanente, a seconda del valore di *fPermanent*.</span><span class="sxs-lookup"><span data-stu-id="fa315-105">The device can be unregistered (removed from the device host) temporarily or permanently, depending on the value of *fPermanent*.</span></span> <span data-ttu-id="fa315-106">Gli sviluppatori devono rimuovere temporaneamente i dispositivi se i dispositivi verranno registrati di nuovo e i dispositivi devono usare lo stesso UDN.</span><span class="sxs-lookup"><span data-stu-id="fa315-106">Developers should remove devices temporarily if the devices will be re-registered, and the devices should use the same UDN.</span></span> <span data-ttu-id="fa315-107">In caso contrario, i dispositivi vengono rimossi in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="fa315-107">Otherwise, the devices are removed permanently.</span></span>

<span data-ttu-id="fa315-108">Il GUID utilizzato per annullare la registrazione non è UDN.</span><span class="sxs-lookup"><span data-stu-id="fa315-108">The GUID used to unregister is not the UDN.</span></span> <span data-ttu-id="fa315-109">È necessario usare l'ID restituito da [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) o [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).</span><span class="sxs-lookup"><span data-stu-id="fa315-109">You must use the ID returned to you by [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) or [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).</span></span>

> [!Note]  
> <span data-ttu-id="fa315-110">È possibile rilasciare l'oggetto [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) .</span><span class="sxs-lookup"><span data-stu-id="fa315-110">You can release the [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) object.</span></span> <span data-ttu-id="fa315-111">Solo l'ID deve essere memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="fa315-111">Only the ID must be cached.</span></span>

 

<span data-ttu-id="fa315-112">Se *fPermanent* è **false**, il dispositivo viene rimosso temporaneamente.</span><span class="sxs-lookup"><span data-stu-id="fa315-112">If *fPermanent* is **FALSE**, the device is removed temporarily.</span></span> <span data-ttu-id="fa315-113">Usare l'interfaccia [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar) per registrare nuovamente il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa315-113">Use [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar) interface to re-register the device.</span></span> <span data-ttu-id="fa315-114">I metodi [**IUPnPReregistrar:: ReregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterdevice) e [**IUPnPReregistrar:: ReregisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterrunningdevice) usano lo stesso UDN o UDNs, nel caso di dispositivi annidati, generati in precedenza dall'host del dispositivo per il dispositivo non registrato.</span><span class="sxs-lookup"><span data-stu-id="fa315-114">The [**IUPnPReregistrar::ReregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterdevice) and [**IUPnPReregistrar::ReregisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterrunningdevice) methods use the same UDN or UDNs, in the case of nested devices, previously generated by the device host for the unregistered device.</span></span>

<span data-ttu-id="fa315-115">Se *fPermanent* è **true**, il dispositivo viene rimosso definitivamente dall'host del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa315-115">If *fPermanent* is **TRUE**, the device is permanently removed from the device host.</span></span> <span data-ttu-id="fa315-116">Se si registra nuovamente questo dispositivo nello stesso computer, viene creato un UDN diverso da quello creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="fa315-116">Registering this device again on the same computer creates a different UDN than the one previously created.</span></span>

> [!Note]  
> <span data-ttu-id="fa315-117">Quando un dispositivo viene registrato più volte nello stesso computer, l'host del dispositivo genera UDNs diversi per ogni istanza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa315-117">When a device is registered multiple times on the same computer, the device host generates different UDNs for each instance of the device.</span></span>

 

 

 




