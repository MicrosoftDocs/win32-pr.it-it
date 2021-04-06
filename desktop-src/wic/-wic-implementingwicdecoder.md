---
description: 'Altre informazioni su: implementazione di un decodificatore WIC-Enabled'
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Implementazione di un decodificatore WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebd6d56258bf18e6cc914a40efa4cd3a57a92fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883406"
---
# <a name="implementing-a-wic-enabled-decoder"></a>Implementazione di un decodificatore WIC-Enabled


L'implementazione di un decodificatore Windows Imaging Component (WIC) richiede la scrittura di due classi. Le interfacce di queste classi corrispondono direttamente alle responsabilità decodificatore descritte nella sezione [decodifica](-wic-howwicworks.md) del funzionamento [del componente Imaging di Windows](-wic-howwicworks.md).

Una delle classi fornisce servizi a livello di contenitore e implementa l'interfaccia [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) . Se il formato dell'immagine supporta i metadati a livello di contenitore, è necessario implementare anche l'interfaccia [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) in questa classe. È consigliabile supportare l'interfaccia [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) sul decodificatore e sul codificatore per supportare un'esperienza utente migliore.

L'altra classe che sarà implementata fornisce servizi a livello di frame ed esegue la decodifica effettiva dei bit dell'immagine per ogni frame nel contenitore. Questa classe implementa l'interfaccia [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) e l'interfaccia [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) . Se si scrive un decodificatore per un formato non elaborato, si implementa anche l'interfaccia [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) in questa classe. Oltre alle interfacce necessarie, si consiglia di implementare l'interfaccia [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) in questa classe per consentire le migliori prestazioni possibili per il formato di immagine.

Uno degli oggetti forniti da WIC è [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory). Spesso si usa l'interfaccia [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) su questo oggetto per creare diversi componenti. Poiché viene usata di frequente, è consigliabile conservarvi un riferimento come proprietà del membro sia per le classi del codificatore che del codificatore.


```C++
IWICImagingFactory* m_pImagingFactory = NULL;
IWICComponentFactory* m_pComponentFactory = NULL;
HRESULT hr;
      
hr = CoCreateInstance(CLSID_WICImagingFactory, NULL,
  CLSCTX_INPROC_SERVER, IID_IWICImagingFactory,
  (LPVOID*) m_pImagingFactory);

hr = m_pImagingFactory->QueryInterface(
  IID_IWICComponentFactory, (void**)&m_pComponentFactory);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Funzionamento del componente Windows Imaging](-wic-howwicworks.md)
</dt> <dt>

[Interfacce del decodificatore](-wic-decoderinterfaces.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Cenni preliminari sui metadati WIC](-wic-about-metadata.md)
</dt> <dt>

[Panoramica della codifica](-wic-creating-encoder.md)
</dt> </dl>

 

 



