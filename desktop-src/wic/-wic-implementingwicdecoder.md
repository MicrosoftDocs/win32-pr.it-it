---
description: 'Altre informazioni: Implementazione di un WIC-Enabled decodificatore'
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Implementazione di un WIC-Enabled decodificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0aa2211c0b21e8f6fc921986406f7079b13c216f0bd7ada684e7748effb6c7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205707"
---
# <a name="implementing-a-wic-enabled-decoder"></a>Implementazione di un WIC-Enabled decodificatore


L'implementazione Windows decodificatore WIC (Windows Imaging Component) richiede la scrittura di due classi. Le interfacce in queste classi corrispondono direttamente alle responsabilità [](-wic-howwicworks.md) del decodificatore descritte nella sezione Decodifica di [How the Windows Imaging Component Works](-wic-howwicworks.md).

Una delle classi fornisce servizi a livello di contenitore e implementa [l'interfaccia IWICBitmapDecoder.](-wic-imp-iwicbitmapdecoder.md) Se il formato dell'immagine supporta i metadati a livello di contenitore, è necessario implementare anche [l'interfaccia IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) in questa classe. È consigliabile supportare [l'interfaccia IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) sia nel decodificatore che nel codificatore per supportare un'esperienza utente migliore.

L'altra classe che verrà implementata fornisce servizi a livello di frame ed esegue la decodifica effettiva dei bit di immagine per ogni frame nel contenitore. Questa classe implementa [l'interfaccia IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) e [l'interfaccia IWICMetadataBlockReader.](-wic-imp-iwicmetadatablockreader.md) Se si scrive un decodificatore per un formato non elaborato, si implementa anche [l'interfaccia IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) in questa classe. Oltre alle interfacce necessarie, è consigliabile implementare [l'interfaccia IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) in questa classe per abilitare le migliori prestazioni possibili per il formato di immagine.

Uno degli oggetti forniti da WIC è [**ImagingFactory.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) L'interfaccia [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) viene spesso utilizzata in questo oggetto per creare vari componenti. Poiché viene usato di frequente, è consigliabile mantenere un riferimento a esso come proprietà membro nelle classi del decodificatore e del codificatore.


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

[Funzionamento del Windows imaging](-wic-howwicworks.md)
</dt> <dt>

[Interfacce del decodificatore](-wic-decoderinterfaces.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Panoramica dei metadati WIC](-wic-about-metadata.md)
</dt> <dt>

[Cenni preliminari sulla codifica](-wic-creating-encoder.md)
</dt> </dl>

 

 



