---
title: Valori restituiti hit test
description: Questa sezione elenca i valori del codice di hit test restituiti nel parametro pwHitTestCode della funzione HitTestThemeBackground.
ms.assetid: 95b4fc1a-2f9b-4464-b672-552d36b60c42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219cb59115bae56ac6cc3ba7f05384c331969b34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044554"
---
# <a name="hit-test-return-values"></a>Valori restituiti hit test

Questa sezione elenca i valori del codice di hit test restituiti nel parametro *pwHitTestCode* della funzione [**HitTestThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) . I valori di codice restituiti dipendono dalle opzioni di hit test specificate nel parametro *dwOptions* della funzione **HitTestThemeBackground** . Per un elenco delle opzioni, vedere [Opzioni di hit test](theme-hit-test-options.md).

## <a name="return-values"></a>Valori restituiti

Nella tabella seguente sono elencate le opzioni di hit test e i corrispondenti codici restituiti.



| Opzione                       | Codici restituiti  | Descrizione                                                                                                        |
|------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------|
| \_BACKGROUNDSEG HTTB          | HTBOTTOM      | L'hit test ha avuto esito positivo nel segmento inferiore del bordo.                                                                   |
|                              | HTBOTTOMLEFT  | L'hit test ha avuto esito positivo nell'intersezione tra i bordi inferiore e sinistro.                                                     |
|                              | HTBOTTOMRIGHT | L'hit test ha avuto esito positivo nell'intersezione dei bordi inferiore e destro.                                                    |
|                              | HTCLIENT      | L'hit test ha avuto esito positivo nel segmento di sfondo medio.                                                               |
|                              | HTLEFT        | L'hit test ha avuto esito positivo nel segmento sinistro del bordo.                                                                     |
|                              | HTNOWHERE     | L'hit test ha avuto esito positivo all'esterno del controllo o in un'area trasparente.                                                   |
|                              | HTRIGHT       | L'hit test ha avuto esito positivo nel segmento di bordo destro.                                                                    |
|                              | HTTOP         | L'hit test ha avuto esito positivo nel segmento di bordo superiore.                                                                      |
|                              | HTTOPLEFT     | L'hit test ha avuto esito positivo nell'intersezione tra i bordi superiore e sinistro.                                                            |
|                              | HTTOPRIGHT    | L'hit test ha avuto esito positivo nell'intersezione dei bordi superiore e destro.                                                       |
| \_didascalia HTTB                | HTCAPTION     | L'hit test ha avuto esito positivo nei segmenti di sfondo superiore, superiore sinistro o superiore destro.                                         |
|                              | HTNOWHERE     | L'hit test ha avuto esito positivo all'esterno del controllo o in un'area trasparente.                                                   |
| \_FIXEDBORDER HTTB            | HTBORDER      | L'hit test ha avuto esito positivo in qualsiasi segmento di sfondo eccetto il segmento di sfondo medio.                                 |
|                              | HTCLIENT      | L'hit test ha avuto esito positivo nel segmento di sfondo medio.                                                               |
| \_RESIZINGBORDER HTTB         | HTBORDER      | L'hit test ha avuto esito negativo nel segmento di sfondo medio e nelle zone di ridimensionamento, ma è riuscito in un segmento di bordo in background. |
| HTTB \_ RESIZINGBORDER \_ Bottom | HTBOTTOM      | L'hit test ha avuto esito positivo nel segmento inferiore del bordo.                                                                   |
| RESIZINGBORDER HTTB a \_ \_ sinistra   | HTLEFT        | L'hit test ha avuto esito positivo nel segmento sinistro del bordo.                                                                     |
| HTTB \_ RESIZINGBORDER a \_ destra  | HTRIGHT       | L'hit test ha avuto esito positivo nel segmento di bordo destro.                                                                    |
| HTTB \_ RESIZINGBORDER in \_ alto    | HTTOP         | L'hit test ha avuto esito positivo nel segmento di bordo superiore.                                                                      |



 

 

 




