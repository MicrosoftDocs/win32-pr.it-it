---
description: In questo argomento vengono fornite informazioni sul codec PNG nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Panoramica del formato PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb00b7530a22fcdbcce112053431ace5e553383
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444442"
---
# <a name="png-format-overview"></a>Panoramica del formato PNG

In questo argomento vengono fornite informazioni sul codec PNG nativo disponibile tramite Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identità codec

Nella tabella seguente vengono fornite informazioni di identificazione dei codec.



|     Componente          | Descrizione                     |
|------------------------|---------------------------------|
| Nomi formali         | Portable Network Graphics (PNG) |
| Estensioni di file | png                             |
| tipo MIME              | image/png                       |
| Supporto delle specifiche  | Specifica PNG 1.2           |



 

Nella tabella seguente sono elencati i GUID usati per identificare i componenti nativi del codec PNG.



| Componente        | Nome descrittivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatPng | 1b7cfaf4-713f-473c-bbcd6137425faeaf |
| Decodificatore          | CLSID \_ WICPngDecoder     | 389ea17b-5078-4cde-b6ef25c15175c751 |
| Codificatore          | CLSID \_ WICPngEncoder     | 27949969-876a-41d7-9447568f6a35a4dc |



 

### <a name="windows-8-and-later"></a>Windows 8 e versioni successive

A partire da Windows 8 WIC fornisce un decodificatore PNG aggiuntivo

## <a name="encoding"></a>Codifica

L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla codifica delle immagini tramite l'API WIC, vedere Cenni [preliminari sulla codifica](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opzioni del codificatore

I codec abilitati per WIC differiscono a livello di opzione di codifica. Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore. Le opzioni del codificatore possono essere opzioni di base supportate da WIC disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportate) o opzioni specifiche del codec progettate dal codec del formato immagine. Per gestire queste opzioni di codifica durante il processo di codifica, WIC usa [**l'interfaccia IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Per altre informazioni sull'uso **dell'interfaccia IPropertyBag2** per la codifica WIC, vedere Cenni [preliminari sulla codifica](-wic-creating-encoder.md).

Il codec PNG usa le opzioni del codificatore WIC di base. Nella tabella seguente sono elencate le opzioni del codificatore WIC supportate dal codec PNG nativo.



| Nome della proprietà   | VARTYPE  | Gamma valori                                                 | Valore predefinito                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| InterlaceOption | VT \_ BOOL | **TRUE** / **FALSE**                                          | **FALSE**                                                        |
| FilterOption    | VT \_ UI1  | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

Se un'opzione del codificatore è presente nell'elenco di opzioni [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) non supportato dal codec, viene ignorata.

### <a name="interlaceoption"></a>InterlaceOption

Specifica se codificare i dati dell'immagine come interlacciati.

Il valore predefinito è **FALSE.**

### <a name="filteroption"></a>FilterOption

Specifica l'opzione di filtro da utilizzare per la compressione delle immagini.

Il valore predefinito è [**WICPngFilterUnspecified.**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)

## <a name="decoding"></a>Decodifica

L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md) Per altre informazioni sull'uso di dati immagine decodificati, vedere Panoramica [delle origini bitmap](-wic-bitmapsources.md).

Il codec PNG nativo supporta anche [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) per la decodifica dei fotogrammi aggiungendo opzioni avanzate per la decodifica di un flusso di immagine. Per altre informazioni su queste opzioni avanzate, vedere Panoramica [delle origini bitmap](-wic-bitmapsources.md).

 

 
