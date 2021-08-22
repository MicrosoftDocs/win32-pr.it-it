---
description: Rettangoli di origine e destinazione nei renderer video
ms.assetid: fdddbffb-c44f-4364-9e2e-b721ba39c74f
title: Rettangoli di origine e destinazione nei renderer video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020be0786a071c6bbdf33649405517ed3788789268052b61ee89d97a23f357f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072545"
---
# <a name="source-and-target-rectangles-in-video-renderers"></a>Rettangoli di origine e destinazione nei renderer video

Sono disponibili tre dimensioni nelle strutture di [**formato VIDEOINFO,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)e [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) dei tipi di supporti video. Questo articolo illustra cosa sono e come funzionano.

In primo luogo, è presente una dimensione nel **membro bmiHeader** di queste strutture. Il **membro bmiHeader** è una [**struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) con i propri membri width e height, **bmiHeader.biWidth** e **bmiHeader.biHeight.**

In secondo piano, è presente un rettangolo nel **membro rcSource** di queste strutture. e infine, è presente un rettangolo nel membro **rcTarget** di queste strutture.

Si supponga di avere due filtri, A e B, e che questi filtri siano connessi tra loro (A a sinistra o a monte e B a destra o a valle) con un determinato tipo di supporto video.

I buffer che passano tra i filtri A e B hanno le dimensioni (**bmiHeader.biWidth**, **bmiHeader.biHeight**). Il filtro A deve richiedere una parte del video di input determinato da **rcSource** ed estendere il video per riempire la parte **rcTarget** del buffer. La parte del video di input da usare si basa sul confronto tra **rcSource** e le dimensioni (**biWidth**, **biHeight**) del tipo di supporto che filtra A e B originariamente connessi. Se **rcSource è** vuoto, il filtro A usa l'intero video di input. Se **rcTarget è** vuoto, il filtro A riempie l'intero buffer di output.

Si supponga, ad esempio, che il filtro A riceva dati video di 160 x 120 pixel. Si supponga anche che il filtro A sia connesso per filtrare B con il tipo di supporto seguente.

-   (**biWidth**, **biHeight**): 320, 240
-   **rcSource:**(0, 0, 0, 0)
-   **rcTarget:**(0, 0, 0, 0)

Ciò significa che il filtro A estenderà il video ricevuto di 2 in entrambe le direzioni x e y e riempirà un buffer di output di 320 x 240.

Come altro esempio, si supponga che il filtro A riceva dati video 160 x 120 e che sia connesso per filtrare B con il tipo di supporto seguente.

-   (**biWidth**, **biHeight**): 320, 240
-   **rcSource**: (0, 0, 160, 240)
-   **rcTarget:**(0, 0, 0, 0)

Il **membro rcSource** è relativo alle dimensioni del buffer connesso di 320, 240. Poiché **l'oggetto rcSource** specificato (0, 0, 160, 240) è la metà sinistra del buffer, il filtro A prenderà la metà sinistra del video di input o la parte (0, 0, 80, 120) e estenderà il video fino a una dimensione di (320, 240) (per 4 nella direzione x e di 2 nella direzione y) e riempiendo il buffer di output 320 x 240.

Si supponga ora che il filtro A chiami [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md)e che all'esempio multimediale restituito sia associato un tipo di supporto, a significare che il filtro B vuole che il filtro A fornisse una dimensione o un tipo di video diverso da quello fornito in precedenza. Si supponga che il nuovo tipo di supporto sia:

-   (**biWidth**, **biHeight**): 640, 480
-   **rcSource**: (0, 0, 160, 120)
-   **rcTarget:**(0, 0, 80, 60)

Ciò significa che l'esempio di supporti ha dimensioni di buffer di 640 x 480. Il membro **rcSource** è relativo al tipo di supporto connesso originale (320, 240) e non al nuovo tipo di supporto (640, 480), quindi **rcSource** specifica che deve essere usato l'angolo superiore sinistro (25%) del video di input. Questa parte del video di input viene posizionata in alto a sinistra (80, 60) pixel del buffer di output 640 x 480, come specificato da **rcTarget** di (0, 0, 80, 60). Poiché il filtro A riceve un video di 160 x 120, l'angolo superiore sinistro del video di input è un elemento (80, 60), le stesse dimensioni della bitmap di output e non è richiesto alcun stretching.

Il filtro A non inserirà dati negli altri pixel del buffer di output e i bit non verranno toccati. Il membro **rcSource** è delimitato dai valori **biWidth** e **biHeight** del tipo di supporto connesso originale tra i filtri A e B e **rcTarget** è delimitato dai nuovi **valori biWidth** e **biHeight** dell'esempio multimediale. Nell'esempio **precedente, rcSource** non poteva uscire dai limiti di (0, 0, 320, 240) e **rcTarget** non poteva uscire dai limiti di (0, 0, 640, 480).

 

 



