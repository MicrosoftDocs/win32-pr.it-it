---
description: L'oggetto DivisionUnit rappresenta un singolo elemento strutturale di un oggetto DivisionResult. Un oggetto DivisionUnit può rappresentare un disegno, un singolo segmento di riconoscimento della grafia, una riga della grafia o un blocco di scrittura manuale.
ms.assetid: 13f6121c-2b83-4788-9d06-460dc03094bf
title: Utilizzo dell'oggetto DivisionUnit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c2ce09bf2b67f5724bba523219d0555063c3f7215810d3b11c48596f979fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966510"
---
# <a name="working-with-the-divisionunit-object"></a>Utilizzo dell'oggetto DivisionUnit

**L'oggetto DivisionUnit** rappresenta un singolo elemento strutturale di un **oggetto DivisionResult.** Un **oggetto DivisionUnit** può rappresentare un disegno, un singolo segmento di riconoscimento della grafia, una riga della grafia o un blocco di scrittura manuale.

[**L'enumerazione InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) definisce i tipi di elementi strutturali che l'analisi del layout riconosce. In Automazione **l'oggetto DivisionUnit** è denominato [**IInkDivisionUnit.**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit)

La [**proprietà DivisionType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_divisiontype) dell'oggetto **DivisionUnit** restituisce il tipo di elemento strutturale **dell'oggetto DivisionUnit.** La [**proprietà RecognitionString**](/previous-versions/windows/desktop/legacy/ms703283(v=vs.85)) dell'oggetto **DivisionUnit** restituisce il testo di riconoscimento per gli elementi di scrittura manuale o **NULL per** gli elementi di disegno.

La [**proprietà Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) dell'oggetto **DivisionUnit** contiene il subset dei tratti nell'oggetto **DivisionResult** che corrispondono a questo elemento. Poiché esistono elementi di scrittura manuale per diversi livelli di dettaglio, le raccolte **Strokes** per elementi diversi possono sovrapporsi. In particolare, un segmento di riconoscimento condivide i tratti con la linea e il blocco di cui fa parte e una linea condivide i tratti con il blocco di cui fa parte.

La [**proprietà RotationTransform**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_rotationtransform) dell'oggetto **DivisionUnit** restituisce una matrice per la rotazione dei tratti dell'elemento in orizzontale. Per gli elementi di paragrafo e disegno, **la proprietà RotationTransform** restituisce la matrice di identità. Un sistema di riconoscimento del testo offre prestazioni molto migliori per la grafia allineata orizzontalmente rispetto alla grafia che non lo è. In Automazione viene chiamata **proprietà RotationTransform** e restituisce un oggetto [**InkTransform**](inktransform-class.md) che contiene la matrice di trasformazione. La **proprietà RotationTransform** restituisce **NULL per gli** elementi di paragrafo e di disegno.

Per altre informazioni **sull'oggetto DivisionResult,** vedere [Utilizzo dell'oggetto DivisionResult.](working-with-the-divisionresult-object.md)

 

 
