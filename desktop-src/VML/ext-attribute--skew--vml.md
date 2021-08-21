---
title: Attributo Ext (Skew)(VML)
description: Attributo Ext (Skew)(VML)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a001812a5504940509fac82333b2ca637ae76a913218f44cd3a06b4c18bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125361"
---
# <a name="ext-attribute-skewvml"></a>Attributo Ext (Skew)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la modalità di visualizzazione di un'avalla. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Inclinazione](msdn-online-vml-skew-element.md)

**Sintassi dei tag**

*<:elemento* v:ext=" *expression* ">

**Sintassi dello script**

*element* .ext="*expression*"

*expression* = *elemento*.ext

**Osservazioni:**

Questo attributo viene usato per indicare agli editor grafici come elaborare **l'elemento Skew.** I possibili valori sono:

-   **edit**
-   **view** (impostazione predefinita)
-   **backwardCompatible**

Se un'estensione è impostata **per la modifica,** può essere ignorata da un visualizzatore software. Se impostato su **view**, il visualizzatore deve invece eseguire il rendering della rappresentazione bitmap.

*Microsoft Office Attributo Extensions*

 

 