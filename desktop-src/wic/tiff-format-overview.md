---
description: Questo argomento fornisce informazioni sul codec TIFF nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Panoramica del formato TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28dfcc85dac21e95e6c76118d2db57cb74a08
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444422"
---
# <a name="tiff-format-overview"></a>Panoramica del formato TIFF

Questo argomento fornisce informazioni sul codec TIFF nativo disponibile tramite Windows Imaging Component (WIC).

-   [Codec Identity](#codec-identity)
-   [Encoding](#encoding)
    -   [Opzioni del codificatore](#encoder-options)
-   [Decodifica](#decoding)

## <a name="codec-identity"></a>Codec Identity

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



|   Componente            |   Descrizione                   |
|------------------------|---------------------------------|
| Nomi formali         | Tagged Image File Format (TIFF) |
| Estensioni di file | tiff, tif                       |
| Tipi MIME           | image/tiff, image/tif           |
| Supporto delle specifiche  | Specifica TIFF 6.0          |



 

Nella tabella seguente sono elencati i GUID utilizzati per identificare i componenti nativi del codec TIFF.



| Componente        | Nome descrittivo             | GUID                                 |
|------------------|---------------------------|--------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatTiff | 163bcc30-e2e9-4f0b-961da3e9fdb788a3  |
| Decodificatore          | CLSID \_ WICTiffDecoder     | b54e85d9-fe23-499f-8b886acea7137502b |
| Codificatore          | CLSID \_ WICTiffEncoder     | 0131be10-2001-4c5f-a9b0cc88fab64ce8  |



 

## <a name="encoding"></a>Codifica

L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla codifica delle immagini tramite l'API WIC, vedere Cenni preliminari [sulla codifica.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Opzioni del codificatore

I codec abilitati per WIC differiscono a livello di opzione di codifica. Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore. Le opzioni del codificatore possono essere opzioni di base supportate da WIC disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportate) o opzioni specifiche del codec progettate dal codec di formato immagine. Per gestire queste opzioni di codifica durante il processo di codifica, WIC usa [**l'interfaccia IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Per altre informazioni sull'uso **dell'interfaccia IPropertyBag2** per la codifica WIC, vedere Cenni [preliminari sulla codifica.](-wic-creating-encoder.md)

Il codec TIFF usa le opzioni WIC di base. La tabella seguente elenca le opzioni del codificatore WIC supportate dal codec TIFF nativo.

| Nome della proprietà         | VARTYPE | Gamma valori | Valore predefinito    |
|-----------------------|---------|-------------|------------------|
| CompressionQuality    | VT \_ R4  | 0 - 1.0     | 0                |
| TiffCompressionMethod | VT \_ UI1 | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

Se un'opzione del codificatore è presente [**nell'elenco di opzioni IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) non supportato dal codec, viene ignorata.

### <a name="compressionquality-option"></a>Opzione CompressionQuality

Specifica la qualità di compressione desiderata. 0,0 indica lo schema di compressione meno efficiente disponibile. In genere, questo schema comporta una codifica più veloce ma un output più grande. Il valore 1.0 specifica lo schema di compressione più efficiente disponibile. In genere, questo schema comporta una codifica più lunga, ma produce un output più piccolo.

Il valore predefinito è 0.

### <a name="tiffcompressionmethod-option"></a>Opzione TiffCompressionMethod

Specifica il metodo di compressione TIFF.

Il valore predefinito è [**WICTiffCompressionDontCare.**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)

## <a name="decoding"></a>Decodifica

Le API di decodifica WIC sono progettate per essere indipendenti dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md) Per altre informazioni sull'uso di dati di immagine decodificati, vedere Cenni [preliminari sulle origini bitmap.](-wic-bitmapsources.md)

 

 
