---
title: Attributo TableLimits di VML
description: Attributo TableLimits di VML
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af52ba570b04e56f1dede169045f7ee1addf374fae5ca4f1cd5de4d9390f1235
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959251"
---
# <a name="vml-tablelimits-attribute"></a>Attributo TableLimits di VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Elenco dei valori di altezza minima per ogni riga di una tabella. Proprietà di lettura/scrittura. **VgLengthArray**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* o:tablelimits=" *expression* ">

**Osservazioni:**

Usato da Microsoft PowerPoint per le tabelle native. Il valore predefinito è **Null.**

Anche se il valore è archiviato in una forma, l'attributo è utile solo quando la tabella è composta da forme raggruppate. Quando il testo viene aggiunto alle celle della tabella, l'altezza della riga può aumentare. **L'attributo TableLimits** archivia l'altezza della riga originale in modo che, se il testo viene eliminato, l'altezza della riga non cada al di sotto del valore originale.

*Microsoft Office Attributo Extensions*

 

 