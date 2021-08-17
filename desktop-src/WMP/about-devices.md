---
title: Informazioni sui dispositivi
description: Informazioni sui dispositivi
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Windows Media Player, sincronizzazione dei dispositivi
- Windows Media Player a oggetti, sincronizzazione dei dispositivi
- modello a oggetti, sincronizzazione dei dispositivi
- Windows Media Player ActiveX, sincronizzazione dei dispositivi
- ActiveX, sincronizzazione dei dispositivi
- Windows Media Player controllo ActiveX dispositivi mobili, sincronizzazione dei dispositivi
- Windows Media Player dispositivi mobili, sincronizzazione dei dispositivi
- sincronizzazione di dispositivi, informazioni
- sincronizzazione dei dispositivi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66383082bae772b48f913f6bd4615724de8f7b7735e387ba93407a9848f17074
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956921"
---
# <a name="about-devices"></a>Informazioni sui dispositivi

I dispositivi portatili sono dispositivi hardware che gli utenti trasportano per usufruire del contenuto multimediale digitale quando sono fuori dal computer. In genere, i dispositivi portatili sono a batteria. Alcuni dispositivi possono riprodurre solo musica. Altri dispositivi possono riprodurre video e musica.

Alcuni dispositivi supportano la sincronizzazione automatica del contenuto multimediale digitale con Windows Media Player. Altri dispositivi supportano solo il trasferimento manuale. È possibile determinare se un determinato dispositivo supporta la sincronizzazione automatica chiamando lo stato [IWMPSyncDevice::get \_ ](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) e quindi controllando il [valore WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperato. Se il valore recuperato è **wmpdsManualDevice**, il dispositivo non supporta la sincronizzazione automatica.

È possibile enumerare i dispositivi connessi al computer dell'utente. A tale scopo, usare prima [di tutto IWMPSyncServices::get \_ deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) per recuperare il conteggio dei dispositivi. In un ciclo chiamare quindi [IWMPSyncServices::getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), passando ogni volta il valore di indice appropriato. È possibile usare [IWMPSyncDevice::get \_ connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) per valutare se un determinato dispositivo è attualmente connesso.

Per sapere quando i dispositivi si connettono o si disconnettino, è possibile ricevere gli eventi **DeviceConnect** **e DeviceDisconnect.** Questi eventi vengono ricevuti tramite **l'interfaccia IWMPEvents2.**

**L'interfaccia IWMPSyncDevice** fornisce metodi aggiuntivi che consentono di ottenere o impostare informazioni su un dispositivo. Esempio:

-   I **metodi get \_ FriendlyName** **e put \_ FriendlyName** consentono di recuperare e specificare il nome del dispositivo definito dall'utente.
-   Il **metodo \_ get deviceName** consente di recuperare il nome del dispositivo visualizzato dagli utenti nella shell Windows XP.
-   Il **metodo getItemInfo** consente di recuperare i metadati dai dispositivi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulla sincronizzazione dei dispositivi**](about-device-synchronization.md)
</dt> <dt>

[**Interfaccia IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Interfaccia IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**Uso di dispositivi portatili**](working-with-portable-devices.md)
</dt> </dl>

 

 




