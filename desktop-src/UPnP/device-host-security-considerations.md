---
title: Considerazioni sulla sicurezza dell'host del dispositivo
description: L'uso dell'host del dispositivo crea problemi di sicurezza.
ms.assetid: 7cb445ea-5df4-4030-babd-62527b4d6210
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5a51b90bff33949a33cd9fa1046deb1916ab30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473403"
---
# <a name="device-host-security-considerations"></a>Considerazioni sulla sicurezza dell'host del dispositivo

L'uso dell'host del dispositivo crea problemi di sicurezza a causa dei seguenti elementi:

-   I dispositivi ospitati in un computer che esegue Windows XP inviano annunci su tutte le reti.
-   I dispositivi ospitati in un computer che esegue Windows XP consentono di controllare i dispositivi di tutte le reti.

Questo aumenta il rischio per i consumer privati, perché i dispositivi come un lettore multimediale o un sistema di illuminazione o HVAC con Bridge ospitato in un computer che esegue Windows XP sono visibili e possono essere controllati da punti di controllo fuori dalla Home.

Quando si crea un dispositivo ospitato, è necessario prendere in considerazione alcuni problemi di sicurezza.

-   Per ridurre l'ambito di individuazione e attacco di dispositivi basati su UPnP, il valore TTL di tutti i messaggi di SSDP è 1. Ciò significa che un dispositivo registrato viene individuato solo dai punti di controllo nella stessa rete. È possibile configurare una durata (TTL) superiore nel registro di sistema.
-   Per la registrazione di un dispositivo non in esecuzione è necessario pre-registrare il file device. dll con COM, che richiede privilegi di amministratore.
-   Per la registrazione di un dispositivo in esecuzione sono necessari privilegi di amministratore, servizio locale o sistema locale.
-   Quando l'host del dispositivo viene avviato, viene eseguito come [LocalService](/windows/desktop/Services/localservice-account). Ciò consente al dispositivo di generare controlli e leggere la chiave del registro di sistema del **\_ \_ computer locale HKEY** . Il dispositivo ha accesso all' **\_ \_ utente corrente di HKEY**. L'account LocalService può usare le risorse a cui è stato concesso l'accesso a LocalService, oltre a quelle che concedono l'accesso a AuthenticatedUser. Il dispositivo ha limitato l'accesso file system.
-   Gli ACL file system devono essere aggiornati per consentire l'accesso [LocalService](/windows/desktop/Services/localservice-account) alla directory delle risorse.
-   Se il dispositivo deve disporre di un accesso più sicuro, è possibile creare un processo personalizzato per il dispositivo e registrarlo usando [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).

 

 