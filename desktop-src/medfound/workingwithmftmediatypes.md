---
description: Uso dei tipi di supporti MFT
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Uso dei tipi di supporti MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ead31c4291cf41cff62f4341227bf0ee1ad22d12e96a6c9eff87ff5a3e6faa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886951"
---
# <a name="working-with-mft-media-types"></a>Uso dei tipi di supporti MFT

Un tipo di supporto è un modo per descrivere il formato di un flusso multimediale. In Media Foundation, i tipi di supporti sono rappresentati **dall'interfaccia IMFMediaType.** Questa interfaccia eredita **l'interfaccia IMFAttributes.** I dettagli di un tipo di supporto vengono specificati come attributi.

Per creare un nuovo tipo di supporto, chiamare la **funzione MFCreateMediaType.** Questa funzione restituisce un puntatore **all'interfaccia IMFMediaType.** Il tipo di supporto inizialmente non ha attributi.

L Media Foundation SDK fornisce diverse funzioni helper per l'inizializzazione dei tipi di supporti dalle strutture di formato. Ad esempio, la funzione **MFInitMediaTypeFromVideoInfoHeader** inizializza un tipo di video da una struttura **VIDEOINFOHEADER** e la funzione **MFInitMediaTypeFromWaveFormatEx** inizializza un tipo di video da una **struttura WAVEFORMATEX** o **WAVEFORMATEXTENSIBLE.**

I tipi di formato usati dai codec sono in genere limitati a quelli descritti dalle strutture **VIDEOINFOHEADER** e **WAVEFORMATEX.**

Altre informazioni sulla creazione e l'accesso Media Foundation tipi di supporti sono disponibili nella documentazione Media Foundation SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei codec MFT](workingwithcodecmfts.md)
</dt> </dl>

 

 



