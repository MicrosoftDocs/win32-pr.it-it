---
title: Annullamento della registrazione di un dispositivo
description: Usare il metodo IUPnPRegistrar UnregisterDevice per annullare la registrazione di un dispositivo.
ms.assetid: 4f7624e3-4d60-406d-8521-1dfc9aee4408
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ff8eeb99ec0ba697c301e8cc15100bd06c0323b95f4099329c46729ceba9c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999491"
---
# <a name="unregistering-a-device"></a>Annullamento della registrazione di un dispositivo

Usare il [**metodo IUPnPRegistrar::UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice) per annullare la registrazione di un dispositivo. Il dispositivo può essere annullato (rimosso dall'host del dispositivo) temporaneamente o definitivamente, a seconda del valore di *fPermanent*. Gli sviluppatori devono rimuovere temporaneamente i dispositivi se i dispositivi verranno registrati nuovamente e i dispositivi devono usare la stessa rete definita dall'utente. In caso contrario, i dispositivi vengono rimossi in modo permanente.

Il GUID usato per annullare la registrazione non è il nome definito dall'utente. È necessario usare l'ID restituito da [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) o [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).

> [!Note]  
> È possibile rilasciare [**l'oggetto IUPnPRegistrar.**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) Solo l'ID deve essere memorizzato nella cache.

 

Se *fPermanent* è **FALSE,** il dispositivo viene rimosso temporaneamente. Usare [**l'interfaccia IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar) per registrare nuovamente il dispositivo. I metodi [**IUPnPReregistrar::ReregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterdevice) e [**IUPnPReregistrar::ReregisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterrunningdevice) usano gli stessi UDN o UNS, nel caso di dispositivi annidati, generati in precedenza dall'host del dispositivo per il dispositivo non registrato.

Se *fPermanent è* **TRUE,** il dispositivo viene rimosso definitivamente dall'host del dispositivo. La registrazione di questo dispositivo nello stesso computer crea una rete definita dall'utente diversa da quella creata in precedenza.

> [!Note]  
> Quando un dispositivo viene registrato più volte nello stesso computer, l'host del dispositivo genera nomi definiti dall'utente diversi per ogni istanza del dispositivo.

 

 

 




