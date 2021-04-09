---
description: Le funzioni seguenti vengono usate per la gestione dei dispositivi.
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: Funzioni di gestione dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587778b489b16355046b0b5af5cbba31c1a39639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966086"
---
# <a name="device-management-functions"></a>Funzioni di gestione dei dispositivi

Le funzioni seguenti vengono usate per la gestione dei dispositivi.



| Funzione                                                             | Descrizione                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | Invia un codice di controllo direttamente a un driver di dispositivo specificato.                           |
| [**InstallNewDevice**](installnewdevice.md)                         | Installa un nuovo dispositivo. All'utente viene richiesto di selezionare il dispositivo.                     |
| [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | Registra il dispositivo o il tipo di dispositivo per il quale una finestra riceverà le notifiche. |
| [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | Chiude l'handle di notifica del dispositivo specificato.                                      |



 

Le funzioni seguenti vengono utilizzate con le unità CD-ROM e DVD.



| Funzione                                                               | Descrizione                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**CdromDisableDigitalPlayback**](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | Disabilita la riproduzione digitale per l'unità CD-ROM o DVD specificata.                                    |
| [**CdromEnableDigitalPlayback**](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | Abilita la riproduzione digitale per l'unità CD-ROM o DVD specificata.                                     |
| [**CdromIsDigitalPlaybackEnabled**](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | Determina se la riproduzione digitale è abilitata per l'unità CD-ROM o DVD specificata.               |
| [**CdromKnownGoodDigitalPlayback**](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | Determina se l'unità CD-ROM o DVD specificata ha una riproduzione digitale che è nota come corretta. |
| [**DvdLauncher**](dvdlauncher.md)                                     | Verifica che l'area multimediale nell'unità DVD corrisponda all'area dell'unità DVD.                       |



 

 

 
