---
title: Disegno di forme di base
description: Questo articolo descrive il disegno di forme di base in VML, una funzionalità deprecata a Windows Internet Explorer 9.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Workshop Web, disegno di forme
- progettazione di pagine Web, disegno di forme
- Vector Markup Language (VML), disegno di forme
- VML (Vector Markup Language),disegno di forme
- grafica vettoriale, disegno di forme
- disegno di forme
- forme VML, disegno
- Vector Markup Language (VML),XML
- VML (Vector Markup Language),XML
- grafica vettoriale, XML
- Vector Markup Language (VML),CSS2
- VML (Vector Markup Language),CSS2
- grafica vettoriale, CSS2
- Vector Markup Language (VML),elements
- VML (Vector Markup Language),elements
- grafica vettoriale, elementi
- elementi VML, disegno di forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4a8b7985371d9cffc6e7359cef1a17c69c403c7802de458b68d9df8c36e3ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136924"
---
# <a name="drawing-basic-shapes"></a>Disegno di forme di base

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

In questo argomento verrà illustrato come sia facile disegnare una forma usando VML.

Per creare un ovale rosso in una pagina Web, come illustrato nell'immagine seguente, è possibile disegnare l'ovale usando uno strumento di modifica grafica, salvare il disegno come bitmap e quindi inserire la bitmap nella pagina Web:

![oval1.gif (627 byte)](images/oval1.gif)

In alternativa, è possibile usare VML per disegnare grafica. Nell'esempio precedente è possibile digitare le righe seguenti nell'area della pagina `<BODY>` Web per disegnare l'ovale rosso:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





`<v:...>` e `</v:...>` sono il tag di inizio e il tag di fine nella [sintassi XML](#xml-structure).`style='width:100pt; height:75pt'` fornisce [informazioni CSS](#css-information). **oval** e **fillcolor**="red" sono [elementi VML](#vml-elements).

È possibile modificare la grafica modificando semplicemente gli attributi delle proprietà in VML. Nell'esempio precedente, se si modifica in , come illustrato nella rappresentazione `fillcolor="red"` `fillcolor="blue"` VML seguente, l'ovale rosso verrà modificato in blu:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





I browser che supportano VML possono eseguire il rendering e visualizzare la grafica rappresentata in VML senza dover scaricare file di immagine separati. Il rendering della maggior parte degli elementi grafici rappresentati in VML viene eseguito più velocemente nei browser e richiede meno spazio su disco e tempi di download.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="xml-structure"></a>Struttura XML

VmL viene formattato in base alle regole di Extensible Markup Language (XML). Qualsiasi parser XML standard può analizzare il linguaggio VML e traslare i dati risultanti a un processore specifico di VML. Per consentire ai browser di determinare come traslare i dati a un [](web-workshop---how-to-use-vml-on-web-pages----appendix.md) processore specifico di VML, è necessario digitare alcune informazioni, ad esempio spazi dei nomi e [oggetti personalizzati incorporati.](web-workshop---how-to-use-vml-on-web-pages----appendix.md) È quindi possibile usare VML per digitare grafica nell'area come `<BODY>` nell'esempio precedente.

Il `"v:"` prefisso in ogni tag XML identifica il tag come VML. Il `"v:"` prefisso `<BODY>` nell'area deve essere coerente con `<html xmlns:v="...">` .

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="css-information"></a>Informazioni CSS

VML [usa Cascading Style Sheets, livello 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) per determinare le dimensioni della grafica e per posizionare la grafica in una pagina Web. Nell'esempio precedente la dimensione dell'ovale è stata specificata come 100 punti (larghezza) per 75 punti (altezza) ( `style='width:100pt;height:75pt'` ).

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="vml-elements"></a>Elementi VML

Nell'esempio precedente è stato usato un elemento predefinito VML `<oval>` per disegnare un ovale. È stato quindi usato **l'attributo della** proprietà fillcolor dell'elemento `<oval>` per riempire l'ovale con il rosso.

In base alla [sezione Start-Tags, End-Tags](https://www.w3.org/TR/REC-xml#sec-starttags) e Empty-Element Tags della specifica [XML 1.0,](https://www.w3.org/TR/REC-xml)i tag di elemento vuoto possono essere usati per qualsiasi elemento senza contenuto. Ad esempio, come illustrato nella rappresentazione VML seguente, non è presente alcun contenuto (sotto-elemento) all'interno `<oval>` dell'elemento . Si noti che lo **stile e** il colore **di riempimento** sono gli attributi dell'elemento e non sono `<oval>` elementi secondari.


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



Pertanto, è possibile usare il tag di elemento vuoto, come illustrato nella rappresentazione VML seguente, per rappresentare la stessa cosa della riga precedente.


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="summary"></a>Riepilogo

È possibile usare VML per disegnare grafica in una pagina Web e quindi personalizzare tali elementi modificando semplicemente gli attributi delle proprietà. Inoltre, il rendering della maggior parte della grafica rappresentata in VML viene eseguito più velocemente nei browser e richiede meno tempo di download e spazio su disco.

 

 