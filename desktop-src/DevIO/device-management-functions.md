---
description: Nella gestione dei dispositivi vengono usate le funzioni seguenti.
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: Funzioni di gestione dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a648fb5141d9efa977e573e3b0abb32fe6c504f11647a2dc392e9838da63ca6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956900"
---
# <a name="device-management-functions"></a>Funzioni di gestione dei dispositivi

Nella gestione dei dispositivi vengono usate le funzioni seguenti.



| Funzione                                                             | Descrizione                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**Deviceiocontrol**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | Invia un codice di controllo direttamente a un driver di dispositivo specificato.                           |
| [**InstallNewDevice**](installnewdevice.md)                         | Installa un nuovo dispositivo. All'utente viene richiesto di selezionare il dispositivo.                     |
| [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | Registra il dispositivo o il tipo di dispositivo per cui una finestra riceverà notifiche. |
| [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | Chiude l'handle di notifica del dispositivo specificato.                                      |



 

Le funzioni seguenti vengono usate con unità CD-ROM e DVD.



| Funzione                                                               | Descrizione                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**CdromDisableDigitalPlayback**](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | Disabilita la riproduzione digitale per l'unità CD-ROM o DVD specificata.                                    |
| [**CdromEnableDigitalPlayback**](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | Abilita la riproduzione digitale per l'unità CD-ROM o DVD specificata.                                     |
| [**CdromIsDigitalPlaybackEnabled**](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | Determina se la riproduzione digitale è abilitata per l'unità CD-ROM o DVD specificata.               |
| [**CdromKnownGoodDigitalPlayback**](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | Determina se l'unità CD-ROM o DVD specificata ha una riproduzione digitale nota come buona. |
| [**DvdLauncher**](dvdlauncher.md)                                     | Verifica che l'area del supporto nell'unità DVD corrisponda all'area dell'unità DVD.                       |



 

 

 
