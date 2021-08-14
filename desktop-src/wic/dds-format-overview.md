---
description: Fornisce informazioni sul codec DDS nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Panoramica del formato DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a9fd00f17d17b7bb227a04e56bbc9369de86eb03f9c953a73267400d4a6df9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204478"
---
# <a name="dds-format-overview"></a>Panoramica del formato DDS

In questo argomento vengono fornite informazioni sul codec DDS nativo disponibile tramite Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Codec Identity

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



| Componente              | Descrizione        |
|------------------------|--------------------|
| Nomi formali         | Superficie DirectDraw |
| Estensioni di file | Dds                |
| tipo MIME              | image/vnd-ms.dds   |



 

Nella tabella seguente sono elencati i GUID utilizzati per identificare i componenti nativi del codec DDS.



| Componente        | Nome descrittivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatDds | 9967cb95-2e85-4ac8-8ca283d7ccd425c9 |
| Decodificatore          | CLSID \_ WICDdsDecoder     | 9053699f-a341-429d-9e90ee437cf80c73 |
| Codificatore          | CLSID \_ WICDdsEncoder     | a61dde94-66ce-4ac1-881b71680588895e |



 

## <a name="pixel-format-support"></a>Supporto del formato pixel

Si noti che il formato DDS supporta qualsiasi [**valore DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valido. Tuttavia, il codec WIC DDS supporta solo file di decodifica e codifica contenenti i formati seguenti:

-   FORMATO DXGI \_ \_ BC1 \_ UNORM
-   FORMATO DXGI \_ \_ BC2 \_ UNORM
-   FORMATO DXGI \_ \_ BC3 \_ UNORM

## <a name="encoding"></a>Codifica

Le API di codifica WIC sono progettate per essere indipendenti dal codec e pertanto la codifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla codifica delle immagini tramite l'API WIC, vedere Cenni [preliminari sulla codifica.](-wic-creating-encoder.md)

Il formato di file DDS presenta requisiti univoci che derivano dal supporto di concetti come mipmap e matrici di trame. Per esercitare il controllo completo sulla codifica delle immagini DDS, è necessario usare [**l'interfaccia IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) per impostare i parametri di codifica specifici di DDS.

## <a name="decoding"></a>Decodifica

Le API di decodifica WIC sono progettate per essere indipendenti dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md) Per altre informazioni sull'uso di dati immagine decodificati, vedere Cenni preliminari [sulle origini bitmap.](-wic-bitmapsources.md)

## <a name="block-compressed-data-access"></a>Bloccare l'accesso ai dati compressi

Oltre a supportare le interfacce codec WIC standard, il decodificatore DDS fornisce l'accesso diretto ai dati compressi in blocchi nativi usando le interfacce specifiche di DDS, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) e [**IWICDdsFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode) Per usare queste interfacce, chiamare QueryInterface rispettivamente da [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)

 

 
