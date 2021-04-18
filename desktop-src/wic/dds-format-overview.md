---
description: Fornisce informazioni sul codec DDS nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Cenni preliminari sul formato DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c45222a66d5a250caaf46db465d2359e09b3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312942"
---
# <a name="dds-format-overview"></a>Cenni preliminari sul formato DDS

In questo argomento vengono fornite informazioni sul codec DDS nativo disponibile tramite Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identità codec

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



|                        |                    |
|------------------------|--------------------|
| Nome/i formale/i         | Superficie DirectDraw |
| Estensioni del nome di file | DDS                |
| tipo MIME              | Image/VND-ms. DDS   |



 

La tabella seguente elenca i GUID usati per identificare i componenti dei codec DDS nativi.



| Componente        | Nome descrittivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatDds | 9967cb95-2e85-4ac8-8ca283d7ccd425c9 |
| Decodificatore          | \_WICDDSDECODER CLSID     | 9053699f-a341-429d-9e90ee437cf80c73 |
| Codificatore          | \_WICDDSENCODER CLSID     | a61dde94-66CE-4ac1-881b71680588895e |



 

## <a name="pixel-format-support"></a>Supporto del formato pixel

Si noti che il formato DDS supporta qualsiasi valore di [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valido. Tuttavia, il codec di WIC DDS supporta solo la decodifica e la codifica di file contenenti i formati seguenti:

-   \_Formato DXGI \_ BC1 \_ UNORM
-   \_Formato DXGI \_ BC2 \_ UNORM
-   \_Formato DXGI \_ BC3 \_ UNORM

## <a name="encoding"></a>Codifica

Le API di codifica WIC sono progettate per essere indipendenti dal codec e pertanto la codifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla codifica delle immagini tramite l'API WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).

Il formato di file DDS presenta requisiti univoci che derivano dal supporto per concetti quali mipmap e matrici di trame. Per esercitare il controllo completo sulla codifica delle immagini DDS, è necessario usare l'interfaccia [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) per impostare i parametri di codifica specifici di DDS.

## <a name="decoding"></a>Decodifica

Le API di decodifica WIC sono progettate per essere indipendenti dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md). Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).

## <a name="block-compressed-data-access"></a>Blocca l'accesso ai dati compressi

Oltre a supportare le interfacce standard del codec WIC, il decodificatore DDS fornisce l'accesso diretto ai dati compressi in blocchi nativi usando le interfacce specifiche di DDS, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) e [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode). Per usare queste interfacce, chiamare rispettivamente QueryInterface di [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).

 

 
