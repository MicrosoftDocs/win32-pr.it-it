---
title: Uso di dati video compressi in un flusso
description: Uso di dati video compressi in un flusso
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7c09de239fa28f3d9739dafc953ce10c2a6f1d69c0c607aeb03bc388a0f3003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622091"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a>Uso di dati video compressi in un flusso

AVIFile offre diversi modi per accedere ai flussi video compressi.

Se si desidera visualizzare uno o più fotogrammi di un flusso video compresso, è possibile recuperare i fotogrammi usando la [**funzione AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) e inoltrando i dati dei fotogrammi compressi alle funzioni DrawDib per visualizzarli. Le funzioni DrawDib possono visualizzare immagini con diverse profondità delle immagini ed eseguire automaticamente il dithering delle immagini per gli schermi che non possono gestire determinati tipi di bitmap indipendenti dal dispositivo (DIB). Queste funzioni funzionano con immagini non compresse e compresse. Per altre informazioni sulle funzioni DrawDib, vedere [Funzioni DrawDib.](drawdib-functions.md)

AVIFile fornisce funzioni per la decompressione di un singolo fotogramma video. Per allocare risorse, usare [**la funzione AVIStreamGetFrameOpen.**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) Questa funzione crea un buffer per i dati decompressi.

È possibile decomprimere un singolo fotogramma video usando la [**funzione AVIStreamGetFrame.**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) Questa funzione decomprime il frame e recupera un frame completo di dati immagine, che restituisce l'indirizzo del DIB nella [struttura BITMAPINFOHEADER.](/previous-versions//ms532290(v=vs.85)) L'applicazione può visualizzare il DIB usando le funzioni di disegno standard o le funzioni DrawDib.

Se l'applicazione effettua chiamate successive **ad AVIStreamGetFrame,** la funzione sovrascrive il buffer con ogni frame recuperato.

Dopo aver terminato di **usare AVIStreamGetFrame** e il DIB decompresso si trova nel buffer, è possibile rilasciare le risorse allocate usando la [**funzione AVIStreamGetFrameClose.**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose)

Per altre informazioni sulla decompressione delle immagini, vedere [Gestione compressione video.](video-compression-manager.md)

 

 