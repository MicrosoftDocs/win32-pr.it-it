---
description: In questo argomento vengono fornite informazioni sul codec GIF nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Panoramica del formato GIF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f592b50300edf79c71ff4050a2c0d5aeba8b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232468"
---
# <a name="gif-format-overview"></a>Panoramica del formato GIF

In questo argomento vengono fornite informazioni sul codec GIF nativo disponibile tramite Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identità codec

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



|                        |                                       |
|------------------------|---------------------------------------|
| Nome/i formale/i         | Graphics Interchange Format 89a (GIF) |
| Estensioni del nome di file | GIF                                   |
| tipo MIME              | image/gif                             |
| Supporto delle specifiche  | Specifica GIF 89a/89m             |



 

La tabella seguente elenca i GUID usati per identificare i componenti dei codec GIF nativi.



| Componente        | Nome descrittivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatGif | 1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5 |
| Decodificatore          | \_WICGIFDECODER CLSID     | 381dda3c-9ce9-4834-a23e1f98f8fc52be |
| Codificatore          | \_WICGIFENCODER CLSID     | 114f5598-0b22-40a0-86a1c83ea495adbd |



 

## <a name="encoding"></a>Codifica

L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla codifica delle immagini tramite l'API WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opzioni del codificatore

I codec abilitati per WIC differiscono a livello di opzione di codifica. Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore. Le opzioni del codificatore possono essere opzioni supportate per WIC di base disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportati) o per le opzioni specifiche del codec progettate dal codec del formato di immagine. Per gestire queste opzioni di codifica durante il processo di codifica, WIC utilizza l'interfaccia [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Per ulteriori informazioni sull'utilizzo dell'interfaccia **IPropertyBag2** per la codifica WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).

Il codificatore GIF non supporta le opzioni WIC di base e non fornisce opzioni del codificatore personalizzate. Se un'opzione del codificatore è presente nell'elenco di opzioni [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , viene ignorata.

## <a name="decoding"></a>Decodifica

L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md). Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).

 

 
