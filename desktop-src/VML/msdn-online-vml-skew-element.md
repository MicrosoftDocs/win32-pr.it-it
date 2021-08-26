---
title: Elemento VML Skew
description: Elemento VML Skew
ms.assetid: ab58bbd9-5fb2-434f-adea-9b3d2d170804
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d659d16e6d10e9ec88875989a812de82403d2ac5b946580e7c7b7def956b45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099041"
---
# <a name="vml-skew-element"></a>Elemento VML Skew

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce un'a inclinazione per una forma.

Gli attributi seguenti modificano un'a inclinazione.



| Attributo                                 | Descrizione                                    |
|-------------------------------------------|------------------------------------------------|
| [Ext](ext-attribute--skew--vml.md)       | Definisce la modalità di visualizzazione di un'a inclinazione.           |
| [ID](id-attribute--skew--vml.md)         | Definisce un identificatore univoco per un'a inclinazione.        |
| [Matrice](matrix-attribute--skew--vml.md) | Definisce una trasformazione prospettica per un'a inclinazione.    |
| [Offset](offset-attribute--skew--vml.md) | Definisce l'offset di un'a inclinazione.                  |
| [Sì](on-attribute--skew--vml.md)         | Determina se verrà visualizzata l'a inclinazione. |
| [Origine](origin-attribute--skew--vml.md) | Determina l'origine di un'a inclinazione.               |



 

**Osservazioni:**

Questo elemento deve essere definito all'interno di un [elemento Shape.](shape-element--vml.md)

Inoltre, gli [attributi Matrix](matrix-attribute--skew--vml.md) e [On](on-attribute--skew--vml.md) devono essere impostati su **True.**

Di seguito è riportato il codice minimo necessario per produrre un'a inclinazione.


```HTML
   <v:rect
   fillcolor="green"
   style="position:relative;top:1;left:1;width:50;height:50">
   <o:skew on="t" matrix="1,-0.5,0,0.75,0,0"/>
   </v:rect>
```



**L'elemento Skew** è un'Microsoft Office a VML.

**esempi**

-   [Esempio di a inclinazione semplice](/previous-versions/bb229482(v=vs.85))
-   [Esempio di a inclinazione dinamica](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/skew/x_skew.md)

 

 