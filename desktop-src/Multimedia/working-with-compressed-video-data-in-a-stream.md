---
title: Utilizzo di dati video compressi in un flusso
description: Utilizzo di dati video compressi in un flusso
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0587ee6c12a93eb014368642ba1605f546129e0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046638"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a>Utilizzo di dati video compressi in un flusso

AVIFile offre diversi modi per accedere ai flussi video compressi.

Se si desidera visualizzare uno o più frame di un flusso video compresso, è possibile recuperare i frame utilizzando la funzione [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) e inviando i dati del frame compresso alle funzioni DrawDib per visualizzarli. Le funzioni DrawDib possono visualizzare immagini di diverse profondità dell'immagine e dithering automatico delle immagini per le visualizzazioni che non possono gestire determinati tipi di bitmap indipendenti dal dispositivo. Queste funzioni funzionano con immagini non compresse e compresse. Per ulteriori informazioni sulle funzioni DrawDib, vedere [funzioni DrawDib](drawdib-functions.md).

AVIFile fornisce funzioni per la decompressione di un singolo fotogramma video. Per allocare le risorse, usare la funzione [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) . Questa funzione crea un buffer per i dati decompressi.

È possibile decomprimere un singolo fotogramma video usando la funzione [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) . Questa funzione decomprime il frame e recupera un frame completo di dati dell'immagine, restituendo l'indirizzo della DIB nella struttura [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) . L'applicazione può visualizzare la DIB usando le funzioni di disegno standard o le funzioni DrawDib.

Se l'applicazione effettua chiamate successive a **AVIStreamGetFrame**, la funzione sovrascrive il buffer con ogni frame recuperato.

Quando si termina l'uso di **AVIStreamGetFrame** e la DIB decompressa si trova nel buffer, è possibile rilasciare le risorse allocate usando la funzione [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) .

Per ulteriori informazioni sulla decompressione delle immagini, vedere [Gestione compressione video](video-compression-manager.md).

 

 