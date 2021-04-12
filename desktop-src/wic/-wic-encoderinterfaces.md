---
description: Interfacce del codificatore
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Interfacce del codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232322"
---
# <a name="encoder-interfaces"></a>Interfacce del codificatore


Nelle tabelle seguenti sono illustrate le interfacce implementate dai codificatori Windows Imaging Component (WIC) e il diagramma classi Mostra la gerarchia di ereditarietà.

Interfacce del codificatore Container-Level



| Interfaccia                                                                                       | Responsabilità                             | Implementazione                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)                                             | Servizi a livello di contenitore                     | Necessario                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | Avviso di stato & supporto per l'annullamento | Consigliato                                                                |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)                                 | Servizi di serializzazione dei metadati              | Facoltativo (obbligatorio solo per i formati che supportano i metadati a livello di contenitore) |



 

Interfacce del codificatore Frame-Level



| Interfaccia                                                       | Responsabilità                | Implementazione |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)     | Servizi a livello di frame            | Necessario       |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md) | Servizi di serializzazione dei metadati | Necessario       |



 

![gerarchia di ereditarietà dell'interfaccia del codificatore WIC](graphics/wicencoderinterfaces.png)

Si noterà che le interfacce del codificatore sono immagini quasi speculari delle interfacce del decodificatore e che la maggior parte dei metodi su queste interfacce corrispondono ai metodi nelle interfacce del decodificatore correlate. Ora che si ha familiarità con l'implementazione di un decodificatore abilitato per WIC, l'implementazione di un codificatore abilitato per WIC può sembrare familiare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di un codificatore di WIC-Enabled](-wic-implementingwicencoder.md)
</dt> <dt>

[Implementazione di IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



