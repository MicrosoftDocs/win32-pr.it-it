---
description: In questo argomento vengono fornite informazioni sul codec DNG nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Panoramica del formato DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0815d6a24bb8e57e6c64b90f9e9068765838e148
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444932"
---
# <a name="dng-format-overview"></a>Panoramica del formato DNG

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

In questo argomento vengono fornite informazioni sul codec DNG nativo disponibile tramite Windows Imaging Component (WIC).

-   [Codec Identity](#codec-identity)
-   [Decodifica](#decoding)

## <a name="codec-identity"></a>Codec Identity

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



|     Componente          |  Descrizione                                         |
|------------------------|------------------------------------------------------|
| Nomi formali         | Digital Negative (DNG)                               |
| Estensioni di file | .dng                                                 |
| Tipi MIME           | image/DNG                                            |
| Supporto delle specifiche  | Digital Negative (DNG) Specification Version 1.4.0.0 |



 

Nella tabella seguente sono elencati i GUID utilizzati per identificare i componenti nativi del codec DNG.



| Componente        | Nome descrittivo             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatAdng | f3ff6d0d-38c0-41c4-b1fe1f3824f17b84 |
| Decodificatore          | CLSID \_ WICAdngDecoder     | 981d9411-909e-42a7-8f5da747ff052edb |



 

## <a name="decoding"></a>Decodifica

L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md) Per altre informazioni sull'uso di dati di immagine decodificati, vedere Cenni [preliminari sulle origini bitmap.](-wic-bitmapsources.md)

Il decodificatore non supporta la decodifica dei dati dei sensori non elaborati e supporta solo i file con una rappresentazione di immagine non non elaborata incorporata in un IFD con NewSubFileType uguale a 1.

 

 



