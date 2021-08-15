---
title: Attributo VML ViewpointOrigin
description: Attributo VML ViewpointOrigin
ms.assetid: 4ccb3e12-bae4-4cb2-b48b-80c155ae7e03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5e69357eddfe535b3c6164579454260d8f478430f7a9f1c7bede3262b1b040
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007561"
---
# <a name="vml-viewpointorigin-attribute"></a>Attributo VML ViewpointOrigin

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce l'origine del punto di vista all'interno del rettangolo di selezione della forma. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Estrusione](msdn-online-vml-extrusion-element.md)

**Sintassi dei tag**

<o: *elemento* viewpointorigin=" *espressione* ">

**Sintassi dello script**

*element* .viewpointorigin="*expression*"

*expression* = *elemento*.viewpointorigin

**Osservazioni:**

Definisce il punto di vista in termini di valori x e y della forma originale. I valori x e y vanno da 0,5 a -0,5 (dal 50% al -50% dell'origine delle coordinate della forma). Il valore predefinito è 0,0.

*Microsoft Office Attributo Extensions*

 

 