---
title: Attributo Type (Shape) (la)
description: Attributo Type (Shape) (la)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e53b275d6b6327b3d3783704dbd06156e643f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046902"
---
# <a name="type-attribute-shapevml"></a>Attributo Type (Shape) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un riferimento all'ID di un elemento [TipoForma](msdn-online-vml-shapetype-element.md) . Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

``` syntax
<v:
          element 
          type=" expression ">
```

**Sintassi dello script**

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

**Osservazioni:**

Se l'attributo **Type** fa riferimento all'ID di un elemento **TipoForma** , i riempimenti, i percorsi e i tratti di **TipoForma** vengono usati come modelli per creare la forma. I valori derivati da **TipoForma** possono essere sottoposti a override dai singoli valori della forma.

Se usato nei tag, il valore della stringa deve iniziare con un simbolo di cancelletto ( \# ).

**Attributo standard la**

**Esempio**

Una forma **TipoForma** viene creata con "MyType" come ID.


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



Se quindi si crea una forma usando i valori **TipoForma** , la forma avrà gli attributi di "MyType" **TipoForma**; ovvero "shape01" avrà un riempimento rosso con un tratto blu.


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



È possibile eseguire l'override dei valori ereditati, ad esempio, modificando il colore in verde.


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



[Esempio di attributo Type](/previous-versions/bb264099(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 