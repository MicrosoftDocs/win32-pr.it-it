---
title: Attributo VML nascosto
description: Attributo VML nascosto
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9122b3a9828fde816684cb20035949628ef25e38d06fb188d8271f0d5384f1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308281"
---
# <a name="vml-obscured-attribute"></a>Attributo VML nascosto

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se un'ombreggiatura è trasparente. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi dei tag**

<v: *element* obscured=" *expression* ">

**Sintassi dello script**

*elemento* .obscured="*expression*"

*expression* = *elemento*.obscured

**Osservazioni:**

Se **True**, consente di visualizzare attraverso l'ombreggiatura se non è presente alcun riempimento sulla forma. L'impostazione predefinita è **False**.

*Attributo standard VML*

**Esempio**

Lo sfondo viene visualizzato tramite l'ombreggiatura.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" obscured="True"/>
   </v:shape>
```



 

 