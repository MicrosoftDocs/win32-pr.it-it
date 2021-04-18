---
description: Questa sezione contiene le funzioni principali per Tablet PC.
ms.assetid: 8f94a82c-de93-4649-a9b5-0adcbe01333d
title: Funzioni di Tablet PC Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9d0369a223959f011612b5aefc820a3668eeff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307488"
---
# <a name="core-tablet-pc-functions"></a>Funzioni di Tablet PC Core

Questa sezione contiene le funzioni principali per Tablet PC.

## <a name="in-this-section"></a>Contenuto della sezione



| Funzione                                                         | Descrizione                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddOneStroke**](addonestroke.md)                             | Aggiunge un nuovo oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) all'oggetto [**InkDivider**](inkdivider-class.md) passato.                                                                 |
| [**CallDivide**](calldivide.md)                                 | Recupera le informazioni di analisi dall'oggetto [**InkDivider**](inkdivider-class.md) .                                                                                                              |
| [**CallDivideResults**](calldivideresults.md)                   | Restituisce i risultati dell'analisi dall'oggetto [**InkDivider**](inkdivider-class.md) .                                                                                                                    |
| [**CallDivideResultsStrokeIds**](calldivideresultsstrokeids.md) | Recupera le proprietà [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) per gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) della parola, della riga, del paragrafo o del disegno corrispondente determinati dall'analisi dell'input penna. |
| [**CreateInkDivider**](createinkdivider.md)                     | Crea un'istanza di un'implementazione dell'interfaccia [**InkDivider**](inkdivider-class.md) e restituisce il relativo handle.                                                                                      |
| [**DeleteInkDivider**](deleteinkdivider.md)                     | Elimina un oggetto [**InkDivider**](inkdivider-class.md) e rilascia le risorse associate.                                                                                                         |
| [**InvokeIDispatch**](invokeidispatch.md)                       | Richiama la funzionalità helper per l'interfaccia IDispatch.                                                                                                                                           |
| [**RecognizerContextSet**](recognizercontextset.md)             | Verifica se l'oggetto [**InkDivider**](inkdivider-class.md) può usare la classe [**InkRecognizerContext**](inkrecognizercontext-class.md) per analizzare le parole.                                      |
| [**RemoveStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-removestrokes)                | Rimuove gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) da [**InkDivider**](inkdivider-class.md).                                                                                           |
| [**SetLineHeight**](setlineheight.md)                           | Imposta la proprietà [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) sull'oggetto [**InkDivider**](inkdivider-class.md) .                                                                                 |
| [**SetLineRecoCallback**](setlinerecocallback.md)               | Imposta una funzione di callback da utilizzare durante il riconoscimento della riga.                                                                                                                                        |



 

 

 
