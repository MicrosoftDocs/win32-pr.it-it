---
title: Attributo ID (VML)
description: Attributo ID (VML)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0ba0addd2d6af8a8b38af4085c79123d3178a3299269468abd73fff1951d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007860"
---
# <a name="id-attribute-vml"></a>Attributo ID (VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Fornisce un identificatore univoco per un elemento. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

Tutti gli elementi VML.

**Sintassi dei tag**

<v: *elementname* id=" *idname* ">

**Sintassi dello script**

*elementname* .id =" *idname* "

*expression* = *elementname*.id

**Osservazioni:**

Usare **l'ID** per fare riferimento a un elemento specifico. Dopo aver creato una forma e aver assegnato un ID, è possibile usare il nome ID quando si vuole modificare l'elemento.

**L'ID** è necessario per usare [l'elemento ShapeType.](msdn-online-vml-shapetype-element.md)

Quando VML viene generato da Microsoft Office, se alla forma viene assegnato un nome di modello a oggetti, **l'ID** viene impostato su questo nome. Se il nome del modello a oggetti non è impostato, il nome viene generato usando *lo Spid* (ID forma interno) più un prefisso (S per la forma, M per la forma master, T per shapetype).

*Attributo VML Standard*.

**Esempio**

Per modificare gli attributi di una forma, è innanzitutto necessario assegnare alla forma un ID. ad esempio "myrect".


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```




```HTML
   myrect.style.width = 80
   myrect.style.height = 80
   myrect.fillColor = "green"
```



[Esempio di attributo ID](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 