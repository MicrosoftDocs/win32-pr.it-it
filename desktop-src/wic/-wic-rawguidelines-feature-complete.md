---
description: 'Completezza delle funzionalità: interfacce consigliate'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Completezza delle funzionalità: interfacce consigliate'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1dba4bcc029b2205985afb443526376c0eecb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315953"
---
# <a name="feature-completeness-recommended-interfaces"></a>Completezza delle funzionalità: interfacce consigliate

Nella tabella seguente sono elencati i codec non ELABORAti delle interfacce di Windows Imaging Component (WIC) che devono essere implementati.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Interfaccia</th>
<th>Necessario per</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></td>
<td>Decodificatori</td>
<td>Rappresenta il punto di partenza per la decodifica di un file di immagine. Fornisce l'accesso alle proprietà a livello di contenitore come anteprime, frame e tavolozza.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></td>
<td>Decodificatori</td>
<td>Rappresenta un frame di immagine specifico all'interno del contenitore che fornisce l'accesso alle proprietà a livello di frame. Si tratta dell'interfaccia che decodifica i bit dell'immagine effettivi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></td>
<td>Decodificatori</td>
<td>Obbligatorio per l'enumerazione e l'iterazione nei blocchi di metadati e per richiamare i reader di metadati appropriati durante la lettura da un file di immagine. <br/>
<blockquote>
[!Note]<br />
Se il formato del contenitore non elaborato è compatibile con TIFF oppure utilizza IFDs o IRBs standard per archiviare i metadati EXIF o XMP, gli autori di codec possono scegliere di richiamare i lettori di metadati predefiniti anziché scriverne di propri.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></td>
<td>Decodificatori</td>
<td>Consente al chiamante di specificare il formato di ridimensionamento, ritaglio, rotazione o pixel desiderato per l'immagine decodificata, che può migliorare significativamente le prestazioni del decodificatore. Ad esempio, i decodificatori JPEG e wireless datagramma (WDP) di Microsoft utilizzano uno schema di ottimizzazione a piramide per ottenere una decodifica più veloce quando la bitmap di destinazione è inferiore alla bitmap di origine. Windows Vista (e versioni successive) tenterà di utilizzare questa interfaccia per estrarre un' &quot; &quot; Anteprima veloce da un'immagine non elaborata ogni volta che l'anteprima incorporata è mancante o inferiore a 1.024 pixel nella dimensione massima.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></td>
<td>Decodificatori</td>
<td>Obbligatorio per i formati non ELABORAti. Espone parametri specifici dell'elaborazione di immagini non ELABORAte. I codec RAW dovrebbero supportare tutti questi parametri applicabili al codec.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></td>
<td>Codificatori</td>
<td>Rappresenta il punto di partenza per la codifica di un file di immagine. Questa interfaccia viene utilizzata per impostare le proprietà a livello di contenitore, ad esempio le anteprime, i frame e la tavolozza. È inoltre necessario richiamare un writer di metadati per abilitare la persistenza dei metadati nel file di immagine. Per questi motivi, questa interfaccia è necessaria anche se la codifica della bitmap primaria nel formato non elaborato non è supportata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></td>
<td>Codificatori</td>
<td>Rappresenta un frame di immagine specifico all'interno del contenitore. Questa interfaccia viene usata per codificare i bit dell'immagine effettivi e per impostare i metadati e le proprietà per fotogramma.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></td>
<td>Codificatori</td>
<td>Obbligatorio per scorrere i blocchi di metadati e richiamare i writer di metadati appropriati durante la serializzazione di un file di immagine.<br/>
<blockquote>
[!Note]<br />
Se il formato del contenitore non elaborato è compatibile con TIFF, gli autori di codec possono scegliere di richiamare i writer di metadati predefiniti anziché scriverne di propri.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida per WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




