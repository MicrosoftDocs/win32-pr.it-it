---
description: In questo argomento vengono fornite informazioni sul codec PNG nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Panoramica del formato PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118d6af831c8fb6f8cacc8407e90f610c0fc426d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316380"
---
# <a name="png-format-overview"></a>Panoramica del formato PNG

In questo argomento vengono fornite informazioni sul codec PNG nativo disponibile tramite Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identità codec

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



|                        |                                 |
|------------------------|---------------------------------|
| Nome/i formale/i         | Portable Network Graphics (PNG) |
| Estensioni del nome di file | png                             |
| tipo MIME              | image/png                       |
| Supporto delle specifiche  | Specifica PNG 1,2           |



 

La tabella seguente elenca i GUID usati per identificare i componenti dei codec PNG nativi.



| Componente        | Nome descrittivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatPng | 1b7cfaf4-713f-473c-bbcd6137425faeaf |
| Decodificatore          | \_WICPNGDECODER CLSID     | 389ea17b-5078-4cde-b6ef25c15175c751 |
| Codificatore          | \_WICPNGENCODER CLSID     | 27949969-876a-41d7-9447568f6a35a4dc |



 

### <a name="windows-8-and-later"></a>Windows 8 e versioni successive

A partire da Windows 8 WIC fornisce un decoder PNG aggiuntivo

## <a name="encoding"></a>Codifica

L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla codifica delle immagini tramite l'API WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opzioni del codificatore

I codec abilitati per WIC differiscono a livello di opzione di codifica. Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore. Le opzioni del codificatore possono essere opzioni supportate per WIC di base disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportati) o per le opzioni specifiche del codec progettate dal codec del formato di immagine. Per gestire queste opzioni di codifica durante il processo di codifica, WIC utilizza l'interfaccia [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Per ulteriori informazioni sull'utilizzo dell'interfaccia **IPropertyBag2** per la codifica WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).

Il codec PNG usa le opzioni di base del codificatore WIC. Nella tabella seguente sono elencate le opzioni del codificatore WIC supportate dal codec PNG nativo.



| Nome della proprietà   | VARTYPE  | Gamma valori                                                 | Valore predefinito                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| InterlaceOption | \_bool VT | Valore **true** / **False**                                          | **FALSE**                                                        |
| FilterOption    | \_Ui1 VT  | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

Se un'opzione del codificatore è presente nell'elenco di opzioni [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) che il codec non supporta, viene ignorato.

### <a name="interlaceoption"></a>InterlaceOption

Specifica se codificare i dati dell'immagine come interlacciato.

Il valore predefinito è **false**.

### <a name="filteroption"></a>FilterOption

Specifica l'opzione di filtro da utilizzare per la compressione dell'immagine.

Il valore predefinito è [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).

## <a name="decoding"></a>Decodifica

L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md). Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).

Il codec PNG nativo supporta anche [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) sulla decodifica dei frame aggiungendo opzioni avanzate per la decodifica di un flusso di immagini. Per ulteriori informazioni su queste opzioni avanzate, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).

 

 
