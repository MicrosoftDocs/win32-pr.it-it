---
title: Uso dell'elemento Path
description: Uso dell'elemento Path
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Workshop Web, elemento path
- progettazione di pagine Web, elemento path
- Vector Markup Language (VML),elemento path
- VML (Vector Markup Language),elemento path
- grafica vettoriale, elemento path
- path - elemento
- elementi VML, percorso
- Forme VML, elemento path
- Vector Markup Language (VML), personalizzazione dei contorni delle forme
- VML (Vector Markup Language),personalizzazione dei contorni delle forme
- grafica vettoriale, personalizzazione dei contorni delle forme
- forme VML, personalizzazione dei contorni
- personalizzazione dei contorni delle forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cbb27dbc2b039478903f697b02cefb14464b71a96ab2165db124d0a0053a400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057185"
---
# <a name="using-the-path-element"></a>Uso dell'elemento Path

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Si è appreso che è possibile usare gli elementi forma predefiniti VML, ad esempio , , , , , e , per `<oval>` `<line>` disegnare una `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` forma. In questo argomento verrà illustrato come usare il `<path>` sotto-elemento per personalizzare la struttura di una forma.

È possibile inserire il `<path>` sotto-elemento all'interno `<shape>` dell'elemento `<shapetype>` o . È quindi possibile usare gli attributi della proprietà del `<path>` sotto-elemento per personalizzare la struttura della forma.

Ad esempio, per disegnare la forma personalizzata illustrata nell'immagine seguente, è possibile usare il sotto-elemento per definire la struttura della forma, come illustrato nella rappresentazione `<path>` VML seguente:

![shape1.gif (1301 byte)](images/shape1p.gif)


```HTML
<body>
<v:shape style='width:250;height:250' strokecolor="red" strokeweight="1.5pt"
fillcolor="blue" coordorigin="0 0" coordsize="200 200">
<v:path v="m 8,65 l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155,
92,121, 42,155, 60,100 x e"/>
</v:shape>
</body>
```





-   I valori `m 8,65` indicano che il disegno inizia in corrispondenza del punto (8,65).
-   I valori indicano che una linea retta inizia in corrispondenza del punto corrente (8, 65) e termina in corrispondenza del punto `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` specificato (72, 65), che diventa il nuovo punto corrente. Una nuova riga inizia in corrispondenza del punto corrente (72, 65) e termina in corrispondenza del punto specificato, che diventa il nuovo punto corrente e così via, fino al punto finale (60, 100).
-   `x` indica che il percorso verrà chiuso da una linea retta che inizia dal punto corrente (60, 100) e termina in corrispondenza del punto originale (8, 65).
-   `e` indica l'interruzione del disegno.

Per altre informazioni su questo elemento, vedere la [specifica VML](https://www.w3.org/TR/NOTE-VML#-toc416858391) .

 

 