---
title: Opzioni di hit test
description: Questa sezione elenca i valori delle opzioni usati con il parametro dwOptions della funzione HitTestThemeBackground. Per un elenco dei valori restituiti quando si specifica una di queste opzioni, vedere Valori restituiti dell'hit test.
ms.assetid: a0d5c6c8-bb50-46e1-98ae-2374842344c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e3f9f3c7ba8b5c7a2c4468177befc3083bb2ed613b674cdb02f7fd3ad7f10c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166526"
---
# <a name="hit-test-options"></a>Opzioni di hit test

Questa sezione elenca i valori delle opzioni usati con il *parametro dwOptions* della [**funzione HitTestThemeBackground.**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) Per un elenco dei valori restituiti quando si specifica una di queste opzioni, vedere [Hit Test Return Values](theme-hit-test-retval.md).

## <a name="option-values"></a>Valori delle opzioni

Nella tabella seguente sono elencate le opzioni di hit test.



| Opzione                       | Valore                                                                                                                    | Descrizione                                                                                                                                                                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HTTB \_ BACKGROUNDSEG          | 0x00000000                                                                                                               | Opzione hit test del segmento di sfondo del tema.                                                                                                                                           |
| HTTB \_ FIXEDBORDER            | 0x00000002                                                                                                               | Correzione dell'opzione di hit test del bordo.                                                                                                                                                       |
| DIDASCALIA \_ HTTB                | 0x00000004                                                                                                               | Opzione dell'hit test della didascalia.                                                                                                                                                            |
| RIDIMENSIONAMENTO DI \_ HTTBBORDER         | (HTTB \_ RESIZINGBORDER \_ LEFT \| HTTB \_ RESIZINGBORDER \_ TOP \| HTTB \_ RESIZINGB RESIZINGBORDER \_ RIGHT \| HTTB \_ RESIZINGBORDER \_ BOTTOM) | Ridimensionamento delle opzioni di hit test del bordo.                                                                                                                                                   |
| RIDIMENSIONAMENTO DI HTTBB \_ A \_ SINISTRA   | 0x00000010                                                                                                               | Opzione ridimensionamento dell'hit test del bordo sinistro.                                                                                                                                               |
| HTTB \_ RESIZINGBORDER \_ TOP    | 0x00000020                                                                                                               | Opzione ridimensionamento dell'hit test del bordo superiore.                                                                                                                                                |
| RIDIMENSIONAMENTO DI HTTB \_ A \_ DESTRA  | 0x00000040                                                                                                               | Ridimensionamento dell'hit test del bordo destro.                                                                                                                                              |
| RIDIMENSIONAMENTO DI \_ HTTBBBORDER \_ INFERIORE | 0x00000080                                                                                                               | Opzione ridimensionamento dell'hit test del bordo inferiore.                                                                                                                                             |
| HTTB \_ SIZINGTEMPLATE         | 0x00000100                                                                                                               | Il ridimensionamento del bordo viene specificato come modello, non solo come bordi della finestra. Questa opzione si escludono a vicenda con HTTB \_ SYSTEMSIZINGMARGINS; HTTB \_ SIZINGTEMPLATE ha la precedenza.         |
| SISTEMI \_ HTTBIZINGMARGINS    | 0x00000200                                                                                                               | Usa la larghezza del bordo di ridimensionamento del sistema anziché i margini del contenuto dello stile di visualizzazione. Questa opzione si escludono a vicenda con HTTB \_ SIZINGTEMPLATE; HTTB \_ SIZINGTEMPLATE ha la precedenza. |



 

 

 




