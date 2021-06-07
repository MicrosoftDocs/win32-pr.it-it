---
description: In questo argomento vengono fornite informazioni sul codec JPEG nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Panoramica del formato JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2acc7fcd71fc962d3321112d342f675b878188
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444192"
---
# <a name="jpeg-format-overview"></a>Panoramica del formato JPEG

In questo argomento vengono fornite informazioni sul codec JPEG nativo disponibile tramite Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Codec Identity

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



|   Componente            | Descrizione                             |
|------------------------|-----------------------------------------|
| Nomi formali         | Joint Photographic Experts Group (JPEG) |
| Estensioni di file | jpe, jpeg, jpg                          |
| tipo MIME              | image/jpeg, image/jpe, image/jpg        |
| Supporto delle specifiche  | Specifica JFIF 1.02                 |



 

Nella tabella seguente sono elencati i GUID utilizzati per identificare i componenti nativi del codec JPEG.



| Componente        | Nome descrittivo             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatJpeg | 19e4a5aa-5662-4fc5-a0c01758028e1057 |
| Decodificatore          | CLSID \_ WICJpegDecoder     | 9456a480-e88b-43ea-9e730b2d9b71b1ca |
| Codificatore          | CLSID \_ WICJpegEncoder     | 1a34f5c1-4a5a-46dc-b6441f4567e7a676 |



 

## <a name="encoding"></a>Codifica

L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla codifica delle immagini tramite l'API WIC, vedere Cenni preliminari [sulla codifica.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Opzioni del codificatore

I codec abilitati per WIC differiscono a livello di opzione di codifica. Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore. Le opzioni del codificatore possono essere opzioni di base supportate da WIC disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportate) o opzioni specifiche del codec progettate dal codec di formato immagine. Per gestire queste opzioni di codifica durante il processo di codifica, WIC usa [**l'interfaccia IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Per altre informazioni sull'uso **dell'interfaccia IPropertyBag2** per la codifica WIC, vedere Cenni [preliminari sulla codifica.](-wic-creating-encoder.md)

Il codec JPEG usa le opzioni WIC di base. La tabella seguente elenca le opzioni del codificatore WIC supportate dal codec JPEG nativo.



| Nome della proprietà                                        | VARTYPE           | Gamma valori                                                                       | Valore predefinito                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ImageQuality](#imagequality-option)                 | VT \_ R4            | 0 - 1.0                                                                           | 0.9                                                                            |
| [BitmapTransform](#bitmaptransform-option)           | VT \_ UI1           | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [Luminanza](#luminance-option)                       | VT \_ UI4/VT \_ ARRAY | 64 voci (DCT)                                                                  | Tabella di luminance predefinita.                                                       |
| [Chrominance](#chrominance-option)                   | VT \_ UI4/VT \_ ARRAY | 64 voci (DCT)                                                                  | Tabella di cronologia predefinita.                                                     |
| [JpegYCrCbSubsampling](#jpegycrcbsubsampling-option) | VT \_ UI1           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [SuppressApp0](/windows)                       | VT \_ BOOL          | **TRUE** / **FALSE**                                                                | **FALSE**                                                                      |



 

Se un'opzione del codificatore è presente [**nell'elenco di opzioni IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) non supportato dal codec, viene ignorata.

### <a name="imagequality-option"></a>Opzione ImageQuality

Specifica la fedeltà dell'immagine desiderata. 0,0 indica la fedeltà più bassa possibile e 1.0 specifica la massima fedeltà.

Il valore predefinito è 0,9.

### <a name="bitmaptransform-option"></a>Opzione BitmapTransform

Specifica come l'immagine deve essere trasformata durante la decodifica dell'immagine. Questa opzione deve essere impostata su uno dei valori di [**enumerazione WICBitmapTransformOptions.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

Il valore predefinito è [**WICBitmapTransformRotate0.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

### <a name="luminance-option"></a>Opzione Luminance

Specifica la tabella del livello di luminosità in scala di grigi da utilizzare per la codifica.

### <a name="chrominance-option"></a>Opzione Chrominance

Specifica la tabella chrominance da usare per la codifica.

### <a name="jpegycrcbsubsampling-option"></a>Opzione JpegYCrCbSubsampling

Specifica il rapporto di sottocampionamento da usare per la codifica YCrCb.

Il valore predefinito [**è WICJpegYCrCbSubsampling420.**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption)

### <a name="suppressapp0-option"></a>Opzione SuppressApp0

Specifica se eliminare la scrittura dei metadati App0 durante la codifica dei dati dell'immagine.

Il valore predefinito è **FALSE.**

## <a name="decoding"></a>Decodifica

L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md) Per altre informazioni sull'uso di dati di immagine decodificati, vedere Cenni [preliminari sulle origini bitmap.](-wic-bitmapsources.md)

Il codec JPEG nativo supporta anche [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) nella decodifica dei fotogrammi aggiungendo opzioni avanzate per la decodifica di un flusso di immagine. Per altre informazioni su queste opzioni avanzate, vedere Cenni preliminari [sulle origini bitmap.](-wic-bitmapsources.md)

 

 
