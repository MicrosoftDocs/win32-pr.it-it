---
description: Confronto tra Top-Down e
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down rispetto a Bottom-Up
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e719bea5923aeccc4a0a92b5f73a253e13d2e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313414"
---
# <a name="top-down-vs-bottom-up-dibs"></a>Top-Down rispetto a Bottom-Up

Se non si ha familiarità con la programmazione grafica, è possibile che una bitmap venga disposta nella memoria in modo che la riga superiore dell'immagine venga visualizzata all'inizio del buffer, seguita dalla riga successiva e così via. Tuttavia, questo non è necessariamente il caso. In Windows, le bitmap indipendenti dal dispositivo (DIB) possono essere posizionate in memoria in due diversi orientamenti, dal basso verso l'alto e dall'alto verso il basso.

In una DIB dal basso in alto, il buffer dell'immagine inizia con la riga inferiore di pixel, seguita dalla riga successiva e così via. La riga superiore dell'immagine è l'ultima riga nel buffer. Il primo byte in memoria è pertanto il pixel inferiore sinistro dell'immagine. In GDI tutte le mie priorità sono dal basso verso l'alto. Il diagramma seguente illustra il layout fisico di una DIB dal basso in alto.

![parte superiore della DIB](images/pixel-layout-bottomup.png)

In una DIB dall'alto verso il basso l'ordine delle righe viene invertito. La riga superiore dell'immagine è la prima riga in memoria, seguita dalla riga successiva. La riga inferiore dell'immagine è l'ultima riga nel buffer. Con una DIB dall'alto in basso, il primo byte in memoria è il pixel superiore sinistro dell'immagine. DirectDraw utilizza l'alto verso il basso. Il diagramma seguente illustra il layout fisico di una DIB dall'alto verso il basso:

![DIB dall'alto in basso](images/pixel-layout-topdown.png)

Per la priorità RGB, l'orientamento dell'immagine è indicato dal membro **biHeight** della struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) . Se **biHeight** è un valore positivo, l'immagine è dal basso verso l'alto. Se **biHeight** è negativo, l'immagine è dall'alto verso il basso.

Le priorità nei formati YUV sono sempre dall'alto verso il basso e il segno del membro **biHeight** viene ignorato. I decodificatori devono offrire formati YUV con una **bialtezza** positiva, ma devono accettare anche formati YUV con una **bialtezza** negativa e ignorare il segno.

Inoltre, qualsiasi tipo di DIB che usa un **fourcc** nel membro di **bicompressione** deve esprimere la propria **bialtezza** come numero positivo, indipendentemente dall'orientamento, poiché il **fourcc** stesso identifica uno schema di compressione il cui orientamento dell'immagine deve essere compreso da qualsiasi filtro compatibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di fotogrammi video](working-with-video-frames.md)
</dt> </dl>

 

 



