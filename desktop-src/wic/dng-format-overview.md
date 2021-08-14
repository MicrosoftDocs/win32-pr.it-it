---
description: Questo argomento fornisce informazioni sul codec DNG nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Panoramica del formato DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32719e3fa9f45802058708e83635e52e287524496ae49f13f2168362358a7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204378"
---
# <a name="dng-format-overview"></a>Panoramica del formato DNG

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Questo argomento fornisce informazioni sul codec DNG nativo disponibile tramite Windows Imaging Component (WIC).

-   [Identità codec](#codec-identity)
-   [Decodifica](#decoding)

## <a name="codec-identity"></a>Identità codec

Nella tabella seguente vengono fornite informazioni di identificazione dei codec.



|     Componente          |  Descrizione                                         |
|------------------------|------------------------------------------------------|
| Nomi formali         | Negativo digitale (DNG)                               |
| Estensioni di file | .dng                                                 |
| Tipi MIME           | image/DNG                                            |
| Supporto delle specifiche  | Digital Negative (DNG) Specification Version 1.4.0.0 |



 

Nella tabella seguente sono elencati i GUID usati per identificare i componenti nativi del codec DNG.



| Componente        | Nome descrittivo             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatAdng | f3ff6d0d-38c0-41c4-b1fe1f3824f17b84 |
| Decodificatore          | CLSID \_ WICAdngDecoder     | 981d9411-909e-42a7-8f5da747ff052edb |



 

## <a name="decoding"></a>Decodifica

L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md) Per altre informazioni sull'uso di dati immagine decodificati, vedere Panoramica [delle origini bitmap](-wic-bitmapsources.md).

Il decodificatore non supporta la decodifica dei dati dei sensori non elaborati e supporta solo i file con una rappresentazione di immagine non non elaborata incorporata in un IFD con NewSubFileType uguale a 1.

 

 



