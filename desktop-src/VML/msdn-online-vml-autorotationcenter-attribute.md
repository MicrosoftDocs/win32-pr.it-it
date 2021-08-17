---
title: Attributo VML AutoRotationCenter
description: Attributo VML AutoRotationCenter
ms.assetid: beb6771f-42f4-458a-b525-4eb67bc1eff0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54b363b34a6b2f943be45d457e252eebcf597afd7f82b7992cf151b0c2eda4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347103"
---
# <a name="vml-autorotationcenter-attribute"></a>Attributo VML AutoRotationCenter

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se il centro di rotazione sarà il centro geometrico dell'estrusione. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Estrusione](msdn-online-vml-extrusion-element.md)

**Sintassi dei tag**

<o: *elemento* autorotationcenter=" *espressione* ">

**Sintassi dello script**

*element* .autorotationcenter="*expression*"

*expression* = *elemento*.autorotationcenter

**Osservazioni:**

Il centro geometrico di una forma estruso è 0,0,0. Se il valore di questo attributo è **False**, il centro di rotazione è determinato dall'attributo [RotationCenter.](msdn-online-vml-rotationcenter-attribute.md) Il valore predefinito è **False**.

*Microsoft Office Attributo Extensions*

 

 