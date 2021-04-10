---
description: L'oggetto DivisionUnit rappresenta un singolo elemento strutturale di un oggetto DivisionResult. Un oggetto DivisionUnit può rappresentare un disegno, un singolo segmento di riconoscimento della grafia, una riga di grafia o un blocco di grafia.
ms.assetid: 13f6121c-2b83-4788-9d06-460dc03094bf
title: Utilizzo dell'oggetto DivisionUnit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade8b617ae8e64c2641ef53a628a44e72e4fc35f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879126"
---
# <a name="working-with-the-divisionunit-object"></a>Utilizzo dell'oggetto DivisionUnit

L'oggetto **DivisionUnit** rappresenta un singolo elemento strutturale di un oggetto **DivisionResult** . Un oggetto **DivisionUnit** può rappresentare un disegno, un singolo segmento di riconoscimento della grafia, una riga di grafia o un blocco di grafia.

L'enumerazione [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) definisce i tipi di elementi strutturali riconosciuti dall'analisi del layout. In automazione, l'oggetto **DivisionUnit** è denominato [**IInkDivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit).

La proprietà [**DivisionType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_divisiontype) dell'oggetto **DivisionUnit** restituisce il tipo di elemento strutturale che rappresenta l'oggetto **DivisionUnit** . La proprietà [**RecognitionString**](/previous-versions/windows/desktop/legacy/ms703283(v=vs.85)) dell'oggetto **DivisionUnit** restituisce il testo di riconoscimento per gli elementi di grafia o **null** per gli elementi di disegno.

La proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) dell'oggetto **DivisionUnit** contiene il subset dei tratti nell'oggetto **DivisionResult** che corrispondono a questo elemento. Poiché esistono elementi di grafia per diversi livelli di dettaglio, le raccolte **Strokes** per diversi elementi possono sovrapporsi. In particolare, un segmento di riconoscimento condivide i tratti con la riga e il blocco di cui fa parte e una linea condivide i tratti con il blocco di cui fa parte.

La proprietà [**RotationTransform**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_rotationtransform) dell'oggetto **DivisionUnit** restituisce una matrice per la rotazione orizzontale dei tratti dell'elemento. Per gli elementi Paragraph e Drawing la proprietà **RotationTransform** restituisce la matrice di identità. Un riconoscimento del testo è molto migliore sulla grafia che è allineata orizzontalmente rispetto a quella eseguita sulla grafia che non lo è. In automazione, questo metodo è denominato proprietà **RotationTransform** e restituisce un oggetto [**InkTransform**](inktransform-class.md) che contiene la matrice di trasformazione. La proprietà **RotationTransform** restituisce **null** per gli elementi Paragraph e Drawing.

Per ulteriori informazioni sull'oggetto **DivisionResult** , vedere [utilizzo dell'oggetto DivisionResult](working-with-the-divisionresult-object.md).

 

 
