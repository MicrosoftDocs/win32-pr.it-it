---
description: Questo argomento fornisce informazioni sul codec DNG nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Panoramica sul formato DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f766356f7c13d7b2bb25adab5411ae55c2735f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345816"
---
# <a name="dng-format-overview"></a>Panoramica sul formato DNG

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Questo argomento fornisce informazioni sul codec DNG nativo disponibile tramite Windows Imaging Component (WIC).

-   [Identità codec](#codec-identity)
-   [Decodifica](#decoding)

## <a name="codec-identity"></a>Identità codec

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



|                        |                                                      |
|------------------------|------------------------------------------------------|
| Nome/i formale/i         | Negativo digitale (DNG)                               |
| Estensioni del nome di file | .dng                                                 |
| Tipi MIME           | Image/DNG                                            |
| Supporto delle specifiche  | Versione della specifica digitale negativa (DNG) 1.4.0.0 |



 

La tabella seguente elenca i GUID usati per identificare i componenti dei codec DNG nativi.



| Componente        | Nome descrittivo             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatAdng | f3ff6d0d-38c0-41c4-b1fe1f3824f17b84 |
| Decodificatore          | \_WICADNGDECODER CLSID     | 981d9411-909e-42a7-8f5da747ff052edb |



 

## <a name="decoding"></a>Decodifica

L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md). Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).

Il decodificatore non supporta la decodifica dei dati dei sensori non elaborati e supporta solo i file con una rappresentazione di immagine non RAW incorporata in un IFD con NewSubFileType uguale a 1.

 

 



