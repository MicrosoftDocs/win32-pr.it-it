---
title: Disegno di forme di base
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Web Workshop, disegno di forme
- progettazione di pagine Web, disegno di forme
- Vector Markup Language (la), disegno di forme
- LA (Vector Markup Language), disegno di forme
- grafica vettoriale, forme disegno
- disegno di forme
- LA forme, disegno
- Vector Markup Language (la), XML
- LA (Vector Markup Language), XML
- grafica vettoriale, XML
- Vector Markup Language (la), CSS2
- LA (Vector Markup Language), CSS2
- grafica vettoriale, CSS2
- Vector Markup Language (la), elementi
- LA (Vector Markup Language), elementi
- grafica vettoriale, elementi
- Elementi la, disegno di forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7ab25fc9310750c9f49c5978a063c76639ec4bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474011"
---
# <a name="drawing-basic-shapes"></a>Disegno di forme di base

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

In questo argomento verrà illustrato quanto sia facile disegnare una forma usando la.

Per creare un Oval rosso in una pagina Web, come illustrato nell'immagine seguente, è possibile disegnare l'ovale usando uno strumento di modifica grafico, salvare il disegno come bitmap e quindi inserire la bitmap nella pagina Web:

![oval1.gif (627 byte)](images/oval1.gif)

In alternativa, è possibile usare la per creare grafica. Nell'esempio precedente, è possibile digitare le righe seguenti nell' `<BODY>` area della pagina Web per creare l'ovale rosso:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





`<v:...>` e `</v:...>` sono i tag di inizio e di fine nella [sintassi XML](#xml-structure).`style='width:100pt; height:75pt'` fornisce [informazioni CSS](#css-information). **Oval** e **FillColor**= "Red" sono [elementi la](#vml-elements).

È possibile modificare la grafica semplicemente modificando gli attributi delle proprietà in la. Nell'esempio precedente, se si passa `fillcolor="red"` a `fillcolor="blue"` , come illustrato nella seguente rappresentazione la, il rosso ovale cambierà in blu:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





I browser che supportano la possono eseguire il rendering e la visualizzazione della grafica rappresentata in la senza dover scaricare file di immagine separati. La maggior parte degli elementi grafici rappresentati in la viene sottoposta a rendering più velocemente nei browser e richiedono meno spazio su disco e tempi di download

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="xml-structure"></a>Struttura XML

LA viene formattato in base alle regole di Extensible Markup Language (XML). Qualsiasi parser XML standard può analizzare la e passare i dati risultanti a un processore specifico di la. Per fare in modo che i browser sappiano come passare i dati a un processore specifico di la, è necessario digitare alcune informazioni, ad esempio [spazi dei nomi](web-workshop---how-to-use-vml-on-web-pages----appendix.md) e [oggetti personalizzati incorporati](web-workshop---how-to-use-vml-on-web-pages----appendix.md). È quindi possibile usare la per digitare elementi grafici nell' `<BODY>` area così come è stato fatto nell'esempio precedente.

Il `"v:"` prefisso in ogni tag XML identifica il tag come la. Il `"v:"` prefisso nell' `<BODY>` area deve essere coerente con `<html xmlns:v="...">` .

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="css-information"></a>Informazioni CSS

LA utilizza [Cascading Style Sheets, livello 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) per determinare le dimensioni della grafica e per posizionare la grafica in una pagina Web. Nell'esempio precedente è stata specificata la dimensione dell'ovale come 100 punti (larghezza) per 75 punti (altezza) ( `style='width:100pt;height:75pt'` ).

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="vml-elements"></a>Elementi la

Nell'esempio precedente è stato usato un elemento predefinito la `<oval>` per creare un Oval. È stato quindi usato l'attributo della proprietà **FillColor** dell' `<oval>` elemento per riempire l'ovale con il rosso.

In base ai tag di [inizio, tag finali e tag Empty-Element](https://www.w3.org/TR/REC-xml#sec-starttags) della [specifica XML 1,0](https://www.w3.org/TR/REC-xml), i tag degli elementi vuoti possono essere usati per qualsiasi elemento senza contenuto. Ad esempio, come illustrato nella seguente rappresentazione la, non è presente alcun contenuto (sottoelemento) nell' `<oval>` elemento. (Si noti che lo **stile** e **FillColor** sono gli attributi dell' `<oval>` elemento, non sono sottoelementi).


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



Pertanto, è possibile utilizzare il tag elemento vuoto, come illustrato nella seguente rappresentazione la, per rappresentare lo stesso elemento della riga precedente.


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="summary"></a>Riepilogo

È possibile usare la per creare elementi grafici in una pagina Web e quindi personalizzare tali elementi semplicemente modificando gli attributi delle proprietà. Inoltre, la maggior parte dei grafici rappresentati in la viene sottoposta a rendering più velocemente nei browser e non è più tempo di download e spazio su disco

 

 