---
description: Top-Down e
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down e DIB Bottom-Up
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff1d525423ef8590a3656a5e63f7541be180e2dcc5c70307f93298eb9ce991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951570"
---
# <a name="top-down-vs-bottom-up-dibs"></a>Top-Down e DIB Bottom-Up

Se non si ha esperienza con la programmazione grafica, si potrebbe prevedere che una bitmap venga disposta in memoria in modo che la riga superiore dell'immagine venga visualizzata all'inizio del buffer, seguita dalla riga successiva e così via. Tuttavia, questo non è necessariamente il caso. In Windows, le bitmap indipendenti dal dispositivo (DIB) possono essere inserite in memoria in due diversi orientamenti, dal basso verso l'alto e dall'alto verso il basso.

In un DIB dal basso verso l'alto, il buffer dell'immagine inizia con la riga inferiore di pixel, seguita dalla riga successiva verso l'alto e così via. La riga superiore dell'immagine è l'ultima riga nel buffer. Pertanto, il primo byte in memoria è il pixel inferiore sinistro dell'immagine. In GDI, tutti i dib sono dal basso verso l'alto. Il diagramma seguente illustra il layout fisico di un DIB dal basso verso l'alto.

![dib bottom-up](images/pixel-layout-bottomup.png)

In un DIB dall'alto verso il basso, l'ordine delle righe viene invertito. La riga superiore dell'immagine è la prima riga in memoria, seguita dalla riga successiva verso il basso. La riga inferiore dell'immagine è l'ultima riga nel buffer. Con un DIB dall'alto verso il basso, il primo byte in memoria è il pixel superiore sinistro dell'immagine. DirectDraw usa dib dall'alto verso il basso. Il diagramma seguente illustra il layout fisico di un DIB dall'alto verso il basso:

![dib dall'alto verso il basso](images/pixel-layout-topdown.png)

Per i DIB RGB, l'orientamento dell'immagine è indicato dal **membro biHeight** della [**struttura BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) Se **biHeight** è positivo, l'immagine è dal basso verso l'alto. Se **biHeight** è negativo, l'immagine è dall'alto verso il basso.

I dib nei formati YUV sono sempre dall'alto verso il basso e il segno del **membro biHeight** viene ignorato. I decodificatori devono offrire formati YUV con **valore biHeight** positivo, ma devono accettare anche formati YUV con **valore biHeight** negativo e ignorare il segno.

Inoltre, qualsiasi tipo DIB che usa **fourCC** nel membro **biCompression** deve esprimere il proprio **valore biHeight** come numero positivo indipendentemente dall'orientamento, poiché **fourCC** stesso identifica uno schema di compressione il cui orientamento dell'immagine deve essere riconosciuto da qualsiasi filtro compatibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei fotogrammi video](working-with-video-frames.md)
</dt> </dl>

 

 



