---
title: Come registrare un dispositivo con l'host del dispositivo
description: È possibile registrare un dispositivo in esecuzione o un dispositivo non in esecuzione.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3be1561d82741ce33e7eb05e63b015d5cb38f52
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044753"
---
# <a name="how-to-register-a-device-with-the-device-host"></a>Come registrare un dispositivo con l'host del dispositivo

È possibile registrare un dispositivo in esecuzione o un dispositivo non in esecuzione.

## <a name="registering-a-running-device"></a>Registrazione di un dispositivo in esecuzione

I dispositivi vengono registrati usando l'interfaccia [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) . Solo gli amministratori possono registrare i dispositivi in esecuzione. Per registrare un dispositivo che dispone di un oggetto controllo dispositivo in esecuzione, un'applicazione deve richiamare [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), passando quanto segue:

-   Testo della descrizione del dispositivo.
-   Puntatore **IUnknown** all'oggetto controllo dispositivo.
-   Una stringa di inizializzazione che viene passata al metodo [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) dell'oggetto controllo del dispositivo.
-   Percorso della directory delle risorse.
-   Durata del dispositivo.
-   Il parametro ID dispositivo (un parametro OUT), ovvero il valore restituito di questa chiamata; un puntatore all'ID dispositivo viene restituito in C++.

## <a name="registering-a-non-running-device"></a>Registrazione di un dispositivo non in esecuzione

Per impostazione predefinita, solo gli amministratori e gli utenti interattivi possono registrare dispositivi non in esecuzione. Per registrare un dispositivo con un oggetto controllo dispositivo che non è in esecuzione, l'applicazione usa il metodo [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) .

Per registrare a livello di codice un dispositivo con un oggetto controllo dispositivo non in esecuzione, l'applicazione deve richiamare [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) e passare i parametri seguenti:

-   Testo della descrizione del dispositivo.
-   ProgID dell'oggetto controllo dispositivo.
-   Una stringa di inizializzazione che viene passata al metodo [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) dell'oggetto controllo del dispositivo.
-   ID del contenitore.
-   Percorso della directory delle risorse.
-   Durata del dispositivo.
-   Il parametro ID dispositivo (un parametro OUT), ovvero il valore restituito di questa chiamata; un puntatore all'ID dispositivo viene restituito in C++.

Le registrazioni dei dispositivi non in esecuzione possono essere configurate in modo da renderle permanente tra gli avvii del sistema (i dispositivi non vengono pubblicati durante la fase di arresto). Se pertanto sono configurati in questo modo, i dispositivi vengono pubblicati e annunciati ogni volta che il computer viene avviato.

 

 




