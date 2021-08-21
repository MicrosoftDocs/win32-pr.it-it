---
description: Analogamente a un'area di ritaglio, un tracciato di ritaglio è un altro oggetto grafico che un'applicazione può selezionare in un contesto di dispositivo.
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: Percorsi di ritaglio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91e77e3867951d09f464393fde6b416b9319f9ab914bcc393448d2b01a1eb24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038149"
---
# <a name="clip-paths"></a>Percorsi di ritaglio

Analogamente a un'area di ritaglio, un tracciato di ritaglio è un altro oggetto grafico che un'applicazione può selezionare in un contesto di dispositivo. A differenza di un'area di ritaglio, un tracciato di ritaglio viene sempre creato da un'applicazione e viene usato per ritagliare una o più forme irregolari. Ad esempio, un'applicazione può usare le linee e le curve che formano i contorni dei caratteri in una stringa di testo per definire un percorso di ritaglio.

Per creare un tracciato di ritaglio, è prima necessario creare un tracciato che descriva la forma irregolare richiesta. I percorsi vengono creati chiamando le funzioni di disegno GDI (Graphics Device Interface) appropriate dopo aver chiamato la [**funzione BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) e prima di chiamare la [**funzione EndPath.**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) Questa raccolta di funzioni è denominata parentesi di percorso. Per altre informazioni sui percorsi e le parentesi quadre, vedere [Percorsi](paths.md).

Dopo la creazione, il percorso può essere convertito in un percorso di clip chiamando la [**funzione SelectClipPath,**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) identificando un contesto di dispositivo e specificando una modalità di utilizzo. La modalità di utilizzo determina il modo in cui il sistema combina il nuovo percorso di ritaglio con l'area di ritaglio originale del contesto di dispositivo. Nella tabella seguente vengono descritte le modalità di utilizzo.



| Mode      | Descrizione                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| RGN \_ E  | Il percorso di ritaglio include l'intersezione (aree sovrapposte) dell'area di ritaglio del contesto di dispositivo e del percorso corrente.    |
| COPIA \_ RGN | Il percorso del clip è il percorso corrente.                                                                                           |
| RGN \_ DIFF | Il percorso di ritaglio include l'area di ritaglio del contesto di dispositivo con eventuali parti intersecanti del percorso corrente escluse.        |
| RGN \_ OR   | Il percorso di ritaglio include l'unione (aree combinate) dell'area di ritaglio del contesto di dispositivo e del percorso corrente.              |
| RGN \_ XOR  | Il percorso di ritaglio include l'unione dell'area di ritaglio del contesto di dispositivo e del percorso corrente, ma esclude l'intersezione. |



 

 

 



