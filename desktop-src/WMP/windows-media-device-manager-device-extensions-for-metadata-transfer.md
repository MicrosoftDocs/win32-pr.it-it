---
title: Windows Estensioni del dispositivo di Gestione dispositivi multimediali per il trasferimento dei metadati
description: Windows Estensioni del dispositivo di Gestione dispositivi multimediali per il trasferimento dei metadati
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Windows Media Player,estensioni del dispositivo
- Windows Media Player,estensioni
- Windows Media Player, metadati
- Windows Media Player,trasferimento accelerato dei metadati
- Windows Media Player, trasferimento accelerato dei metadati
- metadati, estensioni del dispositivo
- metadati, estensioni
- estensioni del dispositivo, trasferimento di metadati
- estensioni, trasferimento di metadati
- trasferimento accelerato di metadati
- metadati, trasferimento accelerato
- estensioni del dispositivo, trasferimento accelerato dei metadati
- estensioni, trasferimento accelerato dei metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9b37271fc9714bf3665dccf1475da1a5840c429d7df9136a50fe95789f7a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571637"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a>Windows Estensioni del dispositivo di Gestione dispositivi multimediali per il trasferimento dei metadati

Per abilitare il trasferimento accelerato dei metadati, i produttori di dispositivi che non supportano MTP devono eseguire le operazioni seguenti nel codice sorgente:

-   Definire **IL SUPPORTO DEI DISPOSITIVI \_ WMDM \_ \_ WMP.**
-   Includere wmpdevices.h, installato come parte di Windows Media Player SDK.

Wmpdevices.h definisce le strutture seguenti.



| Struttura                                                                                 | Descrizione                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [ROUND \_ TRIP DEI METADATI WMDM WMP \_ \_ \_ \_ PC2DEVICE](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | Struttura utilizzata dal Windows Media Player richiedere informazioni di sincronizzazione dei metadati accelerati da dispositivi portatili che non supportano MTP. |
| [WMP \_ WMDM \_ METADATA \_ ROUND \_ TRIP \_ DEVICE2PC](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | Struttura utilizzata dal Windows Media Player ricevere informazioni di sincronizzazione dei metadati accelerata da dispositivi portatili che non supportano MTP. |



 

Per richiedere al dispositivo informazioni sui metadati modificati, Windows Media Player 10 o versioni successive chiama il metodo di Gestione dispositivi multimediali di Windows **IWMDMDevice3::D eviceIoControl**. Quando si effettua questa chiamata, il lettore segue passaggi specifici, come indicato di seguito:

-   Il primo parametro, *dwIoControlCode*, contiene la costante **IOCTL \_ WMP \_ METADATA ROUND \_ \_ TRIP**. Questa costante è definita in wmpdevices.h.
-   Il secondo parametro, *lpInBuffer,* punta a una **struttura \_ WMP WMDM \_ METADATA ROUND TRIP \_ \_ \_ PC2DEVICE.**
-   Il terzo parametro, *nInBufferSize*, contiene le dimensioni del buffer di input.
-   Il quarto parametro, *lpOutBuffer*, punta a una **struttura \_ WMP WMDM \_ METADATA ROUND TRIP \_ \_ \_ DEVICE2PC.** Il dispositivo deve compilare questa struttura con informazioni sulle modifiche.
-   Il quinto parametro, *pnOutBufferSize,* riceve le dimensioni del buffer di output.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Estensioni del dispositivo per il trasferimento accelerato dei metadati**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




