---
title: Come registrare un dispositivo con l'host del dispositivo
description: È possibile registrare un dispositivo in esecuzione o un dispositivo non in esecuzione.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8425578dbd5ccc76685c2a142bee8d2167c4058341c32e4b03bcedca15041579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867581"
---
# <a name="how-to-register-a-device-with-the-device-host"></a>Come registrare un dispositivo con l'host del dispositivo

È possibile registrare un dispositivo in esecuzione o un dispositivo non in esecuzione.

## <a name="registering-a-running-device"></a>Registrazione di un dispositivo in esecuzione

I dispositivi vengono registrati tramite [**l'interfaccia IUPnPRegistrar.**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) Solo gli amministratori sono autorizzati a registrare i dispositivi in esecuzione. Per registrare un dispositivo che dispone di un oggetto controllo dispositivo in esecuzione, un'applicazione deve richiamare [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), passando quanto segue:

-   Testo della descrizione del dispositivo.
-   Puntatore **IUnknown** all'oggetto controllo dispositivo.
-   Stringa di inizializzazione passata al metodo [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) dell'oggetto controllo dispositivo.
-   Percorso della directory delle risorse.
-   Durata del dispositivo.
-   Il parametro ID dispositivo (un parametro OUT), che è il valore restituito di questa chiamata; In C++ viene restituito un puntatore all'ID dispositivo.

## <a name="registering-a-non-running-device"></a>Registrazione di un dispositivo non in esecuzione

Per impostazione predefinita, solo gli amministratori e gli utenti interattivi sono autorizzati a registrare i dispositivi non in esecuzione. Per registrare un dispositivo con un oggetto controllo dispositivo non in esecuzione, l'applicazione usa il [**metodo IUPnPRegistrar::RegisterDevice.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice)

Per registrare un dispositivo a livello di codice con un oggetto controllo dispositivo non in esecuzione, l'applicazione deve richiamare [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) e passare i parametri seguenti:

-   Testo della descrizione del dispositivo.
-   ProgID dell'oggetto controllo dispositivo.
-   Stringa di inizializzazione passata al metodo [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) dell'oggetto controllo dispositivo.
-   ID del contenitore.
-   Percorso della directory delle risorse.
-   Durata del dispositivo.
-   Il parametro ID dispositivo (un parametro OUT), che è il valore restituito di questa chiamata; In C++ viene restituito un puntatore all'ID dispositivo.

Le registrazioni dei dispositivi non in esecuzione possono essere configurate in modo da essere mantenute tra gli avviamenti del sistema (i dispositivi non vengono pubblicati durante la fase di arresto). Pertanto, se sono configurati in questo modo, i dispositivi vengono pubblicati e annunciati ogni volta che il computer viene avviato.

 

 




