---
title: Considerazioni sulla sicurezza dell'host del dispositivo
description: L'uso dell'host del dispositivo crea problemi di sicurezza.
ms.assetid: 7cb445ea-5df4-4030-babd-62527b4d6210
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4e8cdce90cdc5801010833db4cb97c49487c16a3926bf235f126f33e1078f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008091"
---
# <a name="device-host-security-considerations"></a>Considerazioni sulla sicurezza dell'host del dispositivo

L'uso dell'host del dispositivo crea problemi di sicurezza per i motivi seguenti:

-   I dispositivi ospitati in un computer che esegue Windows XP inviano annunci su tutte le reti.
-   I dispositivi ospitati in un computer che esegue Windows XP consentono il controllo dei dispositivi da tutte le reti.

Ciò aumenta il rischio per gli utenti privati, perché i dispositivi come un lettore multimediale o un'illuminazione con bridge o un sistema HVAC ospitato in un computer che esegue Windows XP sono visibili e possono essere controllati dai punti di controllo all'esterno della casa.

Quando si crea un dispositivo ospitato, è necessario prendere in considerazione alcuni problemi di sicurezza.

-   Per ridurre l'ambito di individuazione e attacco dei dispositivi basati su UPnP, il TTL di tutti i messaggi SSDP è 1. Ciò significa che un dispositivo registrato viene individuato solo dai punti di controllo nella stessa rete. È possibile configurare un TTL superiore nel Registro di sistema.
-   La registrazione di un dispositivo non in esecuzione richiede la preregistrazione del dispositivo .dll con COM, che richiede privilegi di amministratore.
-   La registrazione di un dispositivo in esecuzione richiede privilegi di amministratore, servizio locale o sistema locale.
-   Quando l'host del dispositivo viene avviato, viene eseguito come [LocalService](/windows/desktop/Services/localservice-account). In questo modo il dispositivo può generare controlli e leggere la chiave del Registro di sistema **HKEY \_ LOCAL \_ MACHINE.** Il dispositivo ha accesso a **HKEY \_ CURRENT \_ USER**. L'account LocalService può usare le risorse a cui a LocalService è stato concesso l'accesso, nonché quelle che concedono l'accesso a AuthenticatedUser. Il dispositivo ha limitato l'file system accesso.
-   Gli file system ACL devono essere aggiornati per consentire a [LocalService l'accesso](/windows/desktop/Services/localservice-account) alla directory delle risorse.
-   Se il dispositivo deve avere più accesso di sicurezza, è possibile creare un processo personalizzato per il dispositivo e registrarlo usando [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).

 

 