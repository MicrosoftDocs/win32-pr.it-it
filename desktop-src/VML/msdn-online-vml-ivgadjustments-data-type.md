---
title: Tipo di dati la IVgAdjustments
description: Tipo di dati la IVgAdjustments
ms.assetid: d605632b-3ee2-44fd-8122-f38b1f91e965
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29f85f93218db098ca247fa66b1f493e9c622a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473435"
---
# <a name="vml-ivgadjustments-data-type"></a>Tipo di dati la IVgAdjustments

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Raccolta di modifiche a una forma che può essere utilizzata nelle formule. Le regolazioni possono essere utilizzate come segnaposti temporanei o per qualsiasi motivo per cui si utilizzano le variabili. Sono presenti solo 8 modifiche nella raccolta.



| Attributi | Descrizione                                                                                                                                                                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Length     | **Integer**. Numero di rettifiche. Non può essere maggiore di 8.                                                                                                                                                                                                                                                                          |
| Elemento       | **Long**. Matrice di regolazioni indicizzate da 0 a 7. Si noti che le regolazioni possono essere specificate in SPARC; ovvero i valori della matrice intermedia potrebbero non essere sempre compilati. Ad esempio, Item 1, 3 e 5 possono avere valori per una lunghezza di 3, con Item (0), Item (2) e Item (4) specificati. Per verificare se esiste un elemento, usare l'attributo exists. |
| Exists     | **IVgTriState**. Determina se esiste una rettifica specificata. Si noti che è necessario utilizzare un indice. ovvero è necessario utilizzare EXISTS (item) per recuperare l'esistenza di un elemento.                                                                                                                                                           |
| Valore      | **Stringa**. Rappresentazione testuale dei valori numerici, con virgole tra ogni numero.                                                                                                                                                                                                                                                    |



 

 

 