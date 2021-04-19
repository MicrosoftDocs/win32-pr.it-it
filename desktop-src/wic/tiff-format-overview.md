---
description: In questo argomento vengono fornite informazioni sul codec TIFF nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Cenni preliminari sul formato TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db603857da892d4b699bb7df7d8b3e2ee5566326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317243"
---
# <a name="tiff-format-overview"></a>Cenni preliminari sul formato TIFF

In questo argomento vengono fornite informazioni sul codec TIFF nativo disponibile tramite Windows Imaging Component (WIC).

-   [Identità codec](#codec-identity)
-   [Encoding](#encoding)
    -   [Opzioni del codificatore](#encoder-options)
-   [Decodifica](#decoding)

## <a name="codec-identity"></a>Identità codec

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



|                        |                                 |
|------------------------|---------------------------------|
| Nome/i formale/i         | Tagged Image File Format (TIFF) |
| Estensioni del nome di file | TIFF, TIF                       |
| Tipi MIME           | image/TIFF, image/TIF           |
| Supporto delle specifiche  | Specifica TIFF 6,0          |



 

Nella tabella seguente sono elencati i GUID utilizzati per identificare i componenti codec TIFF nativi.



| Componente        | Nome descrittivo             | GUID                                 |
|------------------|---------------------------|--------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatTiff | 163bcc30-e2e9-4f0b-961da3e9fdb788a3  |
| Decodificatore          | \_WICTIFFDECODER CLSID     | b54e85d9-FE23-499f-8b886acea7137502b |
| Codificatore          | \_WICTIFFENCODER CLSID     | 0131be10-2001-4c5f-a9b0cc88fab64ce8  |



 

## <a name="encoding"></a>Codifica

L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla codifica delle immagini tramite l'API WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opzioni del codificatore

I codec abilitati per WIC differiscono a livello di opzione di codifica. Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore. Le opzioni del codificatore possono essere opzioni supportate per WIC di base disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportati) o per le opzioni specifiche del codec progettate dal codec del formato di immagine. Per gestire queste opzioni di codifica durante il processo di codifica, WIC utilizza l'interfaccia [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Per ulteriori informazioni sull'utilizzo dell'interfaccia **IPropertyBag2** per la codifica WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).

Il codec TIFF usa le opzioni WIC di base. Nella tabella seguente sono elencate le opzioni del codificatore WIC supportate dal codec TIFF nativo.

| Nome della proprietà         | VARTYPE | Gamma valori | Valore predefinito    |
|-----------------------|---------|-------------|------------------|
| CompressionQuality    | \_R4 VT  | 0-1,0     | 0                |
| TiffCompressionMethod | \_Ui1 VT | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

Se un'opzione del codificatore è presente nell'elenco di opzioni [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) che il codec non supporta, viene ignorato.

### <a name="compressionquality-option"></a>CompressionQuality-opzione

Specifica la qualità di compressione desiderata. 0,0 indica lo schema di compressione meno efficiente disponibile. In genere, questo schema genera una codifica più veloce ma un output più grande. Il valore 1,0 specifica lo schema di compressione più efficiente disponibile. In genere, questo schema comporta una codifica più lunga, ma produce un output di dimensioni inferiori.

Il valore predefinito è 0.

### <a name="tiffcompressionmethod-option"></a>TiffCompressionMethod-opzione

Specifica il metodo di compressione TIFF.

Il valore predefinito è [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).

## <a name="decoding"></a>Decodifica

Le API di decodifica WIC sono progettate per essere indipendenti dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md). Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).

 

 
