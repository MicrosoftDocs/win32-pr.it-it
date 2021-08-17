---
title: Novità (sdk Windows Media Format 11)
description: Novità
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows Media Format SDK, novità
- Windows Media Format SDK, funzionalità
- Windows Media Format SDK, nuove funzionalità
- Windows MEDIA Format SDK, API estese client
- Windows SDK formato multimediale, aggiornamenti DRM
- Windows SDK formato multimediale, aggiornamenti dei codec
- Windows MEDIA Format SDK, immagini di anteprima
- DRM (Digital Rights Management), nuove funzionalità
- DRM (Digital Rights Management),nuove funzionalità
- anteprime in miniatura delle immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1174078ce6fde94794cff32f4384de4a6c7b774dec2943fa91f2ec279d9d718e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963890"
---
# <a name="whats-new-windows-media-format-11-sdk"></a>Novità (sdk Windows Media Format 11)

L Windows SDK di Media Format 11 introduce nuove funzionalità DRM (Digital Rights Management). Le modifiche seguenti sono state apportate all'SDK dalla versione 9.5.

## <a name="windows-media-drm-client-extended-apis"></a>Windows API estese del client DRM multimediale

Il Windows Media Format 11 SDK viene fornito con un nuovo set di API DRM. Queste API vengono implementate nella propria libreria. Molte delle funzionalità DRM supportate dagli oggetti di Windows Media Format SDK sono supportate anche dalle API estese del client Windows Media DRM. La differenza principale nelle nuove API è che non si basano sulla presenza di un file ASF per funzionare. Al contrario, le nuove API si occupano direttamente dell'archivio licenze locale, spesso usando l'ID chiave per identificare le licenze.

Per altre informazioni, vedere la [Windows Media DRM Client Extended APIs (API](windows-media-drm-client-extended-apis.md) estese del client DRM multimediale).

## <a name="updated-codecs"></a>Codec aggiornati

Il codec Windows Media Video 9 Advanced Profile è stato aggiornato per produrre un flusso di bit compresso conforme allo standard SMPTE VC-1 pubblicato.

Il codec Windows Media Audio 10 Professional è incluso anche in questa versione dell'SDK. Il nuovo codec audio offre una qualità migliorata a velocità in bit inferiori.

## <a name="thumbnail-right"></a>Anteprima a destra

Le applicazioni possono richiedere una nuova azione DRM da leggere dal video per creare un'immagine di anteprima. In questo modo le applicazioni possono creare e visualizzare immagini di anteprima per i file video senza aprire il file per la riproduzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni su Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




