---
title: Tipo di dati VML IVgAdjustments
description: Tipo di dati VML IVgAdjustments
ms.assetid: d605632b-3ee2-44fd-8122-f38b1f91e965
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed6512e36e9621d010e8875eec3190fa81524b4947a30f14364199341d18c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599679"
---
# <a name="vml-ivgadjustments-data-type"></a>Tipo di dati VML IVgAdjustments

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Raccolta di modifiche a una forma che può essere usata nelle formule. Le rettifiche possono essere usate come segnaposto temporanei o per qualsiasi motivo si usino le variabili. Nella raccolta sono presenti solo 8 modifiche.



| Attributi | Descrizione                                                                                                                                                                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Length     | **Integer**. Numero di modifiche. Non può essere maggiore di 8.                                                                                                                                                                                                                                                                          |
| Elemento       | **Long**. Matrice di rettifiche indicizzate da 0 a 7. Si noti che le modifiche possono essere specificate con parsimonio. in altri, i valori intermedi delle matrici potrebbero non essere sempre riempiti. Ad esempio, l'elemento 1, 3 e 5 può avere valori per una lunghezza pari a 3, con item(0), item(2) e item(4) specificati. Per verificare se esiste un elemento, usare l'attributo Exists. |
| Exists     | **IVgTriState**. Determina se esiste una rettifica specificata. Si noti che è necessario usare un indice. ovvero exists(item) deve essere usato per recuperare l'esistenza di un elemento.                                                                                                                                                           |
| Valore      | **Stringa**. Rappresentazione testuale dei valori numerici, con virgole tra ogni numero.                                                                                                                                                                                                                                                    |



 

 

 