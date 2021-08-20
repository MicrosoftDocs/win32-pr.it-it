---
title: Attributo di stampa VML
description: Attributo di stampa VML
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfa364e573d887da2013f946ddf23e0a974e0f63211623de3d2046b0525b2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057729"
---
# <a name="vml-print-attribute"></a>Attributo di stampa VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se la forma verrà stampata. Proprietà di lettura/scrittura. [VgTriState](msdn-online-vml-vgtristate.md).

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* print=" *expression* ">

**Sintassi dello script**

*elemento* .print="*expression*"

*expression* = *elemento*.print

**Osservazioni:**

Fornito come modo per specificare se le forme verranno stampate. Si noti che una forma può comunque essere visualizzata sullo schermo, anche se non viene stampata come risultato del fatto che questo attributo è **False.** Il valore predefinito è **True**.

Questo attributo viene usato da Microsoft Office ma non da Microsoft Internet Explorer.

*Microsoft Office Attributo Extensions*

 

 