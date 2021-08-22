---
title: Attributo VML MSO-Wrap-Mode
description: Attributo VML MSO-Wrap-Mode
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e3743522b9286da8a7f30e9100e06205430b1b18fa3c62def60b57f54b65d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136984"
---
# <a name="vml-mso-wrap-mode-attribute"></a>Attributo VML MSO-Wrap-Mode

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la modalità di ritorno a capo per il testo. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* style="mso-wrap-mode: *expression* ">

**Osservazioni:**

I possibili valori sono:



| Valore          | Descrizione                          |
|----------------|--------------------------------------|
| square         | Racchiude il testo intorno alla forma in un quadrato. |
| Stretto          | Il testo viene racchiuso in un punto vicino alla forma.  |
| in alto e in basso | Il testo passa dall'alto verso il basso.       |
| -        | Il testo viene visualizzato attraverso la forma.     |
| Nessuno           | Il testo non va a capo.                   |



 

Usato da Microsoft PowerPoint salvataggio in HTML per indicare se il ritorno a capo automatico all'interno di una forma è on (**square**) o off (**none**).

*Microsoft Office Attributo Extensions*

**Esempio**

Il codice seguente indica che il ritorno a capo automatico all'interno di una forma è attivato in PowerPoint.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 