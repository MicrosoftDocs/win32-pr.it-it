---
description: 'Completezza delle funzionalità: interfacce consigliate'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Completezza delle funzionalità: interfacce consigliate'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c819f56b9343eab8326eb755d86280bde242a01
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473827"
---
# <a name="feature-completeness-recommended-interfaces"></a>Completezza delle funzionalità: interfacce consigliate

Nella tabella seguente sono elencate le Windows che i codec RAW del componente di creazione dell'immagine (WIC) devono implementare.




| Interfaccia | Necessario per | Descrizione | 
|-----------|--------------|-------------|
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a> | Decoder | Rappresenta il punto iniziale per la decodifica di un file di immagine. Fornisce l'accesso alle proprietà a livello di contenitore, ad esempio anteprime, fotogrammi e tavolozza.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a> | Decoder | Rappresenta una cornice di immagine specifica all'interno del contenitore che fornisce l'accesso alle proprietà a livello di frame. Si tratta dell'interfaccia che decodifica i bit effettivi dell'immagine.<br /> | 
| <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> | Decoder | Obbligatorio per l'enumerazione e l'scorrere i blocchi di metadati e richiamare i lettori di metadati appropriati durante la lettura da un file di immagine. <br /><blockquote>[!Note]<br />Se il formato del contenitore RAW è compatibile con TIFF o usa IFD o IRB standard per archiviare metadati EXIF o XMP, gli autori di codec possono scegliere di richiamare i lettori di metadati predefiniti anziché scriverne di propri.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a> | Decoder | Consente al chiamante di specificare il ridimensionamento, il ritaglio, la rotazione o il formato pixel desiderato per l'immagine decodificata, migliorando in modo significativo le prestazioni del decodificatore. Ad esempio, i decodificatori JPEG e WDP (Wireless Datagram Protocol) di Microsoft usano uno schema di ottimizzazione a piramide per ottenere una decodifica più veloce quando la bitmap di destinazione è più piccola della bitmap di origine. Windows Vista (e versioni successive) tenterà di usare questa interfaccia per estrarre un'anteprima "veloce" da un'immagine RAW ogni volta che l'anteprima incorporata è mancante o inferiore a 1.024 pixel nella dimensione più grande.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a> | Decoder | Obbligatorio per i formati RAW. Espone parametri specifici dell'elaborazione di immagini RAW. I codec RAW devono supportare tutti questi parametri applicabili al codec.<br /> | 
| <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a> | Codificatori | Rappresenta il punto iniziale per la codifica di un file di immagine. Questa interfaccia viene usata per impostare proprietà a livello di contenitore, ad esempio anteprime, fotogrammi e tavolozza. È anche necessario richiamare un writer di metadati per abilitare la persistenza dei metadati nel file di immagine. Per questi motivi, questa interfaccia è necessaria anche se la codifica della bitmap primaria nel formato RAW non è supportata.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a> | Codificatori | Rappresenta una cornice di immagine specifica all'interno del contenitore. Questa interfaccia viene usata per codificare i bit di immagine effettivi e per impostare proprietà e metadati per frame.<br /> | 
| <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> | Codificatori | Obbligatorio per scorrere i blocchi di metadati e richiamare i writer di metadati appropriati durante la serializzazione di un file di immagine.<br /><blockquote>[!Note]<br />Se il formato del contenitore RAW è compatibile con TIFF, gli autori di codec possono scegliere di richiamare i writer di metadati predefiniti anziché scriverne di propri.</blockquote><br /><br /> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




