---
title: Attributo Src (VMLFrame)(VML)
description: Attributo Src (VMLFrame)(VML)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44f7761a55304eefc655d00ed58d84b7af8f7ce5daf86a3aaf462308b43c193
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057584"
---
# <a name="src-attribute-vmlframevml"></a>Attributo Src (VMLFrame)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce l'origine dei dati per il frame. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintassi dei tag**

<v: *element* src=" *expression* ">

**Sintassi dello script**

*element* .src="*expression*"

*expression* = *elemento*.src

**Osservazioni:**

**L'attributo Src** può includere le sintassi seguenti:

-   URL del file esterno. Il file deve essere un file XML con il formato seguente:
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   All'interno del file è necessario avere una o più forme VML con ID validi a cui è possibile fare riferimento usando questa sintassi:
    ```HTML
       filename#shapename
    ```

    

-   Nel riferimento seguente i file esterni hanno l'estensione vml, ma è possibile usare qualsiasi estensione:
    ```HTML
       external.vml#image01
    ```

    

-   È possibile fare riferimento a una forma all'interno dello stesso file usando la sintassi seguente:
    ```HTML
       #shapename
    ```

    

Se **Clip** è **False,** la forma verrà ridimensionata in base al frame. Se **True,** le parti della forma esterne al frame non verranno visualizzate.

Si noti [che Origin](origin-attribute--vmlframe--vml.md) e [Size](size-attribute--vmlframe.md) non verranno usati a meno che **Clip** non sia **True.**

**Attributo VML Standard**

**Esempio**

L'immagine definita nel file esterno verrà ritagliata.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 