---
title: Attributo src (VMLFrame) (la)
description: Attributo src (VMLFrame) (la)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a9c3ec4849098c9469fba56f26d4c3dd514746
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337951"
---
# <a name="src-attribute-vmlframevml"></a>Attributo src (VMLFrame) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce l'origine dei dati per il frame. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintassi Tag**

<v: *element* src = " *Expression* " >

**Sintassi dello script**

*element* . src = "*Expression*"

*espressione* = *elemento*. src

**Osservazioni:**

L'attributo **src** può includere le seguenti sintassi:

-   URL del file esterno. Il file deve essere un file XML con il formato seguente:
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   All'interno del file è necessario disporre di una o più forme la con ID validi a cui è possibile fare riferimento utilizzando questa sintassi:
    ```HTML
       filename#shapename
    ```

    

-   Nel seguente riferimento, i file esterni hanno l'estensione. la, ma è possibile usare qualsiasi estensione:
    ```HTML
       external.vml#image01
    ```

    

-   È possibile fare riferimento a una forma nello stesso file usando la sintassi seguente:
    ```HTML
       #shapename
    ```

    

Se il **clip** è **false**, la forma verrà ridimensionata in base al frame. Se **true**, tutte le parti della forma che si trovano all'esterno del frame non verranno visualizzate.

Si noti che l' [origine](origin-attribute--vmlframe--vml.md) e le [dimensioni](size-attribute--vmlframe.md) non verranno utilizzate a meno che la **clip** non sia **true**.

**Attributo standard la**

**Esempio**

L'immagine definita nel file esterno verrà ritagliata.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 