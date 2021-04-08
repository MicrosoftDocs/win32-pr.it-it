---
title: Attributo AltHRef (ImageData) (la)
description: Attributo AltHRef (ImageData) (la)
ms.assetid: c55ede90-3d57-4f27-9940-1fe4751cef71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004625d769c12e67de024bf537ee04c377a18c8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046930"
---
# <a name="althref-attribute-imagedatavml"></a>Attributo AltHRef (ImageData) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica un riferimento alternativo per un'immagine. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi Tag**

<v: *element* o:althref = " *Expression* " >

**Sintassi dello script**

*element* . althref = "*Expression*"

*espressione* = *elemento*. althref

**Osservazioni:**

Supporta la conservazione dei dati PICT tramite Roundtripping HTML. Nella scrittura HTML la rappresentazione alternativa, ovvero i dati PICT originali se il file proviene da Macintosh, viene salvata. In una lettura HTML, **AltHRef** è favorito tramite **src**.

*Attributo Microsoft Office Extensions*

 

 