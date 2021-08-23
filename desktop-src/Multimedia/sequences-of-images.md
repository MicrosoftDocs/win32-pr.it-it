---
title: Sequenze di immagini
description: Sequenze di immagini
ms.assetid: fbfb944c-a927-4c92-b3d6-2f8c278408e6
keywords:
- DrawDib, sequenze di immagini
- DrawDib, sequenza di bitmap
- Funzione DrawDibDraw
- Funzione DrawDibBegin
- Funzione DrawDibEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac063cb2e9697b3b95045b95c9cc759a562197b56f10ff86a076ddcfa9a72cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688793"
---
# <a name="sequences-of-images"></a>Sequenze di immagini

È possibile visualizzare una sequenza di bitmap con le stesse dimensioni e formati usando la [**funzione DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) con la [**funzione DrawDibBegin.**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) **DrawDibBegin migliora** l'efficienza di **DrawDibDraw preparando** il controller di dominio DrawDib per il disegno.

> [!Note]  
> Se l'applicazione non usa [**DrawDibBegin,**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) la esegue in modo implicito prima del disegno. Se l'applicazione usa **DrawDibBegin** prima di **DrawDibDraw,** **DrawDibDraw** non deve elaborare la funzione e attendere il completamento.

 

La [**funzione DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) fornisce [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) con il controller di dominio DrawDib, l'handle del controller di dominio, l'indirizzo [**della struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) e le dimensioni del rettangolo di origine e di destinazione. Quando si visualizza una sequenza di bitmap, **DrawDibDraw** controlla i valori di questi elementi per ogni immagine nella sequenza. Se **DrawDibDraw rileva** modifiche a uno di questi elementi, chiama in modo implicito di nuovo **DrawDibBegin** per modificare le impostazioni del controller di dominio DrawDib.

Dopo aver [**utilizzato DrawDibBegin,**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)è possibile disegnare la sequenza di immagini [**usando DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) e specificando uno o più flag in base alle esigenze. Specificare il flag **DDF \_ SAME \_ HDC** purché l'handle del controller di dominio non sia stato modificato. Specificare il flag DDF SAME DRAW quando i parametri seguenti per \_ \_ **DrawDibDraw** non sono stati modificati: l'indirizzo della [**struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) e le dimensioni del rettangolo di origine e di destinazione.

È possibile aggiornare i flag impostati con [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) usando la [**funzione DrawDibEnd seguita**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) da un'altra chiamata a **DrawDibBegin.** Usare quindi **DrawDibEnd per** cancellare i flag e le impostazioni correnti del controller di dominio DrawDib. La chiamata successiva a **DrawDibBegin** reinizializza il controller di dominio DrawDib con i flag e le impostazioni appropriati. In alternativa, è possibile aggiornare i flag per un controller di dominio DrawDib usando **DrawDibBegin** senza **DrawDibEnd.** A tale scopo, è necessario modificare almeno una delle impostazioni seguenti contemporaneamente ai flag: l'indirizzo della [**struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) o le dimensioni del rettangolo di origine o di destinazione.

È possibile aumentare l'efficienza di [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) per le operazioni di streaming dei dati che usano immagini compresse, ad esempio la riproduzione di un clip video, usando le funzioni [**DrawDibStart**](/windows/desktop/api/Vfw/nf-vfw-drawdibstart) e [**DrawDibStop.**](/windows/desktop/api/Vfw/nf-vfw-drawdibstop) La **funzione DrawDibStart** prepara il controller di dominio DrawDib a ricevere un flusso di immagini inviando un messaggio al gestore della compressione video. Al termine del flusso, **DrawDibStop** invia un messaggio a VCM che indica che è possibile rilasciare le risorse allocate per l'operazione di streaming dei dati. Per altre informazioni su Gestione compressione video, vedere [Gestione compressione video.](video-compression-manager.md)

> [!Note]  
> È necessario specificare la larghezza e l'altezza dei rettangoli di origine e di destinazione nell'applicazione. Tuttavia, non è necessario specificare le origini dei rettangoli. L'applicazione può ridefinire le origini in [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) per usare parti diverse dell'immagine o per aggiornare parti diverse della visualizzazione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering delle immagini](image-rendering.md)
</dt> </dl>

 

 