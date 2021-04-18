---
description: In questo argomento vengono fornite informazioni sul codec JPEG nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Panoramica sul formato JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953d1d6a02e47b41d1b7cf872f3381cd640151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312389"
---
# <a name="jpeg-format-overview"></a>Panoramica sul formato JPEG

In questo argomento vengono fornite informazioni sul codec JPEG nativo disponibile tramite Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identità codec

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



|                        |                                         |
|------------------------|-----------------------------------------|
| Nome/i formale/i         | Joint Photographic Experts Group (JPEG) |
| Estensioni del nome di file | JPE, JPEG, jpg                          |
| tipo MIME              | image/jpeg, image/JPE, image/jpg        |
| Supporto delle specifiche  | Specifica JFIF 1,02                 |



 

Nella tabella seguente sono elencati i GUID utilizzati per identificare i componenti dei codec JPEG nativi.



| Componente        | Nome descrittivo             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatJpeg | 19e4a5aa-5662-4fc5-a0c01758028e1057 |
| Decodificatore          | \_WICJPEGDECODER CLSID     | 9456a480-e88b-43ea-9e730b2d9b71b1ca |
| Codificatore          | \_WICJPEGENCODER CLSID     | 1a34f5c1-4a5a-46dc-b6441f4567e7a676 |



 

## <a name="encoding"></a>Codifica

L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla codifica delle immagini tramite l'API WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opzioni del codificatore

I codec abilitati per WIC differiscono a livello di opzione di codifica. Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore. Le opzioni del codificatore possono essere opzioni supportate per WIC di base disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportati) o per le opzioni specifiche del codec progettate dal codec del formato di immagine. Per gestire queste opzioni di codifica durante il processo di codifica, WIC utilizza l'interfaccia [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Per ulteriori informazioni sull'utilizzo dell'interfaccia **IPropertyBag2** per la codifica WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).

Il codec JPEG usa le opzioni WIC di base. Nella tabella seguente sono elencate le opzioni del codificatore WIC supportate dal codec JPEG nativo.



| Nome della proprietà                                        | VARTYPE           | Gamma valori                                                                       | Valore predefinito                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ImageQuality](#imagequality-option)                 | \_R4 VT            | 0-1,0                                                                           | 0.9                                                                            |
| [BitmapTransform](#bitmaptransform-option)           | \_Ui1 VT           | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [Luminanza](#luminance-option)                       | \_Array VT UI4/VT \_ | 64 voci (DCT)                                                                  | Tabella luminanza predefinita.                                                       |
| [Chrominance](#chrominance-option)                   | \_Array VT UI4/VT \_ | 64 voci (DCT)                                                                  | Tabella cromatura predefinita.                                                     |
| [JpegYCrCbSubsampling](#jpegycrcbsubsampling-option) | \_Ui1 VT           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [SuppressApp0](/windows)                       | \_bool VT          | Valore **true** / **False**                                                                | **FALSE**                                                                      |



 

Se un'opzione del codificatore è presente nell'elenco di opzioni [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) che il codec non supporta, viene ignorato.

### <a name="imagequality-option"></a>ImageQuality-opzione

Specifica la fedeltà dell'immagine desiderata. 0,0 indica che la fedeltà più bassa possibile e 1,0 specifica la massima fedeltà.

Il valore predefinito è 0,9.

### <a name="bitmaptransform-option"></a>BitmapTransform-opzione

Specifica la modalità di trasformazione dell'immagine durante la decodifica delle immagini. Questa opzione deve essere impostata su uno dei valori di enumerazione [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .

Il valore predefinito è [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).

### <a name="luminance-option"></a>Opzione luminanza

Specifica la tabella del livello di luminosità in scala di grigi da usare per la codifica.

### <a name="chrominance-option"></a>Cromatura-opzione

Specifica la tabella cromatura da utilizzare per la codifica.

### <a name="jpegycrcbsubsampling-option"></a>JpegYCrCbSubsampling-opzione

Specifica il rapporto di sottocampionamento da utilizzare per la codifica YCrCb.

Il valore predefinito è [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).

### <a name="suppressapp0-option"></a>SuppressApp0-opzione

Specifica se escludere la scrittura dei metadati APP0 durante la codifica dei dati dell'immagine.

Il valore predefinito è **false**.

## <a name="decoding"></a>Decodifica

L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md). Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).

Il codec JPEG nativo supporta anche [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) sulla decodifica dei frame aggiungendo opzioni avanzato per la decodifica di un flusso di immagini. Per ulteriori informazioni su queste opzioni avanzate, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).

 

 
