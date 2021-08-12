---
title: Attributo VML InvY
description: Attributo VML InvY
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d012e8ac6afe0e7808236c36d8dd3088ce9fa3552b4b7efa0542ea8612e4d36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599869"
---
# <a name="vml-invy-attribute"></a>Attributo VML InvY

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se la posizione y dell'handle è invertita. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[H](msdn-online-vml-h-element.md) (sottoelemento di [Handle](msdn-online-vml-handles-element.md))

**Sintassi dei tag**

<v: *element* invy=" *expression* ">

**Osservazioni:**

Se **True,** la posizione y dell'handle viene invertita sottraendo il valore y dal valore y di **CoordOrigin** aggiunto al valore y di **CoordSize.** Il valore predefinito è **False**.

Questo attributo è l'equivalente di


```HTML
coordorigin.y + coordsize.y - h.position.y
```



*Attributo VML Standard*

 

 