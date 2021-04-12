---
title: Elemento TipoForma di la
description: Elemento TipoForma di la
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbb35eef0a3c987fe1e6ec35d15701236ae0af1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223925"
---
# <a name="vml-shapetype-element"></a>Elemento TipoForma di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce una forma che può essere utilizzata per creare altre forme.

L'attributo seguente modifica un **TipoForma**.



| Attributo                                      | Descrizione                                             |
|------------------------------------------------|---------------------------------------------------------|
| [Master](msdn-online-vml-master-attribute.md) | Determina se un **TipoForma** è un elemento Master. |



 

**Osservazioni:**

**TipoForma** è identico all'elemento **Shape** con la differenza che non può fare riferimento a un altro elemento **TipoForma** .

Quando un elemento **Shape** fa riferimento a un **TipoForma**, la **forma** può duplicare alcune delle proprietà che sono già state specificate in **TipoForma**. In questi casi, gli attributi nella **forma** eseguono l'override di quelli di **TipoForma**.

L'attributo **Type** non può essere utilizzato con **TipoForma**.

Gli attributi di posizionamento CSS (ad esempio **Top**, **Left** e così via) non vengono passati a una **forma** da un **TipoForma**.

Per usare questo elemento, creare un **TipoForma** con un attributo [ID](id-attribute--vml.md) specifico. Creare quindi una **forma** e fare riferimento a **TipoForma** con l'attributo **Type** . Per ulteriori informazioni, vedere l'attributo [Type](type-attribute--shape--vml.md) .

 

 