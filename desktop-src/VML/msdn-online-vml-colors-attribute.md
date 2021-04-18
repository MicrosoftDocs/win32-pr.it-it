---
title: Attributo colori la
description: Attributo colori la
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c5df5b2dc97c19441d6abaf6cd6c03d949c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516965"
---
# <a name="vml-colors-attribute"></a>Attributo colori la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce più colori per un riempimento sfumato. Proprietà di lettura/scrittura. **IVgGradientColorArray**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *elemento* Colors = " *Expression* " >

**Sintassi dello script**

*element* . Colors = "*Expression*"

*espressione* = *elemento*. Colors

**Osservazioni:**

Utilizzato per definire una matrice costituita da valori abbinati di percentuali ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) e color ([VgColor](msdn-online-vml-ivgcolor.md)). La matrice crea un riempimento sfumato usando ogni punto della matrice, a partire dallo 0% (definito da **colore**) e terminando al 100% (definito da **color2**). È possibile definire colori intermedi lungo il percorso assegnando un valore di colore a una percentuale. La coppia percentuale e colore non è separata da una virgola, ma le coppie sono separate tra loro da virgole.

Attributo standard la

**Esempio**

La forma presenta un riempimento sfumato costituito da quattro colori, a partire da rosso, da sfumatura a giallo, da verde a finallyblue.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   colors="30% yellow,70% green"/>
   </v:shape>
```



 

 