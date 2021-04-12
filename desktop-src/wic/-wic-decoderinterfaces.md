---
description: Interfacce del decodificatore
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Interfacce del decodificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef90ca2dd521c15460295505a6d5b7ea451c4dba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233541"
---
# <a name="decoder-interfaces"></a>Interfacce del decodificatore

Nelle tabelle seguenti sono illustrate le interfacce implementate dai decodificatori di Windows Imaging Component (WIC) e il diagramma classi Mostra la gerarchia di ereditarietà.

Interfacce del decodificatore Container-Level



| Interfaccia                                                                                       | Responsabilità                             | Implementazione                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)                                             | Servizi a livello di contenitore                     | Necessario                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | Avviso di stato & supporto per l'annullamento | Consigliato                                                                |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)                                 | Enumerazione dei metadati                         | Facoltativo (obbligatorio solo per i formati che supportano i metadati a livello di contenitore) |



 

Interfacce del decodificatore Frame-Level



| Interfaccia                                                           | Responsabilità          | Implementazione                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)         | Servizi a livello di frame      | Necessario                      |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)     | Enumerazione dei metadati      | Necessario                      |
| [IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md) | Trasformazioni del decodificatore Native | Consigliato                   |
| [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)                       | Servizi di elaborazione non elaborati   | Obbligatorio solo per formati RAW |



 

![gerarchia di ereditarietà dell'interfaccia WIC](graphics/wicinterfaces.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di un decodificatore WIC-Enabled](-wic-implementingwicdecoder.md)
</dt> <dt>

[Implementazione di IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



