---
description: Quando si usano finestre di Windows microsoft, è necessario etichettare tutti i controlli per facilitare la funzionalità voce. La finestra di dialogo Esegui seguente mostra un'etichetta di controllo testo statico per una casella di riepilogo a discesa. Il testo statico termina con i due punti.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Denominazione dei controlli nelle finestre di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c33720c08a7f5454b54d7d982b14c091fe6e1df4c18a49cd649f54690f2eb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449829"
---
# <a name="naming-controls-in-dialog-boxes"></a>Denominazione dei controlli nelle finestre di dialogo

Quando si usano finestre di Windows microsoft, è necessario etichettare tutti i controlli per facilitare la funzionalità voce. La finestra **di dialogo** Esegui seguente mostra un'etichetta di controllo testo statico per una casella di riepilogo a discesa. Il testo statico termina con i due punti.

![Screenshot che mostra la finestra di dialogo Esegui](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

Sono disponibili due tipi di controlli:

-   Controlli con didascalie come proprietà del controllo, ad esempio pulsanti di comando e caselle di controllo. Gli strumenti per l'accessibilità non hanno problemi a identificare questi controlli, purché la didascalia sia definita correttamente.
-   I controlli che non dispongono di didascalie personalizzate, ad esempio controlli di modifica, caselle di riepilogo e visualizzazioni elenco, devono essere etichettati usando controlli di testo statici separati. Per altre informazioni sui controlli che non dispongono di didascalie personalizzate, vedere [Controlli senza proprietà didascalia](controls-without-caption-properties.md).

È possibile usare diverse tecniche per superare situazioni in cui i controlli non hanno didascalie proprie, ma sono efficaci solo per le finestre visualizzate da SDM (Standard Dialog Manager). Tutte le altre finestre devono esporre i nomi e la relazione tra i controlli supportando in modo esplicito Microsoft Active Accessibility. Per altre informazioni sui Active Accessibility, vedere la sezione [Accessibilità](/windows/desktop/accessibility) di MSDN Library.

 

 
