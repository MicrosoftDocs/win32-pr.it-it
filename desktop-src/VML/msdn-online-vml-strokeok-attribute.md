---
title: Attributo StrokeOK di VML
description: Attributo StrokeOK di VML
ms.assetid: f150f87b-1ed9-4c53-bf7f-ebe1e81642fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5051f3a2d5e7ac8e4d509d8b8f65182f86799db41bbd8a4d71741961c3a1e406
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475221"
---
# <a name="vml-strokeok-attribute"></a>Attributo StrokeOK di VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se verrà visualizzato un tratto. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi dei tag**

<v: *elemento* strokeok=" *espressione* ">

**Sintassi dello script**

*element* .strokeok="*expression*"

*expression* = *elemento*.strokeok

**Osservazioni:**

Se **False,** il percorso non può essere tracciato. Il valore predefinito è **True**. Questo attributo esegue l'override di tutti gli altri attributi del tratto nell'elemento padre o **Stroke.**

*Attributo standard VML*

**Esempio**

Il tracciato non verrà tracciato.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" strokeok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 