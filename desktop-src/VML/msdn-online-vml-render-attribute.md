---
title: Attributo di rendering VML
description: Attributo di rendering VML
ms.assetid: a05e7f6e-4784-4ff8-9deb-0501d3a5658e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17063d1e742a5b014e18d61d2d4290eb2511843ef24f1513bd3564ee83c5e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513341"
---
# <a name="vml-render-attribute"></a>Attributo di rendering VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la modalità di rendering dell'estrusione. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Estrusione](msdn-online-vml-extrusion-element.md)

**Sintassi dei tag**

<o: *elemento* render=" *espressione* ">

**Sintassi dello script**

*elemento* .render="*expression*"

*expression* = *elemento*.render

**Osservazioni:**

I possibili valori sono:



| Valore        | Descrizione                                                   |
|--------------|---------------------------------------------------------------|
| Solido        | Il rendering visualizza una forma a tinta unita. Valore predefinito.                    |
| Wireframe    | Il rendering visualizza una forma wireframe.                         |
| boundingcube | Il rendering visualizza il cubo di delimitazione che contiene la forma. |



 

*Microsoft Office Attributo Extensions*

 

 