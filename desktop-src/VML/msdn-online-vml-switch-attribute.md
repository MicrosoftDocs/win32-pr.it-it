---
title: Attributo del commutatore VML
description: Attributo del commutatore VML
ms.assetid: fc099c0a-6789-41e8-ab08-36f4fd2d3bfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db2205f83449b09c22314c81ed460bee8410a3873e8f5550c073d7f3a1c1e8c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123893"
---
# <a name="vml-switch-attribute"></a>Attributo del commutatore VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se le direzioni dell'handle vengono scambiate. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[H](msdn-online-vml-h-element.md) (sottoelemento di [Handle](msdn-online-vml-handles-element.md))

**Sintassi dei tag**

<v: *element* switch=" *expression* ">

**Osservazioni:**

Se **True,** l'handle viene alternato tra le direzioni x e y se la forma è più alta di quella larga. Il valore predefinito è **False**.

Questo attributo viene usato per le forme con comportamento di estensione delle limousine.

*Attributo VML Standard*

 

 