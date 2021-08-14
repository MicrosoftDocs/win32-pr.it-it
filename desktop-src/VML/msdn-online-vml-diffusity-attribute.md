---
title: Attributo di diffusione VML
description: Attributo di diffusione VML
ms.assetid: 1d131540-9166-47fc-bb0d-fada38f6a3de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b311c70e1cf49ece7f0072d70b07e886d11f0fe9122fc5d248a32f4321ba19b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754738"
---
# <a name="vml-diffusity-attribute"></a>Attributo di diffusione VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce la quantità di diffusione della luce riflessa da una forma estruso. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[Estrusione](msdn-online-vml-extrusion-element.md)

**Sintassi dei tag**

<o: *element* diffusity=" *expression* ">

**Sintassi dello script**

*element* .diffusity="*expression*"

*expression* = *elemento*.diffusity

**Osservazioni:**

Questo valore definisce il rapporto tra la luce dell'evento imprevisto e la luce riflessa diffusa. I valori normali sono da 0 a 1. Il valore predefinito è 0.

Se vengono specificati valori maggiori di 1, possono verificarsi effetti insoliti.

*Microsoft Office Attributo Extensions*

 

 