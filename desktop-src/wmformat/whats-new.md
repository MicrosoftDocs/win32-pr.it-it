---
title: Novità (Windows Media Format 11 SDK)
description: Novità
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows Media Format SDK, novità
- Windows Media Format SDK, funzionalità
- Windows Media Format SDK, nuove funzionalità
- Windows Media Format SDK, API client estese
- Windows Media Format SDK, aggiornamenti DRM
- Windows Media Format SDK, aggiornamenti dei codec
- Windows Media Format SDK, immagini di anteprima
- Digital Rights Management (DRM), nuove funzionalità
- DRM (Digital Rights Management), nuove funzionalità
- anteprime in miniatura delle immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739503"
---
# <a name="whats-new-windows-media-format-11-sdk"></a>Novità (Windows Media Format 11 SDK)

Windows Media Format 11 SDK introduce nuove funzionalità di Digital Rights Management (DRM). Le modifiche seguenti sono state apportate all'SDK dalla versione 9,5.

## <a name="windows-media-drm-client-extended-apis"></a>API estese del client Windows Media DRM

Windows Media Format 11 SDK viene fornito con un nuovo set di API di DRM. Queste API sono implementate nella propria libreria. Molte delle funzionalità DRM supportate dagli oggetti di Windows Media Format SDK sono supportate anche dalle API estese del client Windows Media DRM. La differenza principale tra le nuove API è che non si basano su un file ASF da usare. Al contrario, le nuove API gestiscono direttamente l'archivio licenze locale, usando spesso l'ID chiave per identificare le licenze.

Per ulteriori informazioni, vedere la documentazione sulle [API estese del client Windows Media DRM](windows-media-drm-client-extended-apis.md) .

## <a name="updated-codecs"></a>Codec aggiornati

Il codec del profilo avanzato Windows Media Video 9 è stato aggiornato per produrre un flusso di bit compresso che è conforme allo standard SMPTE VC-1 pubblicato.

Il codec Windows Media Audio 10 Professional è incluso anche in questa versione dell'SDK. Il nuovo codec audio presenta una qualità migliorata a velocità in bit inferiori.

## <a name="thumbnail-right"></a>Anteprima a destra

Le applicazioni possono richiedere una nuova azione DRM per leggere da video per creare un'immagine di anteprima. Ciò consente alle applicazioni di creare e visualizzare immagini di anteprima per file video senza aprire il file per la riproduzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni su Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




