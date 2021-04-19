---
description: In questo argomento vengono fornite informazioni sul codec ICO nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Panoramica sul formato ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d370497e9231d6deb8d1793a26a53565b5cd99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317866"
---
# <a name="ico-format-overview"></a>Panoramica sul formato ICO

In questo argomento vengono fornite informazioni sul codec ICO nativo disponibile tramite Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identità codec

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



|                        |                   |
|------------------------|-------------------|
| Nome/i formale/i         | Formato dell'icona (ICO) |
| Estensioni del nome di file | ico               |
| tipo MIME              | immagine/ICO         |
| Supporto delle specifiche  |                   |



 

La tabella seguente elenca i GUID usati per identificare i componenti del codec ICO nativi.



| Componente        | Nome descrittivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatIco | a3a860c4-338f-4c17-919afba4b5628f21 |
| Decodificatore          | \_WICICODECODER CLSID     | c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe |
| Codificatore          | NON DISPONIBILE            | NON DISPONIBILE                       |



 

## <a name="encoding"></a>Codifica

WIC non fornisce un codificatore di immagini ICO nativo.

## <a name="decoding"></a>Decodifica

L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md). Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).

 

 



