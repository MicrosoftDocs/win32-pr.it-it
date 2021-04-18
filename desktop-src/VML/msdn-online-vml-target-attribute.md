---
title: Attributo di destinazione la
description: Attributo di destinazione la
ms.assetid: 2e1cc002-65c9-4945-8c07-f23dc704d867
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cb4e438cef8d10093aa2788fc1493d9e2dcc75
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299847"
---
# <a name="vml-target-attribute"></a>Attributo di destinazione la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un frame o una finestra in cui viene visualizzato un URL. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* target = " *Expression* " >

**Osservazioni:**

L'attributo di **destinazione** è simile all'attributo di **destinazione** HTML standard degli ancoraggi.

I possibili valori sono:



| Valore      | Descrizione                                                                                                                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TargetName | Stringa contenente il nome del frame o della finestra in cui caricare il documento.                                                                                                                                                                                 |
| \_vuoto    | Specifica che il documento collegato viene caricato in una nuova finestra vuota. Questa finestra non è denominata.                                                                                                                                                                  |
| \_media    | A partire da Internet Explorer 6 per Windows XP Service Pack 2, l' \_ attributo supporto è obsoleto e non è più supportato. Disponibile per la prima volta in Internet Explorer 6, questo valore specifica che il documento collegato deve essere caricato sulla barra multimediale.                |
| \_padre   | Specifica che il documento collegato viene caricato nell'elemento padre diretto del documento contenente il collegamento.                                                                                                                                                      |
| \_ricerca   | A partire da Internet Explorer 7 per Windows XP Service Pack 2,: l' \_ attributo di ricerca è obsoleto e non è più supportato. Disponibile per la prima volta in Internet Explorer 6, questo valore specifica che il documento collegato deve essere caricato nel riquadro di ricerca del browser. |
| \_auto     | Specifica che il documento collegato viene caricato nella finestra in cui è stato fatto clic sul collegamento (la finestra attiva).                                                                                                                                                  |
| \_In alto      | Specifica che il documento collegato viene caricato nella finestra in primo piano.                                                                                                                                                                                            |



 

*Attributo standard la*

**Esempio**

Quando si fa clic sul rettangolo, il browser carica il home page Microsoft Corporation nella stessa finestra.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com" target="_self"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Esempio di attributo di destinazione](/previous-versions/bb264096(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 