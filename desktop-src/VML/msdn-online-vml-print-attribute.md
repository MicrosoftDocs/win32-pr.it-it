---
title: Attributo di stampa la
description: Attributo di stampa la
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55925621ab56f011c998f3feac21a892a4d7ea66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299900"
---
# <a name="vml-print-attribute"></a>Attributo di stampa la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se la forma verrà stampata. Proprietà di lettura/scrittura. [VgTriState](msdn-online-vml-vgtristate.md).

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* Print = " *Expression* " >

**Sintassi dello script**

*element* . Print = "*Expression*"

*espressione* = *elemento*. Print

**Osservazioni:**

Fornito come metodo per specificare se verranno stampate forme. Si noti che è comunque possibile visualizzare una forma sullo schermo, anche se non viene stampata come risultato di questo attributo **false**. Il valore predefinito è **True**.

Questo attributo viene utilizzato da Microsoft Office ma non viene utilizzato da Microsoft Internet Explorer.

*Attributo Microsoft Office Extensions*

 

 