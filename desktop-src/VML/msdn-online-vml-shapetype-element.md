---
title: Elemento ShapeType VML
description: Elemento ShapeType VML
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0632919a141ae04f80b0b6cd6782ea907aa8cfe1d720e599964110c038f3998e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099091"
---
# <a name="vml-shapetype-element"></a>Elemento ShapeType VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce una forma che può essere usata per creare altre forme.

L'attributo seguente modifica **un oggetto ShapeType**.



| Attributo                                      | Descrizione                                             |
|------------------------------------------------|---------------------------------------------------------|
| [Master](msdn-online-vml-master-attribute.md) | Determina se **shapeType** è un elemento master. |



 

**Osservazioni:**

**ShapeType è** identico **all'elemento Shape,** ma non può fare riferimento a un **altro elemento ShapeType.**

Quando un **elemento Shape** fa riferimento a un **oggetto ShapeType,** **Shape** può duplicare alcune delle proprietà già specificate in **ShapeType.** In questi casi, gli attributi in **Shape** eseguono l'override di quelli di **ShapeType**.

**L'attributo Type** non può essere usato con **ShapeType.**

Gli attributi di posizionamento CSS (ad esempio **Top,** **Left** e così via) non vengono passati a **un oggetto Shape** da un oggetto **ShapeType.**

Per usare questo elemento, creare un **oggetto ShapeType** con un [attributo ID](id-attribute--vml.md) specifico. Creare quindi un **oggetto Shape** e fare riferimento **a ShapeType** con l'attributo **Type.** Per altre [informazioni, vedere l'attributo](type-attribute--shape--vml.md) Type.

 

 