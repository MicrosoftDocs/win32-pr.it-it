---
title: Sequenze di immagini
description: Sequenze di immagini
ms.assetid: fbfb944c-a927-4c92-b3d6-2f8c278408e6
keywords:
- DrawDib, sequenze di immagini
- DrawDib, sequenza di bitmap
- DrawDibDraw (funzione)
- DrawDibBegin (funzione)
- DrawDibEnd (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7ae2c85d62e93e4149518221aa520eabe13ee2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299709"
---
# <a name="sequences-of-images"></a>Sequenze di immagini

È possibile visualizzare una sequenza di bitmap con le stesse dimensioni e formati usando la funzione [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) con la funzione [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) . **DrawDibBegin** migliora l'efficienza di **DrawDibDraw** preparando il controller di dominio DrawDib per il disegno.

> [!Note]  
> Se l'applicazione non usa [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin), [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) la esegue in modo implicito prima di disegnare. Se l'applicazione usa **DrawDibBegin** prima di **DrawDibDraw**, **DrawDibDraw** non deve elaborare la funzione e attenderne il completamento.

 

La funzione [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) fornisce [**DRAWDIBDRAW**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) con il controller di dominio DrawDib, l'handle del controller di dominio, l'indirizzo della struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) e le dimensioni del rettangolo di origine e di destinazione. Quando si visualizza una sequenza di bitmap, **DrawDibDraw** controlla i valori di questi elementi per ogni immagine nella sequenza. Se **DrawDibDraw** rileva le modifiche apportate a uno di questi elementi, chiama in modo implicito **DrawDibBegin** per modificare le impostazioni del controller di dominio DrawDib.

Dopo aver usato [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin), è possibile creare la sequenza di immagini usando [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) e specificando uno o più flag appropriati. Specificare lo **\_ stesso flag \_ HDC DDF** a condizione che l'handle del controller di dominio non sia stato modificato. Specificare lo \_ stesso \_ flag di traccia DDF quando i parametri seguenti per **DrawDibDraw** non sono stati modificati: l'indirizzo della struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) e le dimensioni del rettangolo di origine e di destinazione.

È possibile aggiornare i flag impostati con [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) usando la funzione [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) seguita da un'altra chiamata a **DrawDibBegin**. Usare quindi **DrawDibEnd** per cancellare il controller di dominio DrawDib dei flag e delle impostazioni correnti. La chiamata successiva a **DrawDibBegin** REINIZIALIZZA il controller di dominio DrawDib con i flag e le impostazioni appropriati. In alternativa, è possibile aggiornare i flag per un controller di dominio DrawDib usando **DrawDibBegin** senza **DrawDibEnd**. A tale scopo, è necessario modificare almeno una delle impostazioni seguenti simultaneamente ai flag, ovvero l'indirizzo della struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) o le dimensioni del rettangolo di origine o di destinazione.

È possibile aumentare l'efficienza di [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) per le operazioni di streaming dei dati che usano immagini compresse, ad esempio la riproduzione di un clip video, usando le funzioni [**DrawDibStart**](/windows/desktop/api/Vfw/nf-vfw-drawdibstart) e [**DrawDibStop**](/windows/desktop/api/Vfw/nf-vfw-drawdibstop) . La funzione **DrawDibStart** prepara il controller di dominio DrawDib per la ricezione di un flusso di immagini tramite l'invio di un messaggio a video Compression Manager (VCM). Quando il flusso è terminato, **DrawDibStop** Invia un messaggio a VCM indicante che è possibile rilasciare le risorse allocate per l'operazione di flusso dei dati. Per ulteriori informazioni su VCM, vedere [Gestione compressione video](video-compression-manager.md).

> [!Note]  
> È necessario specificare la larghezza e l'altezza dei rettangoli di origine e di destinazione nell'applicazione. Tuttavia, non è necessario specificare le origini dei rettangoli. L'applicazione può ridefinire le origini in [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) per usare parti diverse dell'immagine o per aggiornare parti diverse della visualizzazione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di immagini](image-rendering.md)
</dt> </dl>

 

 