---
description: Rettangoli di origine e di destinazione nei renderer video
ms.assetid: fdddbffb-c44f-4364-9e2e-b721ba39c74f
title: Rettangoli di origine e di destinazione nei renderer video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556aea6aad22e5ea6df61c74ed0a46d2e3984d67
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521873"
---
# <a name="source-and-target-rectangles-in-video-renderers"></a>Rettangoli di origine e di destinazione nei renderer video

Nelle strutture di formato [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)e [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) dei tipi di supporti video sono disponibili tre dimensioni. Questo articolo spiega cosa sono e come funzionano.

In primo luogo, esiste una dimensione nel membro **bmiHeader** di queste strutture. Il membro **bmiHeader** è una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) con i relativi membri Width e Height, **BmiHeader. biWidth** e **bmiHeader. biHeight**.

In secondo luogo, esiste un rettangolo nel membro **rcSource** di queste strutture. Infine, esiste un rettangolo nel membro **rcTarget** di queste strutture.

Si supponga di disporre di due filtri, A e B, e che questi filtri siano collegati tra loro (A a sinistra, A Monte e B a destra o a valle) con un determinato tipo di supporti video.

I buffer che passano tra i filtri A e B hanno le dimensioni (**bmiHeader. biWidth**, **BmiHeader. biHeight**). Filter A deve prendere parte del video di input determinato da **rcSource** ed estendere il video in modo da riempire la parte **rcTarget** del buffer. La parte del video di input da usare è basata sulla modalità di confronto tra **rcSource** e la dimensione (**biWidth**, **biHeight**) del tipo di supporto che filtra a e B originariamente connessi con. Se **rcSource** è vuoto, il filtro A utilizza l'intero video di input. Se **rcTarget** è vuoto, il filtro A riempie l'intero buffer di output.

Si supponga, ad esempio, che il filtro A riceva dati video di 160 x 120 pixel. Si supponga inoltre che il filtro A sia connesso al filtro B con il seguente tipo di supporto.

-   (**biWidth**, **biHeight**): 320, 240
-   **rcSource**: (0, 0, 0, 0)
-   **rcTarget**: (0, 0, 0, 0)

Questo significa che il filtro A estenderà il video ricevuto da 2 nelle direzioni x e y e riempirà un buffer di output 320 x 240.

Per un altro esempio, si supponga che il filtro A riceva dati video di 160 x 120 e che sia connesso al filtro B con il seguente tipo di supporto.

-   (**biWidth**, **biHeight**): 320, 240
-   **rcSource**: (0, 0, 160, 240)
-   **rcTarget**: (0, 0, 0, 0)

Il membro **rcSource** è relativo alle dimensioni del buffer connesso 320, 240. Poiché il **rcSource** specificato (0, 0, 160, 240) è la metà sinistra del buffer, il filtro a accetta la metà sinistra del video di input o la parte (0, 0, 80, 120) ed estende il video alla dimensione (320, 240) (per 4 nella direzione x e 2 nella direzione y) e riempie il buffer di output 320 x 240.

Si supponga ora che Filter A chiami [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md)e che l'esempio multimediale restituito disponga di un tipo di supporto collegato, a indicare che Filter B desidera che il filtro a fornisca una dimensione o un tipo di video diverso da quello fornito in precedenza. Si supponga che il nuovo tipo di supporto sia:

-   (**biWidth**, **biHeight**): 640, 480
-   **rcSource**: (0, 0, 160, 120)
-   **rcTarget**: (0, 0, 80, 60)

Questo significa che l'esempio di supporto ha un buffer con dimensioni pari a 640 x 480. Il membro **rcSource** è relativo al tipo di supporto originale connesso (320, 240) non al nuovo tipo di supporto di (640, 480), quindi **rcSource** specifica che l'angolo superiore sinistro (25%) del video di input da usare. Questa parte del video di input viene posizionata in alto a sinistra (80, 60) pixel del buffer di output 640 x 480, come specificato da **rcTarget** di (0, 0, 80, 60). Poiché il filtro A sta ricevendo 160 x 120 video, l'angolo superiore sinistro del video di input è un elemento (80, 60), le stesse dimensioni della bitmap di output e non è necessaria alcuna estensione.

Il filtro A non inserisce dati negli altri pixel del buffer di output e li lascia invariati. Il membro **rcSource** è limitato dalla **bilarghezza** e dalla **bialtezza** del tipo di supporto originale connesso tra i filtri A e B e **RcTarget** è vincolato dalla nuova **bilarghezza** e dall' **altezza** dell'esempio multimediale. Nell'esempio precedente, **rcSource** non può superare i limiti di (0, 0, 320, 240) e **rcTarget** non possono superare i limiti di (0, 0, 640, 480).

 

 



