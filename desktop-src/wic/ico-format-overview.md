---
description: Questo argomento fornisce informazioni sul codec ICO nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Panoramica del formato ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf90f0a31beb2d004dcb43e08cb0b6b1539021071ff2cb3302b3076033bc833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204071"
---
# <a name="ico-format-overview"></a>Panoramica del formato ICO

Questo argomento fornisce informazioni sul codec ICO nativo disponibile tramite Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Codec Identity

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



|   Componente            | Descrizione       |
|------------------------|-------------------|
| Nomi formali         | Formato icona (ICO) |
| Estensioni di file | Ico               |
| tipo MIME              | image/ico         |
| Supporto delle specifiche  |                   |



 

Nella tabella seguente sono elencati i GUID usati per identificare i componenti nativi del codec ICO.



| Componente        | Nome descrittivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatIco | a3a860c4-338f-4c17-919afba4b5628f21 |
| Decodificatore          | CLSID \_ WICIcoDecoder     | c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe |
| Codificatore          | NON DISPONIBILE            | NON DISPONIBILE                       |



 

## <a name="encoding"></a>Codifica

WIC non fornisce un codificatore di immagini ICO nativo.

## <a name="decoding"></a>Decodifica

L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md) Per altre informazioni sull'uso di dati immagine decodificati, vedere Cenni preliminari [sulle origini bitmap.](-wic-bitmapsources.md)

 

 



