---
description: In questo argomento vengono fornite informazioni sul codec BMP nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Panoramica del formato BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3492189f80b43915bab94a7ea8359f2e5950f7c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756911"
---
# <a name="bmp-format-overview"></a>Panoramica del formato BMP

In questo argomento vengono fornite informazioni sul codec BMP nativo disponibile tramite Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identità codec

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



|                        |                       |
|------------------------|-----------------------|
| Nome/i formale/i         | Formato bitmap Windows |
| Estensioni del nome di file | BMP, DIB              |
| tipo MIME              | image/bmp             |
| Supporto delle specifiche  | Specifica BMP V5  |



 

La tabella seguente elenca i GUID usati per identificare i componenti dei codec BMP nativi.



| Componente        | Nome descrittivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatBmp | 0af1d87e-fcfe-4188-bdeba7906471cbe3 |
| Decodificatore          | \_WICBMPDECODER CLSID     | 6b462062-7cbf-400D-9fdb813dd10f2778 |
| Codificatore          | \_WICBMPENCODER CLSID     | 69be8bb4-d66d-47c8-865aed1589433782 |



 

## <a name="encoding"></a>Codifica

L'API di codifica WIC è progettata per essere indipendente dal codec e pertanto la codifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla codifica delle immagini tramite l'API WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opzioni del codificatore

I codec abilitati per WIC differiscono a livello di opzione di codifica. Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore. Le opzioni del codificatore possono essere opzioni supportate per WIC di base disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportati) o per le opzioni specifiche del codec progettate dal codec del formato di immagine. Per gestire queste opzioni di codifica durante il processo di codifica, WIC utilizza l'interfaccia [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Per ulteriori informazioni sull'utilizzo dell'interfaccia **IPropertyBag2** per la codifica WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).

Nella tabella seguente sono elencate le opzioni del codificatore WIC supportate dal codec BMP nativo.



| Nome della proprietà               | VARTYPE      | Gamma valori                      | Valore predefinito      |
|-----------------------------|--------------|----------------------------------|--------------------|
| **EnableV5Header32bppBGRA** | **\_bool VT** | **VARIANT \_ true/Variant \_ false** | **VARIANTE \_ false** |



 

### <a name="enablev5header32bppbgra"></a>EnableV5Header32bppBGRA

Specifica se consentire la codifica dei dati nel \_ formato pixel WICPIXELFORMAT32BPPBGRA GUID. Se questa opzione è impostata su **Variant \_ true**, il formato BMP verrà scritto con un'intestazione BITMAPV5HEADER.

Il valore predefinito è **Variant \_ false**.

Se un'opzione del codificatore è presente nell'elenco di opzioni IPropertyBag2 che il codec non supporta, viene ignorato.

Nota per i file BMP Windows a 16 bit e a 32 bit, il codec BMP ignora qualsiasi canale alfa, in quanto molti file di immagine legacy contengono dati non validi in questo canale aggiuntivo. A partire da Windows 8, i file di Windows BMP a 32 bit scritti usando **BITMAPV5HEADER** con contenuto del canale alfa valido vengono letti come WICPixelFormat32bppBGRA

## <a name="decoding"></a>Decodifica

L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md). Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).

 

 
