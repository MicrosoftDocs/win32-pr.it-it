---
title: Provider di dispositivi
description: I provider di dispositivi sono oggetti registrati che il computer inizia a ogni avvio del sistema.
ms.assetid: 80c08993-0a8b-4ee9-93cd-bcc3c00e843b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67fac270342830045fc3bac9f0573f283d87dc6a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117862"
---
# <a name="device-providers"></a>Provider di dispositivi

I provider di dispositivi sono oggetti registrati che il computer inizia a ogni avvio del sistema. I provider di dispositivi registrano e annullano la registrazione dei dispositivi in esecuzione con l'host del dispositivo in risposta a un evento. Questi dispositivi sono dispositivi che sono stati avviati automaticamente al momento dell'avvio del sistema. Per motivi di sicurezza, un provider di dispositivi deve essere in genere eseguito come [LocalService](/windows/desktop/Services/localservice-account), anziché [LocalSystem](/windows/desktop/Services/localsystem-account).

I provider di dispositivi possono essere usati per i dispositivi temporanei. I provider di dispositivi possono anche essere usati per collegare i dispositivi ai supporti sottoposti a polling. Ad esempio, un dispositivo periferico, ad esempio un lettore musicale digitale, è connesso a un computer tramite una porta seriale. Per esporre Music Player come dispositivo basato su UPnP, sono necessari un oggetto controllo dispositivo e un set di oggetti servizio. Questi oggetti implementano le azioni lettore musicale basate su UPnP come comandi seriali. Tuttavia, il lettore musicale deve essere collegato alla porta seriale e disponibile per il controllo prima che questi oggetti vengano registrati.

Poiché la porta seriale non offre un meccanismo di notifica esplicito quando i dispositivi sono connessi, è necessario il codice di polling. Questo codice può essere implementato in un oggetto provider di dispositivi, in un servizio o in un'applicazione autonoma. Quando il computer viene avviato, l'host del dispositivo crea un'istanza dell'oggetto provider di dispositivi e quindi richiama il metodo [**Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) . Quando il provider di dispositivi rileva la presenza di un dispositivo Music Player, crea un'istanza dell'oggetto di controllo del dispositivo appropriato e lo registra chiamando [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice). Questo metodo pubblica il dispositivo e lo annuncia alla rete basata su UPnP.

La stessa funzionalità può essere eseguita anche implementando un servizio che esegue il polling della porta seriale. Tuttavia, i provider di dispositivi semplificano le operazioni richiedendo solo le funzionalità di base, ovvero il polling, da implementare perché i provider di dispositivi si basano sull'host del dispositivo per avviarli e arrestarli. L'uso di provider di dispositivi è più semplice dell'implementazione di un servizio.

Al momento della registrazione e, a ogni avvio del sistema successivo, il computer crea un'istanza dell'oggetto provider di dispositivi e quindi richiama il metodo [**IUPnPDeviceProvider:: Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) , passandogli la stringa di inizializzazione specificata durante la registrazione.

Una volta chiamato il metodo [**Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) , il provider di dispositivi esegue tutte le operazioni di elaborazione necessarie e, quando necessario, il provider di dispositivi registra i dispositivi chiamando [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), come descritto nella sezione [registrazione di un dispositivo ospitato con l'host del dispositivo](registering-a-hosted-device-with-the-device-host.md).

Quando il computer viene arrestato, l'host del dispositivo richiama il metodo [**IUPnPDeviceProvider:: Stop**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-stop) per indicare che il provider di dispositivi termina le operazioni.

 

 