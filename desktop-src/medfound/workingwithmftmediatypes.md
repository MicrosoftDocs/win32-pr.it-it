---
description: Uso dei tipi di supporto MFT
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Uso dei tipi di supporto MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98bfc996704f6069ca1d16570b33f456ea1cc115
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234482"
---
# <a name="working-with-mft-media-types"></a>Uso dei tipi di supporto MFT

Un tipo di supporto è un modo per descrivere il formato di un flusso multimediale. In Media Foundation i tipi di supporto sono rappresentati dall'interfaccia **IMFMediaType** . Questa interfaccia eredita l'interfaccia **IMFAttributes** . I dettagli di un tipo di supporto vengono specificati come attributi.

Per creare un nuovo tipo di supporto, chiamare la funzione **MFCreateMediaType** . Questa funzione restituisce un puntatore all'interfaccia **IMFMediaType** . Il tipo di supporto inizialmente non ha attributi.

Il Media Foundation SDK fornisce diverse funzioni di supporto per l'inizializzazione di tipi di supporto da strutture di formato. Ad esempio, la funzione **MFInitMediaTypeFromVideoInfoHeader** Inizializza un tipo di video da una struttura **VIDEOINFOHEADER** e la funzione **MFInitMediaTypeFromWaveFormatEx** Inizializza un tipo di video da una struttura **WAVEFORMATEX** o **WAVEFORMATEXTENSIBLE** .

I tipi di formato usati dai codec sono generalmente limitati a quelli descritti dalle strutture **VIDEOINFOHEADER** e **WAVEFORMATEX** .

Altre informazioni sulla creazione e l'accesso a Media Foundation tipi di supporto sono disponibili nella documentazione di Media Foundation SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



