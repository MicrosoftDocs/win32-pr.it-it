---
title: Estensioni del dispositivo Windows Media Gestione dispositivi per il trasferimento dei metadati
description: Estensioni del dispositivo Windows Media Gestione dispositivi per il trasferimento dei metadati
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Windows Media Player, estensioni del dispositivo
- Windows Media Player, estensioni
- Media Player di Windows, metadati
- Windows Media Player, trasferimento di metadati accelerato
- Windows Media Player, trasferimento accelerato dei metadati
- metadati, estensioni del dispositivo
- metadati, estensioni
- estensioni del dispositivo, trasferimento di metadati
- estensioni, trasferimento di metadati
- trasferimento di metadati accelerato
- metadati, trasferimento accelerato
- estensioni del dispositivo, trasferimento di metadati accelerato
- estensioni, trasferimento di metadati accelerato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d85ff7026e3395338fdf048c54b8ff7401c9ee7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471438"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a>Estensioni del dispositivo Windows Media Gestione dispositivi per il trasferimento dei metadati

Per consentire il trasferimento di metadati accelerati, i produttori di dispositivi che non supportano MTP devono eseguire le operazioni seguenti nel codice sorgente:

-   Definire **il \_ \_ \_ supporto del dispositivo WMDM di WMP**.
-   Includere wmpdevices. h, che viene installato come parte di Windows Media Player SDK.

Wmpdevices. h definisce le strutture seguenti.



| Struttura                                                                                 | Descrizione                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [WMP \_ WMDM \_ metadati \_ round \_ Trip \_ PC2DEVICE](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | Struttura utilizzata da Windows Media Player per richiedere informazioni di sincronizzazione dei metadati accelerate da dispositivi portatili che non supportano MTP. |
| [WMP \_ WMDM \_ metadati \_ round \_ Trip \_ DEVICE2PC](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | Struttura utilizzata da Windows Media Player per ricevere informazioni di sincronizzazione dei metadati accelerate dai dispositivi portatili che non supportano MTP. |



 

Per richiedere informazioni dal dispositivo sui metadati che sono stati modificati, Windows Media Player 10 o versione successiva chiama il metodo Windows Media Gestione dispositivi **IWMDMDevice3::D eviceiocontrol**. Quando si effettua questa chiamata, il giocatore segue passaggi specifici, come indicato di seguito:

-   Il primo parametro, *dwIoControlCode*, contiene la costante **\_ \_ \_ round \_ trip dei metadati IOCTL WMP**. Questa costante è definita in wmpdevices. h.
-   Il secondo parametro, *lpInBuffer*, punta a una struttura di **\_ \_ round trip dei metadati di WMP WMDM \_ \_ \_ PC2DEVICE** .
-   Il terzo parametro, *nInBufferSize*, contiene la dimensione del buffer di input.
-   Il quarto parametro, *lpOutBuffer*, punta a una struttura di **\_ \_ round trip dei metadati di WMP WMDM \_ \_ \_ DEVICE2PC** . Il dispositivo deve compilare questa struttura con le informazioni sulle modifiche.
-   Il quinto parametro, *pnOutBufferSize*, riceve la dimensione del buffer di output.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Estensioni del dispositivo per il trasferimento di metadati accelerati**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




