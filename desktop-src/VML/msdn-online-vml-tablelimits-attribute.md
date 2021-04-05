---
title: Attributo TableLimits di la
description: Attributo TableLimits di la
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b35a7449cc2f348e6040161c1fb599c29972803
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727578"
---
# <a name="vml-tablelimits-attribute"></a>Attributo TableLimits di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Elenco di valori di altezza minima per ogni riga di una tabella. Proprietà di lettura/scrittura. **VgLengthArray**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* o:tablelimits = " *Expression* " >

**Osservazioni:**

Usato da Microsoft PowerPoint per le tabelle native. Il valore predefinito è **null**.

Anche se il valore viene archiviato in una forma, l'attributo è utile solo quando la tabella è costituita da forme raggruppate. Quando si aggiunge un testo alle celle della tabella, è possibile che l'altezza della riga aumenti. L'attributo **TableLimits** archivia l'altezza della riga originale in modo che, se il testo viene eliminato, l'altezza della riga non scenderà al di sotto del valore originale.

*Attributo Microsoft Office Extensions*

 

 