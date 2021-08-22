---
description: Interfacce del codificatore
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Interfacce del codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6169dcf55ffafe0bf4c006b45c173ecc7486555fb001456112f8f333a8ccf2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965125"
---
# <a name="encoder-interfaces"></a>Interfacce del codificatore


Le tabelle seguenti illustrano le interfacce implementate dai codificatori WIC (Windows Imaging Component) e il diagramma classi mostra la gerarchia di ereditarietà.

Container-Level codificatore



| Interfaccia                                                                                       | Responsabilità                             | Implementazione                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)                                             | Servizi a livello di contenitore                     | Necessario                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | Notifica dello stato di avanzamento & supporto dell'annullamento | Consigliato                                                                |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)                                 | Servizi di serializzazione dei metadati              | Facoltativo (obbligatorio solo per i formati che supportano i metadati a livello di contenitore) |



 

Frame-Level codificatore



| Interfaccia                                                       | Responsabilità                | Implementazione |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)     | Servizi a livello di frame            | Necessario       |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md) | Servizi di serializzazione dei metadati | Necessario       |



 

![Gerarchia di ereditarietà dell'interfaccia del codificatore Wic](graphics/wicencoderinterfaces.png)

Si noterà che le interfacce del codificatore sono quasi immagini speculari delle interfacce del decodificatore e che la maggior parte dei metodi in queste interfacce corrispondono ai metodi sulle interfacce del decodificatore correlate. Ora che si ha familiarità con l'implementazione di un decodificatore abilitato per WIC, anche l'implementazione di un codificatore abilitato per WIC sembra familiare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di un WIC-Enabled codificatore](-wic-implementingwicencoder.md)
</dt> <dt>

[Implementazione di IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



