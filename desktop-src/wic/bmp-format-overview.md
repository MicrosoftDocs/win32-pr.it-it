---
description: In questo argomento vengono fornite informazioni sul codec BMP nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Panoramica del formato BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975f27af5b731ed1f62f3571109553848705239
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444962"
---
# <a name="bmp-format-overview"></a>Panoramica del formato BMP

In questo argomento vengono fornite informazioni sul codec BMP nativo disponibile tramite Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identità codec

Nella tabella seguente vengono fornite informazioni di identificazione dei codec.



| Componente              | Descrizione           |
|------------------------|-----------------------|
| Nomi formali         | Formato bitmap di Windows |
| Estensioni di file | bmp, dib              |
| tipo MIME              | image/bmp             |
| Supporto delle specifiche  | Specifica BMP v5  |



 

Nella tabella seguente sono elencati i GUID usati per identificare i componenti nativi del codec BMP.



| Componente        | Nome descrittivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatBmp | 0af1d87e-fcfe-4188-bdeba7906471cbe3 |
| Decodificatore          | CLSID \_ WICBmpDecoder     | 6b462062-7cbf-400d-9fdb813dd10f2778 |
| Codificatore          | CLSID \_ WICBmpEncoder     | 69be8bb4-d66d-47c8-865aed1589433782 |



 

## <a name="encoding"></a>Codifica

L'API di codifica WIC è progettata per essere indipendente dal codec e pertanto la codifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla codifica delle immagini tramite l'API WIC, vedere Cenni [preliminari sulla codifica](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opzioni del codificatore

I codec abilitati per WIC differiscono a livello di opzione di codifica. Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore. Le opzioni del codificatore possono essere opzioni di base supportate da WIC disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportate) o opzioni specifiche del codec progettate dal codec del formato immagine. Per gestire queste opzioni di codifica durante il processo di codifica, WIC usa [**l'interfaccia IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Per altre informazioni sull'uso **dell'interfaccia IPropertyBag2** per la codifica WIC, vedere Cenni [preliminari sulla codifica](-wic-creating-encoder.md).

Nella tabella seguente sono elencate le opzioni del codificatore WIC supportate dal codec BMP nativo.



| Nome della proprietà               | VARTYPE      | Gamma valori                      | Valore predefinito      |
|-----------------------------|--------------|----------------------------------|--------------------|
| **EnableV5Header32bppBGRA** | **VT \_ BOOL** | **VARIANT \_ TRUE/VARIANT \_ FALSE** | **VARIANT \_ FALSE** |



 

### <a name="enablev5header32bppbgra"></a>EnableV5Header32bppBGRA

Specifica se consentire la codifica dei dati nel formato pixel \_ GUID WICPixelFormat32bppBGRA. Se questa opzione è impostata su **VARIANT \_ TRUE,** il BMP verrà scritto con un'intestazione BITMAPV5HEADER.

Il valore predefinito è **VARIANT \_ FALSE.**

Se un'opzione del codificatore è presente nell'elenco di opzioni IPropertyBag2 non supportato dal codec, viene ignorata.

Nota per i file BMP di Windows a 16 e 32 bit, il codec BMP ignora qualsiasi canale alfa, poiché molti file di immagine legacy contengono dati non validi in questo canale aggiuntivo. A partire da Windows 8, i file BMP di Windows a 32 bit scritti usando **BITMAPV5HEADER** con contenuto del canale alfa valido vengono letti come WICPixelFormat32bppBGRA

## <a name="decoding"></a>Decodifica

L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md) Per altre informazioni sull'uso di dati immagine decodificati, vedere Panoramica [delle origini bitmap](-wic-bitmapsources.md).

 

 
