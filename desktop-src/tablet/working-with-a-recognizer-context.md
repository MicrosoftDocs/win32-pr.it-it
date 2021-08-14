---
description: L'oggetto Divider usa recognizerContext per migliorare l'analisi dei segmenti di riconoscimento e per generare il testo di riconoscimento per gli elementi di scrittura manuale.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Uso di un contesto di riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d99020e97170f0b68b1459abdc4b85f81ebc3fbba426233c2c13b5e042f28ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715099"
---
# <a name="working-with-a-recognizer-context"></a>Uso di un contesto di riconoscimento

[**L'oggetto Divider**](inkdivider-class.md) usa [**recognizerContext per**](inkrecognizercontext-class.md) migliorare l'analisi dei segmenti di riconoscimento e per generare il testo di riconoscimento per gli elementi di scrittura manuale.

È possibile impostare il contesto del riconoscitore usando la proprietà [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) dell'oggetto [**Divider**](inkdivider-class.md) o fornendo il contesto di riconoscimento nella chiamata al costruttore [Divider](/previous-versions/ms839465(v=msdn.10)) (nel codice gestito). Se alla proprietà **RecognizerContext** viene assegnato un contesto di riconoscimento per un sistema di riconoscimento della grafia o per un sistema di riconoscimento che non supporta la funzionalità di input libero, viene generata un'eccezione.

Se i riconoscitori non sono installati o non è assegnato un contesto di riconoscimento all'oggetto [**Divider,**](inkdivider-class.md) l'oggetto **Divider** non usa un contesto di riconoscimento. In questo caso, la funzionalità di analisi del layout esegue la divisione dei segmenti e [**all'oggetto DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) non è associato alcun testo.

> [!Note]  
> La [**proprietà RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) non può essere modificata dopo che i tratti sono stati assegnati all'oggetto [**Divider.**](inkdivider-class.md) **L'oggetto Divider** usa i valori di proprietà predefiniti [**dell'oggetto RecognizerContext.**](inkrecognizercontext-class.md)

 

[**L'oggetto Divider**](inkdivider-class.md) applica il contesto di riconoscimento agli elementi scritti a mano durante l'analisi del layout. Tutti i tratti assegnati direttamente al contesto del riconoscitore vengono ignorati **dall'oggetto Divider.** Per altre informazioni sul riconoscimento del testo, vedere [Informazioni sul riconoscimento della grafia.](about-handwriting-recognition.md)

 

 
