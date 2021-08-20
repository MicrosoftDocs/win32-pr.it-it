---
title: Attributo colori VML
description: Attributo colori VML
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a699b0ab8da898dd82fa4e1bf4823c0f9fdd443eb8275e25dbfaac6d2f039a6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999281"
---
# <a name="vml-colors-attribute"></a>Attributo colori VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce più colori per un riempimento sfumato. Proprietà di lettura/scrittura. **Oggetto IVgGradientColorArray.**

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi dei tag**

<v: *element* colors=" *expression* ">

**Sintassi dello script**

*element* .colors="*expression*"

*expression* = *.colors dell'elemento*

**Osservazioni:**

Usato per definire una matrice costituita da valori abbinati di percentuali ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) e colore ([VgColor](msdn-online-vml-ivgcolor.md)). La matrice crea un riempimento misto usando ogni punto della matrice, a partire da 0% (definito da **Color)** e terminando in corrispondenza del 100% (definito da **Color2).** I colori intermedi lungo il percorso possono essere definiti assegnando un valore di colore a una percentuale. La coppia di percentuali e colori non è separata da una virgola, ma le coppie sono separate tra loro da virgole.

Attributo VML Standard

**Esempio**

La forma ha un riempimento sfumato costituito da quattro colori, a partire dal rosso, con fusione in giallo, verde e infine blu.


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



 

 