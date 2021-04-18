---
description: Descrive l'istruzione SELECT per una query di dati.
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: Istruzione SELECT per le query di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06905cfd9ef5e55022b3fc2275ed705a670a0ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309883"
---
# <a name="select-statement-for-data-queries"></a>Istruzione SELECT per le query di dati

È possibile utilizzare un'ampia gamma di istruzioni SELECT per eseguire una query per ottenere informazioni. Le istruzioni possono essere istruzioni di base oppure possono essere più restrittive per limitare il set di risultati restituito dalla query.

L'esempio seguente è un'istruzione SELECT di base utilizzata per eseguire una query per i dati.


```sql
SELECT * FROM Class
```



Questa istruzione restituisce le istanze della classe specificata e delle relative sottoclassi. Sono incluse tutte le proprietà di sistema e definite dall'utente per le classi. Se una proprietà di sistema non è pertinente per una determinata query, contiene **null**.

È possibile utilizzare diverse tecniche per ridurre la larghezza di banda necessaria per recuperare il set di risultati, se l'esecuzione della query comporta un sovraccarico eccessivo e l'utente è interessato solo a un sottoinsieme delle proprietà. In primo luogo, le query possono sostituire l'asterisco con le proprietà desiderate.

Nell'esempio seguente viene illustrato come eseguire una query per proprietà specifiche.


```sql
SELECT property_1, property_2, property_3 FROM class
```



Il set di risultati include tutte le proprietà di sistema e le proprietà non di sistema specificate.

Un'altra tecnica per limitare l'ambito del set di risultati di una query consiste nell'usare la proprietà di sistema della [**\_ \_ classe**](wmi-system-properties.md) . Per impostazione predefinita, le query restituiscono tutte le istanze della classe specificata e delle relative sottoclassi. È possibile utilizzare la proprietà di sistema della **\_ \_ classe** per richiedere solo istanze della classe specificata, escluse le sottoclassi.

Nell'esempio seguente viene illustrato come utilizzare la proprietà di sistema della [**\_ \_ classe**](wmi-system-properties.md) in una clausola WHERE.


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



È inoltre possibile utilizzare la proprietà di sistema della [**\_ \_ classe**](wmi-system-properties.md) per limitare il set di risultati a istanze di sottoclassi specifiche.

Nell'esempio seguente viene illustrato come limitare il set di risultati a istanze di sottoclassi specifiche.


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> Se si crea una query con un percorso non valido per un oggetto incorporato, la query non restituisce un errore o i risultati.

 

Nell'esempio seguente viene restituita un'istanza di **MainClass**, supponendo che esista un'istanza di **MainClass** contenente l'oggetto incorporato **EmbedObj** con una proprietà **P \_ UInt32** uguale a "70011".


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



Nell'esempio seguente non viene restituito alcun risultato e non viene restituito un errore, a condizione che l'oggetto incorporato **EmbedObj** nell'istanza di **MainClass** non disponga di una proprietà non **valida**.


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



