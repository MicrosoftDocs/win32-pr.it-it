---
title: Attributo VML InvX
description: Attributo VML InvX
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e040c4ff013ec9c2a606e1034458f9149d666813dd42341d9ec68a39901094b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600127"
---
# <a name="vml-invx-attribute"></a>Attributo VML InvX

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se la posizione x dell'handle è invertita. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[H](msdn-online-vml-h-element.md) (sottoelemento [di Handle](msdn-online-vml-handles-element.md))

**Sintassi dei tag**

<v: *element* invx=" *expression* ">

**Osservazioni:**

Se **True,** la posizione x dell'handle viene invertita sottraendo il valore x dal valore x di **CoordOrigin** aggiunto al valore x di **CoordSize**. Il valore predefinito è **False**.

Questo attributo è l'equivalente di

coordorigin.x + coordsize.x - h.position.x

*Attributo standard VML*

 

 