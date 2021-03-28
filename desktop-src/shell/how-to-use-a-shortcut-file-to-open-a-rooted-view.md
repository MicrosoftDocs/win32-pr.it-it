---
description: È possibile avviare una visualizzazione radice di un punto di giunzione tramite un file di collegamento a tale punto di giunzione.
title: Come aprire una visualizzazione radice di un punto di giunzione tramite un file di collegamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb83a6628b0dcffdf7d3bad66a25fc671c1feea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227430"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a>Come aprire una visualizzazione radice di un punto di giunzione tramite un file di collegamento

È possibile avviare una visualizzazione radice di un punto di giunzione tramite un [file di collegamento](./links.md) a tale punto di giunzione.

## <a name="instructions"></a>Istruzioni


Impostare la riga di destinazione del file di collegamento su Explorer.exe con un flag/root. Il formato esatto del comando dipende dalla posizione del punto di giunzione:

-   Se il punto di giunzione è una sottocartella del desktop, usare:

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   Se il punto di giunzione è una cartella file system, usare:

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   Se il punto di giunzione è una sottocartella di una cartella virtuale di sistema, usare:

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    Le cartelle virtuali di sistema che possono contenere punti di giunzione hanno gli identificatori di classe seguenti (CLSID):

    

    |                   |                                        |
    |-------------------|----------------------------------------|
    | Risorse del computer       | {20D04FE0-3AEA-1069-A2D8-08002B30309D} |
    | Risorse di rete | {208D2C60-3AEA-1069-A2D7-08002B30309D} |
    | Control panel     | {21EC2020-3AEA-1069-A2DD-08002B30309D} |
    | Internet Explorer | 871C5380-42A0-1069-A2EA-08002B30309D |

    

     

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della posizione di un'estensione dello spazio dei nomi](nse-junction.md)
</dt> <dt>

[Come aprire una visualizzazione radice di un punto di giunzione tramite il registro di sistema](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
