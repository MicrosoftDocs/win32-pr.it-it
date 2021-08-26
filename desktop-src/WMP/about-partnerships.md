---
title: Informazioni sulle partnership
description: Informazioni sulle partnership
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player, partnership
- Windows Media Player a oggetti, partnership
- modello a oggetti, partnership
- Windows Media Player ActiveX, partnership
- ActiveX, partnership
- Windows Media Player controllo ActiveX dispositivi mobili, partnership
- Windows Media Player Dispositivi mobili, partnership
- sincronizzazione di dispositivi, partnership
- sincronizzazione dei dispositivi, partnership
- partnership tra dispositivi e Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c018934ed06e5872d5866a463bdd909ea2501a1872ded29231be222572b2ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004491"
---
# <a name="about-partnerships"></a>Informazioni sulle partnership

Una relazione è una relazione speciale tra un dispositivo portatile e Windows Media Player. Gli utenti possono stabilire una relazione per un particolare dispositivo usando l'Windows Media Player utente. È possibile gestire le partnership a livello di codice usando [IWMPSyncDevice::createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) e [IWMPSyncDevice::d eletePartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership). Il **metodo createPartnership** avvia un processo asincrono che termina quando l'evento **CreatePartnershipComplete** viene ricevuto tramite l'interfaccia **IWMPEvents2.**

Windows Media Player 10 o versioni successive supporta la creazione di partnership con un massimo di 16 dispositivi. A ogni relazione è associato un indice di partnership. È possibile recuperare l'indice della relazione per un particolare dispositivo chiamando [IWMPSyncDevice::get \_ partnershipIndex.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex) Gli indici di partnership sono numerati da 1 a 16. Quando un particolare dispositivo non ha una relazione con Windows Media Player, **getPartnershipIndex** restituisce zero per l'indice.

È possibile recuperare lo stato di relazione di un particolare dispositivo chiamando lo stato [IWMPSyncDevice::get \_ ](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) e quindi controllando il [valore WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperato. Windows Media Player consente una relazione con la libreria di un utente in un computer per ogni dispositivo. Ciò significa che la creazione di una nuova relazione elimina qualsiasi relazione esistente che il dispositivo corrente potrebbe avere con un altro computer. Per sapere quando lo stato cambia per un dispositivo, è possibile ricevere **l'evento DeviceStatusChange.**

Windows Media Player possibile creare una relazione con un dispositivo con stato **wmpdsManualDevice**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulla sincronizzazione dei dispositivi**](about-device-synchronization.md)
</dt> <dt>

[**Interfaccia IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Uso di dispositivi portatili**](working-with-portable-devices.md)
</dt> </dl>

 

 




