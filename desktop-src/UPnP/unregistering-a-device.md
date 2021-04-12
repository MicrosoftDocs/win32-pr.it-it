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
# <a name="unregistering-a-device"></a>Annullamento della registrazione di un dispositivo

Usare il metodo [**IUPnPRegistrar:: UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice) per annullare la registrazione di un dispositivo. È possibile annullare la registrazione del dispositivo (rimosso dall'host del dispositivo) temporaneamente o in modo permanente, a seconda del valore di *fPermanent*. Gli sviluppatori devono rimuovere temporaneamente i dispositivi se i dispositivi verranno registrati di nuovo e i dispositivi devono usare lo stesso UDN. In caso contrario, i dispositivi vengono rimossi in modo permanente.

Il GUID utilizzato per annullare la registrazione non è UDN. È necessario usare l'ID restituito da [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) o [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).

> [!Note]  
> È possibile rilasciare l'oggetto [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) . Solo l'ID deve essere memorizzato nella cache.

 

Se *fPermanent* è **false**, il dispositivo viene rimosso temporaneamente. Usare l'interfaccia [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar) per registrare nuovamente il dispositivo. I metodi [**IUPnPReregistrar:: ReregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterdevice) e [**IUPnPReregistrar:: ReregisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterrunningdevice) usano lo stesso UDN o UDNs, nel caso di dispositivi annidati, generati in precedenza dall'host del dispositivo per il dispositivo non registrato.

Se *fPermanent* è **true**, il dispositivo viene rimosso definitivamente dall'host del dispositivo. Se si registra nuovamente questo dispositivo nello stesso computer, viene creato un UDN diverso da quello creato in precedenza.

> [!Note]  
> Quando un dispositivo viene registrato più volte nello stesso computer, l'host del dispositivo genera UDNs diversi per ogni istanza del dispositivo.

 

 

 




