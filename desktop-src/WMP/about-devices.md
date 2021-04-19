---
title: Informazioni sui dispositivi
description: Informazioni sui dispositivi
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Windows Media Player, sincronizzazione dei dispositivi
- Modello a oggetti di Windows Media Player, sincronizzazione dei dispositivi
- modello a oggetti, sincronizzazione dei dispositivi
- Controllo ActiveX di Windows Media Player, sincronizzazione dei dispositivi
- Controllo ActiveX, sincronizzazione dei dispositivi
- Controllo ActiveX Windows Media Player Mobile, sincronizzazione dei dispositivi
- Windows Media Player Mobile, sincronizzazione dei dispositivi
- sincronizzazione dei dispositivi, informazioni
- sincronizzazione dei dispositivi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89a074e4edb5bdbc7d90391398d5e0e4133505a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299375"
---
# <a name="about-devices"></a>Informazioni sui dispositivi

I dispositivi portatili sono dispositivi hardware che gli utenti portano a utilizzare contenuti multimediali digitali quando sono lontani dal computer. In genere, i dispositivi portatili vengono usati a batteria. Alcuni dispositivi possono riprodurre solo musica. Altri dispositivi possono riprodurre video e musica.

Alcuni dispositivi supportano la sincronizzazione automatica del contenuto multimediale digitale con Windows Media Player. Altri dispositivi supportano solo il trasferimento manuale. È possibile determinare se un determinato dispositivo supporta la sincronizzazione automatica chiamando [IWMPSyncDevice:: Get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) e quindi controllando il valore [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperato. Se il valore recuperato è **wmpdsManualDevice**, il dispositivo non supporta la sincronizzazione automatica.

È possibile enumerare i dispositivi connessi al computer dell'utente. A tale scopo, usare prima [IWMPSyncServices:: Get \_ deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) per recuperare il conteggio dei dispositivi. Quindi, in un ciclo, chiamare [IWMPSyncServices:: GetDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), passando ogni volta il valore di indice appropriato. È possibile usare [IWMPSyncDevice:: Get \_ Connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) per valutare se un determinato dispositivo è attualmente connesso.

Per informazioni su quando i dispositivi si connettono o si disconnettono, è possibile ricevere gli eventi **DeviceConnect** e **DeviceDisconnect** . Questi eventi vengono ricevuti tramite l'interfaccia **IWMPEvents2** .

L'interfaccia **IWMPSyncDevice** fornisce metodi aggiuntivi che consentono di ottenere o impostare informazioni su un dispositivo. Ad esempio:

-   I metodi **get \_ FriendlyName** e **put \_ FriendlyName** consentono di recuperare e specificare il nome del dispositivo definito dall'utente.
-   Il metodo **get \_ DeviceName** consente di recuperare il nome del dispositivo visualizzato dagli utenti nella shell di Windows XP.
-   Il metodo **GetItemInfo** consente di recuperare i metadati dai dispositivi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulla sincronizzazione dei dispositivi**](about-device-synchronization.md)
</dt> <dt>

[**Interfaccia IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Interfaccia IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**Uso dei dispositivi portatili**](working-with-portable-devices.md)
</dt> </dl>

 

 




