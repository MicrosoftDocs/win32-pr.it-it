---
description: L'oggetto divisore utilizza un oggetto RecognizerContext per migliorare l'analisi dei segmenti di riconoscimento e generare testo di riconoscimento per gli elementi di grafia.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Utilizzo di un contesto di riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdea8c59bc894a6962e8bbe7e58f316327a548e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049565"
---
# <a name="working-with-a-recognizer-context"></a>Utilizzo di un contesto di riconoscimento

L'oggetto [**divisore**](inkdivider-class.md) utilizza un oggetto [**RecognizerContext**](inkrecognizercontext-class.md) per migliorare l'analisi dei segmenti di riconoscimento e generare testo di riconoscimento per gli elementi di grafia.

È possibile impostare il contesto di riconoscimento usando la proprietà [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) dell'oggetto [**divisore**](inkdivider-class.md) o specificando il contesto di riconoscimento nella chiamata al costruttore del [divisore](/previous-versions/ms839465(v=msdn.10)) (nel codice gestito). Se un contesto di riconoscimento per un riconoscimento non grafia o per un riconoscimento che non supporta la funzionalità di input libero viene assegnato alla proprietà **RecognizerContext** , viene generata un'eccezione.

Se i riconoscitori non sono installati o un contesto di riconoscimento non è assegnato all'oggetto [**divisore**](inkdivider-class.md) , l'oggetto **divisore** non utilizza un contesto di riconoscimento. In questo caso, la funzionalità di analisi del layout esegue la divisione del segmento e nessun testo è associato all'oggetto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .

> [!Note]  
> Non è possibile modificare la proprietà [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) dopo che sono stati assegnati Strokes all'oggetto [**divisore**](inkdivider-class.md) . L'oggetto **divisore** utilizza i valori predefiniti delle proprietà dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) .

 

L'oggetto [**divisore**](inkdivider-class.md) applica il contesto del riconoscimento agli elementi scritti a mano durante l'analisi del layout. Tutti i tratti assegnati direttamente al contesto del riconoscimento vengono ignorati dall'oggetto **divisore** . Per ulteriori informazioni sul riconoscimento del testo, vedere [informazioni sul riconoscimento della grafia](about-handwriting-recognition.md).

 

 
