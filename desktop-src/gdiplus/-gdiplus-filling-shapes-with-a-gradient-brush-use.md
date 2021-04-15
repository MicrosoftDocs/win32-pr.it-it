---
description: È possibile utilizzare un pennello sfumatura per riempire una forma con un colore a modifica graduale.
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: Riempimento di forme con un pennello sfumatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6784d0bfd59fd37f217e8d7a1cdd230348807d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994253"
---
# <a name="filling-shapes-with-a-gradient-brush"></a>Riempimento di forme con un pennello sfumatura

È possibile utilizzare un pennello sfumatura per riempire una forma con un colore a modifica graduale. È ad esempio possibile utilizzare una sfumatura orizzontale per riempire una forma con un colore che cambia gradualmente man mano che si passa dal bordo sinistro della forma al bordo destro. Immaginate un rettangolo con un bordo sinistro nero (rappresentato da componenti rosso, verde e blu 0, 0, 0) e un bordo destro rosso (rappresentato da 255, 0, 0). Se il rettangolo è 256 pixel di larghezza, il componente rosso di un determinato pixel sarà maggiore di uno rispetto al componente rosso del pixel alla sua sinistra. Il pixel più a sinistra in una riga ha componenti di colore (0, 0, 0), il secondo pixel ha (1, 0, 0), il terzo pixel ha (2, 0, 0) e così via, fino a quando non si arriva al pixel più a destra, che include componenti colore (255, 0, 0). Questi valori di colore interpolati costituiscono la sfumatura di colore.

Una sfumatura lineare cambia colore mentre si sposta orizzontalmente, verticalmente o in parallelo in una linea inclinata specificata. Una sfumatura di tracciato cambia colore mentre si sposta sull'interno e sul limite di un tracciato. È possibile personalizzare le sfumature del tracciato per ottenere una vasta gamma di effetti.

GDI+ fornisce le classi [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) e [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) , entrambe ereditate dalla classe [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

Negli argomenti seguenti vengono illustrate le sfumature lineari e di percorso in modo più dettagliato:

-   [Creazione di una sfumatura lineare](-gdiplus-creating-a-linear-gradient-use.md)
-   [Creazione di una sfumatura del percorso](-gdiplus-creating-a-path-gradient-use.md)
-   [Applicazione della correzione gamma a una sfumatura](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 



