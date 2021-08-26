---
description: È possibile usare un pennello sfumato per riempire una forma con un colore che cambia gradualmente.
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: Riempimento di forme con un pennello sfumato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d471e9d3e2d7fb6d151d50ab3b5f10212874180b4554769b5c00a552085391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015051"
---
# <a name="filling-shapes-with-a-gradient-brush"></a>Riempimento di forme con un pennello sfumato

È possibile usare un pennello sfumato per riempire una forma con un colore che cambia gradualmente. Ad esempio, è possibile usare una sfumatura orizzontale per riempire una forma con un colore che cambia gradualmente quando si passa dal bordo sinistro della forma al bordo destro. Imagine un rettangolo con un bordo sinistro nero (rappresentato da componenti rosso, verde e blu 0, 0, 0) e un bordo destro rosso (rappresentato da 255, 0, 0). Se il rettangolo ha una larghezza di 256 pixel, il componente rosso di un determinato pixel sarà maggiore di uno rispetto al componente rosso del pixel a sinistra. Il pixel più a sinistra in una riga ha componenti di colore (0, 0, 0), il secondo pixel ha (1, 0, 0), il terzo pixel ha (2, 0, 0) e così via, fino a raggiungere il pixel più a destra, che include componenti di colore (255, 0, 0). Questi valori di colore interpolati costituiscono la sfumatura di colore.

Una sfumatura lineare cambia colore quando ci si sposta orizzontalmente, verticalmente o parallelamente a una linea sgradata specificata. Una sfumatura di percorso cambia colore quando ci si sposta all'interno e al limite di un tracciato. È possibile personalizzare le sfumature del tracciato per ottenere un'ampia gamma di effetti.

GDI+ fornisce le [**classi LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) e [**PathGradientBrush,**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) che ereditano entrambe dalla [**classe Brush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)

Gli argomenti seguenti descrivono in modo più dettagliato le sfumature lineari e di percorso:

-   [Creazione di una sfumatura lineare](-gdiplus-creating-a-linear-gradient-use.md)
-   [Creazione di una sfumatura di percorso](-gdiplus-creating-a-path-gradient-use.md)
-   [Applicazione della correzione gamma a una sfumatura](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 



