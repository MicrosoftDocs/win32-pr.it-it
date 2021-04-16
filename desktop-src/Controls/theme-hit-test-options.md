---
title: Opzioni di hit test
description: Questa sezione elenca i valori delle opzioni usati con il parametro dwOptions della funzione HitTestThemeBackground. Per un elenco dei valori restituiti quando si specifica una di queste opzioni, vedere valori restituiti di hit test.
ms.assetid: a0d5c6c8-bb50-46e1-98ae-2374842344c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 638a7aaca83c658ad852b195cdb9514210a14c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471294"
---
# <a name="hit-test-options"></a>Opzioni di hit test

Questa sezione elenca i valori delle opzioni usati con il parametro *dwOptions* della funzione [**HitTestThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) . Per un elenco dei valori restituiti quando si specifica una di queste opzioni, vedere [valori restituiti di hit test](theme-hit-test-retval.md).

## <a name="option-values"></a>Valori delle opzioni

Nella tabella seguente sono elencate le opzioni di hit test.



| Opzione                       | Valore                                                                                                                    | Descrizione                                                                                                                                                                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_BACKGROUNDSEG HTTB          | 0x00000000                                                                                                               | Opzione hit test del segmento background del tema.                                                                                                                                           |
| \_FIXEDBORDER HTTB            | 0x00000002                                                                                                               | Opzione di hit test del bordo fisso.                                                                                                                                                       |
| \_didascalia HTTB                | 0x00000004                                                                                                               | Opzione Didascalia hit test.                                                                                                                                                            |
| \_RESIZINGBORDER HTTB         | (HTTB \_ RESIZINGBORDER \_ Left \| HTTB \_ RESIZINGBORDER \_ Top \| HTTB \_ RESIZINGBORDER \_ right \| HTTB \_ RESIZINGBORDER \_ Bottom) | Ridimensionamento delle opzioni di hit test del bordo.                                                                                                                                                   |
| RESIZINGBORDER HTTB a \_ \_ sinistra   | 0x00000010                                                                                                               | Ridimensionamento dell'opzione di hit test del bordo sinistro.                                                                                                                                               |
| HTTB \_ RESIZINGBORDER in \_ alto    | 0x00000020                                                                                                               | Ridimensionamento dell'opzione di hit test del bordo superiore.                                                                                                                                                |
| HTTB \_ RESIZINGBORDER a \_ destra  | 0x00000040                                                                                                               | Ridimensionamento dell'opzione di hit test del bordo destro.                                                                                                                                              |
| HTTB \_ RESIZINGBORDER \_ Bottom | 0x00000080                                                                                                               | Ridimensionamento dell'opzione di hit test del bordo inferiore.                                                                                                                                             |
| \_SIZINGTEMPLATE HTTB         | 0x00000100                                                                                                               | Il bordo di ridimensionamento viene specificato come modello, non solo per i bordi della finestra. Questa opzione si escludono a vicenda con HTTB \_ SYSTEMSIZINGMARGINS; SIZINGTEMPLATE HTTB ha la \_ precedenza.         |
| \_SYSTEMSIZINGMARGINS HTTB    | 0x00000200                                                                                                               | USA lo spessore del bordo di ridimensionamento del sistema anziché i margini del contenuto dello stile di visualizzazione. Questa opzione si escludono a vicenda con HTTB \_ SIZINGTEMPLATE; SIZINGTEMPLATE HTTB ha la \_ precedenza. |



 

 

 




