---
description: Descrivere l'istruzione SELECT per una query di dati.
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: Istruzione SELECT per query di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fec0526c5e5d47a74d6e165726222f9e521bd7102072e5a4b79e960f8dae19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315949"
---
# <a name="select-statement-for-data-queries"></a>Istruzione SELECT per query di dati

È possibile utilizzare un'ampia gamma di istruzioni SELECT per eseguire query per ottenere informazioni. Le istruzioni possono essere istruzioni di base o più restrittive per limitare il set di risultati restituito dalla query.

L'esempio seguente è un'istruzione SELECT di base usata per eseguire query sui dati.


```sql
SELECT * FROM Class
```



Questa istruzione restituisce istanze della classe specificata e di una delle relative sottoclassi. Sono incluse tutte le proprietà di sistema e definite dall'utente per le classi. Se una proprietà di sistema non è pertinente per una determinata query, contiene **NULL.**

È possibile usare diverse tecniche per ridurre la larghezza di banda necessaria per recuperare il set di risultati, se l'esecuzione della query comporta un sovraccarico troppo alto e l'utente è interessato solo a un subset delle proprietà. In primo luogo, le query possono sostituire l'asterisco con le proprietà desiderate.

Nell'esempio seguente viene illustrato come eseguire una query per proprietà specifiche.


```sql
SELECT property_1, property_2, property_3 FROM class
```



Il set di risultati include tutte le proprietà di sistema e le proprietà non di sistema specificate.

Un'altra tecnica per restringere l'ambito del set di risultati di una query consiste nell'usare la proprietà di sistema [**\_ \_ CLASS.**](wmi-system-properties.md) Per impostazione predefinita, le query restituiscono tutte le istanze della classe specificata e delle relative sottoclassi. È possibile usare la **\_ \_ proprietà di** sistema CLASS per richiedere solo istanze della classe specificata, escluse le relative sottoclassi.

Nell'esempio seguente viene illustrato come utilizzare la [**\_ \_ proprietà di**](wmi-system-properties.md) sistema CLASS in una clausola WHERE.


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



È anche possibile usare la [**\_ \_ proprietà di**](wmi-system-properties.md) sistema CLASS per limitare il set di risultati a istanze di sottoclassi specifiche.

Nell'esempio seguente viene illustrato come limitare il set di risultati a istanze di sottoclassi specifiche.


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> Se si crea una query con un percorso non valido per un oggetto incorporato, la query non restituisce un errore o alcun risultato.

 

Nell'esempio seguente viene restituita un'istanza di **MainClass**, presupponendo che esista un'istanza di **MainClass** contenente l'oggetto **incorporato EmbedObj** con una proprietà **P \_ Uint32** uguale a "70011".


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



Nell'esempio seguente non viene restituito alcun risultato e non viene restituito un errore, presupponendo che l'oggetto incorporato **EmbedObj** nell'istanza di **MainClass** non abbia una proprietà **INVALID**.


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



