---
title: Informazioni sulle relazioni
description: Informazioni sulle relazioni
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player, relazioni
- Modello a oggetti di Windows Media Player, relazioni
- modello a oggetti, relazioni
- Controllo ActiveX Windows Media Player, relazioni
- Controllo ActiveX, relazioni
- Controllo ActiveX Windows Media Player Mobile, relazioni
- Windows Media Player Mobile, relazioni
- sincronizzazione di dispositivi, relazioni
- sincronizzazione dei dispositivi, relazioni
- partenariati tra dispositivi e Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfc3fa20e1e8a4b6a4c7993ea7dcc5842719f2a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104472243"
---
# <a name="about-partnerships"></a>Informazioni sulle relazioni

Una partnership è una relazione speciale tra un dispositivo portatile e Windows Media Player. Gli utenti possono stabilire una relazione per un particolare dispositivo usando l'interfaccia utente di Windows Media Player. È possibile gestire le relazioni a livello di codice usando [IWMPSyncDevice:: createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) e [IWMPSyncDevice::d eletepartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership). Il metodo **createPartnership** avvia un processo asincrono che termina quando viene ricevuto l'evento **CreatePartnershipComplete** tramite l'interfaccia **IWMPEvents2** .

Windows Media Player 10 o versioni successive supporta la creazione di relazioni con un massimo di 16 dispositivi. A ogni relazione è associato un indice di relazione. È possibile recuperare l'indice di relazione per un determinato dispositivo chiamando [IWMPSyncDevice:: Get \_ partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex). Gli indici di partnership sono numerati da 1 a 16. Quando un particolare dispositivo non dispone di una relazione con Windows Media Player, **getPartnershipIndex** restituisce zero per l'indice.

È possibile recuperare lo stato della partnership di un determinato dispositivo chiamando [IWMPSyncDevice:: Get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) ed esaminando il valore [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperato. Windows Media Player consente la collaborazione con una libreria di un utente in un computer per ogni dispositivo. Ciò significa che la creazione di una nuova partnership elimina qualsiasi relazione esistente che il dispositivo corrente potrebbe avere con un altro computer. Per capire quando lo stato cambia per un dispositivo, è possibile ricevere l'evento **DeviceStatusChange** .

Windows Media Player non è in grado di creare una relazione con un dispositivo con lo stato **wmpdsManualDevice**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulla sincronizzazione dei dispositivi**](about-device-synchronization.md)
</dt> <dt>

[**Interfaccia IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Uso dei dispositivi portatili**](working-with-portable-devices.md)
</dt> </dl>

 

 




