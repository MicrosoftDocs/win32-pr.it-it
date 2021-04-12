---
title: Attributo ID (la)
description: Attributo ID (la)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a3925166a735b7813efd4cb9bc68f50bb8fa52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473478"
---
# <a name="id-attribute-vml"></a>Attributo ID (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Fornisce un identificatore univoco per un elemento. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

Tutti gli elementi la.

**Sintassi Tag**

<v: *ElementName* ID = " *IDname* " >

**Sintassi dello script**

*ElementName* . ID = " *IDname* "

*espressione* = *ElementName*. ID

**Osservazioni:**

Usare **ID** per fare riferimento a un elemento specifico. Dopo aver creato una forma e dato un ID, è possibile utilizzare il nome ID quando si desidera modificare l'elemento.

L' **ID** è necessario per usare l'elemento [TipoForma](msdn-online-vml-shapetype-element.md) .

Quando la viene generato da Microsoft Office, se il nome di un modello a oggetti viene assegnato alla forma, l' **ID** viene impostato su questo nome. Se il nome del modello a oggetti non è impostato, il nome viene generato utilizzando *SPID* (Internal Shape ID) più un prefisso (S per Shape, M per la forma master, T per TipoForma).

*Attributo standard la*.

**Esempio**

Per modificare gli attributi di una forma, è necessario innanzitutto assegnare un ID alla forma. ad esempio, "rect".


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



[Esempio di attributo ID](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 