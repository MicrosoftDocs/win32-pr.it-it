---
description: Analogamente a un'area di ridimensionamento, un percorso di ritaglio è un altro oggetto grafico che un'applicazione può selezionare in un contesto di dispositivo.
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: Percorsi di ritaglio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4a93b0047110a6adb2f68d413e89cb1e97fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978770"
---
# <a name="clip-paths"></a>Percorsi di ritaglio

Analogamente a un'area di ridimensionamento, un percorso di ritaglio è un altro oggetto grafico che un'applicazione può selezionare in un contesto di dispositivo. A differenza di un'area di ridimensionamento, un tracciato di ritaglio viene sempre creato da un'applicazione e viene usato per il ritaglio a una o più forme irregolari. Ad esempio, un'applicazione può usare le linee e le curve che formano i contorni dei caratteri di una stringa di testo per definire un percorso di ritaglio.

Per creare un tracciato di ritaglio, è prima necessario creare un percorso che descriva la forma irregolare richiesta. I percorsi vengono creati chiamando le funzioni di disegno GDI (Graphics Device Interface) appropriate dopo aver chiamato la funzione [**beginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) e prima di chiamare la funzione [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) . Questa raccolta di funzioni è detta parentesi del percorso. Per ulteriori informazioni sui percorsi e sulle parentesi quadre, vedere [percorsi](paths.md).

Una volta creato il percorso, è possibile convertirlo in un percorso di clip chiamando la funzione [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) , identificando un contesto di dispositivo e specificando una modalità di utilizzo. La modalità di utilizzo determina il modo in cui il sistema combina il nuovo tracciato di ritaglio con l'area di ritaglio originale del contesto di dispositivo. Nella tabella seguente vengono descritte le modalità di utilizzo di.



| Mode      | Descrizione                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| RGN \_ e  | Il percorso di ritaglio include l'intersezione (aree sovrapposte) dell'area di ridimensionamento del contesto di dispositivo e il percorso corrente.    |
| copia di RGN \_ | Il percorso di ritaglio è il percorso corrente.                                                                                           |
| \_diff RGN | Il percorso della clip include l'area di ridimensionamento del contesto di dispositivo con le parti di intersezione del percorso corrente escluse.        |
| RGN \_ o   | Il percorso di ritaglio include l'Unione (aree combinate) dell'area di ridimensionamento del contesto di dispositivo e il percorso corrente.              |
| \_Xor RGN  | Il percorso della clip include l'Unione dell'area di ridimensionamento del contesto di dispositivo e il percorso corrente, ma esclude l'intersezione. |



 

 

 



