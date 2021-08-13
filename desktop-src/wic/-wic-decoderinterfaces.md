---
description: Interfacce del decodificatore
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Interfacce del decodificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a52a0924f6302e45b10cb32a1d621db04967d33a3251ee39cce359e5030af5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119393526"
---
# <a name="decoder-interfaces"></a>Interfacce del decodificatore

Le tabelle seguenti illustrano le interfacce implementate dai Windows WiC (Imaging Component) e il diagramma classi mostra la gerarchia di ereditarietà.

Container-Level di decodificatore



| Interfaccia                                                                                       | Responsabilità                             | Implementazione                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)                                             | Servizi a livello di contenitore                     | Necessario                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | Notifica dello stato & supporto dell'annullamento | Consigliato                                                                |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)                                 | Enumerazione dei metadati                         | Facoltativo (obbligatorio solo per i formati che supportano i metadati a livello di contenitore) |



 

Frame-Level di decodificatore



| Interfaccia                                                           | Responsabilità          | Implementazione                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)         | Servizi a livello di frame      | Necessario                      |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)     | Enumerazione dei metadati      | Necessario                      |
| [IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md) | Trasformazioni del decodificatore nativo | Consigliato                   |
| [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)                       | Servizi di elaborazione non elaborati   | Obbligatorio solo per i formati non elaborati |



 

![Gerarchia di ereditarietà dell'interfaccia wic](graphics/wicinterfaces.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di un WIC-Enabled decodificatore](-wic-implementingwicdecoder.md)
</dt> <dt>

[Implementazione di IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



