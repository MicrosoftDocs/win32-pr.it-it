---
title: Attributo LockRotationCenter di la
description: Attributo LockRotationCenter di la
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49dd6ccada3f713f1cf2384a96f131c9a7714db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300320"
---
# <a name="vml-lockrotationcenter-attribute"></a>Attributo LockRotationCenter di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se la rotazione dell'oggetto estruso è specificata dall'attributo [RotationAngle](msdn-online-vml-rotationangle-attribute.md) . Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Estrusione](msdn-online-vml-extrusion-element.md)

**Sintassi Tag**

<o: *element* lockrotationcenter = " *Expression* " >

**Sintassi dello script**

*element* . lockrotationcenter = "*Expression*"

*espressione* = *elemento*. lockrotationcenter

**Osservazioni:**

Se **false**, la rotazione viene specificata dall'attributo [Orientation](msdn-online-vml-orientation-attribute.md) . Il valore predefinito è **True**.

Tenere presente quanto segue:


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



è lo stesso di:


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



*Attributo Microsoft Office Extensions*

 

 