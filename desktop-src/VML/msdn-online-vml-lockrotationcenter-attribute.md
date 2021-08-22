---
title: Attributo VML LockRotationCenter
description: Attributo VML LockRotationCenter
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ef0cfee24998cfa343265569274ace688a05f90a270b721317394e59589a51e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598059"
---
# <a name="vml-lockrotationcenter-attribute"></a>Attributo VML LockRotationCenter

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se la rotazione dell'oggetto estruso viene specificata [dall'attributo RotationAngle.](msdn-online-vml-rotationangle-attribute.md) Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Estrusione](msdn-online-vml-extrusion-element.md)

**Sintassi dei tag**

<o: *elemento* lockrotationcenter=" *espressione* ">

**Sintassi dello script**

*element* .lockrotationcenter="*expression*"

*expression* = *elemento*.lockrotationcenter

**Osservazioni:**

Se **False**, la rotazione viene specificata dall'attributo [Orientation.](msdn-online-vml-orientation-attribute.md) Il valore predefinito è **True**.

Tenere presente quanto segue:


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



è lo stesso di:


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



*Microsoft Office Attributo Extensions*

 

 