---
title: Valori restituiti dell'hit test
description: Questa sezione elenca i valori del codice di hit test restituiti nel parametro pwHitTestCode della funzione HitTestThemeBackground.
ms.assetid: 95b4fc1a-2f9b-4464-b672-552d36b60c42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020765e6f766efc2c79e869a1b06cfceac2c13a451cc381d88ae066cc1478c11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797601"
---
# <a name="hit-test-return-values"></a>Valori restituiti dell'hit test

Questa sezione elenca i valori del codice di hit test restituiti nel *parametro pwHitTestCode* della [**funzione HitTestThemeBackground.**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) I valori del codice restituiti dipendono dalle opzioni di hit test specificate nel *parametro dwOptions* della **funzione HitTestThemeBackground.** Per un elenco delle opzioni, vedere [Opzioni di hit test.](theme-hit-test-options.md)

## <a name="return-values"></a>Valori restituiti

Nella tabella seguente sono elencate le opzioni di hit test e i codici restituiti corrispondenti.



| Opzione                       | Codici restituiti  | Descrizione                                                                                                        |
|------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------|
| HTTB \_ BACKGROUNDSEG          | HTBOTTOM      | L'hit test ha avuto esito positivo nel segmento del bordo inferiore.                                                                   |
|                              | HTBOTTOMLEFT  | L'hit test ha avuto esito positivo nell'intersezione dei bordi inferiore e sinistro.                                                     |
|                              | HTBOTTOMRIGHT | L'hit test ha avuto esito positivo nell'intersezione dei bordi inferiore e destro.                                                    |
|                              | HTCLIENT      | Hit test riuscito nel segmento di sfondo intermedio.                                                               |
|                              | HTLEFT        | Hit test riuscito nel segmento del bordo sinistro.                                                                     |
|                              | HTNOWHERE     | L'hit test ha avuto esito positivo all'esterno del controllo o in un'area trasparente.                                                   |
|                              | HTRIGHT       | Hit test riuscito nel segmento del bordo destro.                                                                    |
|                              | HTTOP         | Hit test riuscito nel segmento del bordo superiore.                                                                      |
|                              | HTTOPLEFT     | L'hit test ha avuto esito positivo nell'intersezione dei bordi superiore e sinistro.                                                            |
|                              | HTTOPRIGHT    | L'hit test ha avuto esito positivo nell'intersezione dei bordi superiore e destro.                                                       |
| DIDASCALIA \_ HTTB                | APTION     | L'hit test ha avuto esito positivo nei segmenti di sfondo in alto a sinistra o in alto a destra.                                         |
|                              | HTNOWHERE     | L'hit test ha avuto esito positivo all'esterno del controllo o in un'area trasparente.                                                   |
| HTTB \_ FIXEDBORDER            | HTBORDER      | L'hit test ha avuto esito positivo in qualsiasi segmento di sfondo ad eccezione del segmento di sfondo intermedio.                                 |
|                              | HTCLIENT      | Hit test riuscito nel segmento di sfondo intermedio.                                                               |
| HTTB \_ RESIZINGBORDER         | HTBORDER      | L'hit test non è riuscito nel segmento di sfondo centrale e nelle zone di ridimensionamento, ma ha avuto esito positivo in un segmento di bordo di sfondo. |
| HTTB \_ RESIZINGBORDER \_ BOTTOM | HTBOTTOM      | L'hit test ha avuto esito positivo nel segmento del bordo inferiore.                                                                   |
| HTTB \_ RESIZINGBORDER \_ LEFT   | HTLEFT        | Hit test riuscito nel segmento del bordo sinistro.                                                                     |
| HTTB \_ RESIZINGBORDER \_ RIGHT  | HTRIGHT       | Hit test riuscito nel segmento del bordo destro.                                                                    |
| HTTB \_ RESIZINGBORDER \_ TOP    | HTTOP         | Hit test riuscito nel segmento del bordo superiore.                                                                      |



 

 

 




