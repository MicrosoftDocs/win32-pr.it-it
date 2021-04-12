---
title: Attributo DashStyle di la
description: Attributo DashStyle di la
ms.assetid: 7d6c7cbf-9ccc-4117-af0a-ca8f36684f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4651af9ade605166121c7225925e3bf1ed8264ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337718"
---
# <a name="vml-dashstyle-attribute"></a>Attributo DashStyle di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica il punto e il tratteggio per un tratto. Proprietà di lettura/scrittura. **VgLineDashStyle**.

**Si applica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintassi Tag**

<v: *element* DashStyle = " *Expression* " >

**Sintassi dello script**

*element* . DashStyle = "*Expression*"

*espressione* = *elemento*. DashStyle

**Osservazioni:**

I possibili valori sono:

-   Solid (valore predefinito)
-   ShortDash
-   ShortDot
-   ShortDashDot
-   ShortDashDotDot
-   Punto
-   Trattino
-   LongDash
-   DashDot
-   LongDashDot
-   LongDashDotDot

L'attributo **DashStyle** consente all'utente di specificare un modello Dash definito in modo personalizzato. Questa operazione viene eseguita usando una serie di numeri. Gli stili Dash sono definiti in termini di lunghezza del trattino (la parte disegnata del tratto) e della lunghezza dello spazio tra i trattini. Le lunghezze sono relative alla lunghezza riga: la lunghezza di "1" è uguale alla lunghezza riga. Lo stile di **estremità** viene applicato a ogni trattino, lo stile della freccia non lo è. La stringa definisce prima di tutto la lunghezza del trattino, quindi la lunghezza dello spazio. Questa operazione può essere ripetuta per formare stili trattini complessi. La stringa deve sempre contenere una coppia di numeri; Se contiene un numero dispari di numeri, l'ultimo può essere ignorato.

Nella tabella seguente sono elencati alcuni valori tipici e una descrizione dell'effetto desiderato. "0" implica un punto che dovrebbe essere quadruplo simmetrico (con i tappi di fine round deve essere un cerchio). Se il limite finale della riga è "flat", un visualizzatore deve scegliere un trattino del sistema operativo predefinito, laddove possibile (in altre parole. un elemento che è veloce da creare. La tabella seguente illustra alcuni esempi.



| DashStyle     | Descrizione                                                                                          |
|---------------|------------------------------------------------------------------------------------------------------|
| "2 2"         | Trattini brevi. Ogni trattino e lo spazio tra corrispondono al doppio della larghezza della linea.                        |
| "0 2"         | Punti. Lo spazio tra corrisponde al doppio della larghezza della linea.                                                  |
| "2 2 0 2"     | Punto di trattino breve.                                                                                      |
| "2 2 0 2 0 2" | Punto di tratteggio breve.                                                                                  |
| "1 2"         | Punto. Ogni trattino è la larghezza della linea, mentre ogni spazio corrisponde al doppio della larghezza della linea.            |
| "4 2"         | Dash. Ogni trattino è quattro volte la larghezza della linea mentre ogni spazio corrisponde al doppio della larghezza della linea. |
| "8 2"         | Trattino lungo.                                                                                           |
| "4 2 1 2"     | Punto tratteggiato.                                                                                            |
| "8 2 1 2"     | Punto di tratteggio lungo.                                                                                       |
| "8 2 1 2 1 2" | Punto di tratteggio lungo.                                                                                   |



 

*Attributo standard la*

**Esempio**

La forma presenta uno stile tratteggiato di trattini alternativi e punti.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200,200, 200,1 x e">
   <v:stroke dashstyle="dashdot"/>
   </v:shape>
```



 

 