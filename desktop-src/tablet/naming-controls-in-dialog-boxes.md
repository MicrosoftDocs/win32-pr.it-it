---
description: Quando si utilizzano le finestre di dialogo di Microsoft Windows, è necessario etichettare tutti i controlli per facilitare la funzionalità di riconoscimento vocale. Nella finestra di dialogo Esegui seguente viene visualizzata un'etichetta di controllo testo statico per una casella di riepilogo a discesa. Il testo statico termina con i due punti.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Denominazione dei controlli nelle finestre di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f74ecb3737b422450388ee87ab4177e899aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554083"
---
# <a name="naming-controls-in-dialog-boxes"></a>Denominazione dei controlli nelle finestre di dialogo

Quando si utilizzano le finestre di dialogo di Microsoft Windows, è necessario etichettare tutti i controlli per facilitare la funzionalità di riconoscimento vocale. Nella finestra di dialogo **Esegui** seguente viene visualizzata un'etichetta di controllo testo statico per una casella di riepilogo a discesa. Il testo statico termina con i due punti.

![screenshot che mostra la finestra di dialogo Esegui](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

Sono disponibili due tipi di controlli:

-   Controlli con didascalie come proprietà del controllo, ad esempio pulsanti di comando e caselle di controllo. Gli strumenti di accessibilità non hanno problemi nell'identificazione di questi controlli purché la didascalia sia definita correttamente.
-   I controlli che non hanno didascalie proprie, ad esempio i controlli di modifica, le caselle di riepilogo e le visualizzazioni elenco, devono essere contrassegnati con controlli di testo statici distinti. Per ulteriori informazioni sui controlli che non dispongono di didascalie, vedere [controlli senza proprietà didascalia](controls-without-caption-properties.md).

È possibile utilizzare diverse tecniche per superare le situazioni in cui i controlli non hanno didascalie proprie, ma sono efficaci solo per le finestre visualizzate da Gestione finestre di dialogo standard (SDM). Tutte le altre finestre devono esporre i nomi e la relazione tra i controlli, supportando in modo esplicito Microsoft Active Accessibility. Per ulteriori informazioni su Active Accessibility, vedere la sezione relativa all' [accessibilità](/windows/desktop/accessibility) in MSDN Library.

 

 
