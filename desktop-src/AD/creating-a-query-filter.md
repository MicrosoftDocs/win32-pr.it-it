---
title: Creazione di un filtro query
description: Un filtro di query indica Active Directory Domain Services per trovare i dati in una sintassi di query LDAP. Tutte le tecnologie di accesso ai dati specificate elencate nell'argomento scelta della tecnologia di ricerca supportano la sintassi delle query LDAP.
ms.assetid: 0bd652f0-41a6-4a0d-8742-9d6a2a7f168a
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, creazione di un filtro di query
- filtri query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e0a4e4a02312fcc9affb681407044ba0d8e18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855202"
---
# <a name="creating-a-query-filter"></a>Creazione di un filtro query

Un filtro di query indica Active Directory Domain Services per trovare i dati in una sintassi di query LDAP. Tutte le tecnologie di accesso ai dati specificate elencate nell'argomento [scelta della tecnologia di ricerca](choosing-the-search-technology.md) supportano la sintassi delle query LDAP.

La sintassi della query LDAP è la seguente:


```C++
<expression><expression>...
```



Un filtro può contenere una o più espressioni. Un'espressione ha il formato seguente:


```C++
(<logicaloperator><comparison><comparison...>)
```



dove " &lt; LogicalOperator &gt; " è uno dei seguenti.



| Operatore        | Descrizione                |
|-----------------|----------------------------|
| "\|"<br/> | **Or** logico<br/>  |
| "&"<br/>  | **And** logico<br/> |
| "!"<br/>  | **Not** logico<br/> |



 

e &lt; il "confronto &gt; " è il seguente:


```C++
(<attribute><operator><value>)
```



dove " &lt; Attribute &gt; " è l' **ldapDisplayName** dell'attributo da valutare, " &lt; value &gt; " è il valore da confrontare e " &lt; Operator &gt; " è uno degli operatori di confronto seguenti.



| Operatore           | Descrizione                         |
|--------------------|-------------------------------------|
| "="<br/>     | Uguale a<br/>                   |
| "~="<br/>    | Approssimativamente uguale a<br/>     |
| "<="<br/> | Minore o uguale a<br/>    |
| ">="<br/> | Maggiore o uguale a<br/> |



 

Inoltre, a seconda della sintassi dell'attributo, il " &lt; valore &gt; " può contenere il carattere jolly (" \* "). Un " &lt; valore &gt; " che contiene solo un carattere jolly verificherà l'esistenza di qualsiasi valore in " &lt; Attribute &gt; ". Se non è impostato alcun valore per " &lt; Attribute &gt; ", il test avrà esito negativo.

Se uno dei seguenti caratteri speciali deve essere visualizzato nel filtro della query come valori letterali, è necessario sostituirli con la sequenza di escape elencata.



| Carattere ASCII    | Sostituzione sequenza di escape |
|--------------------|----------------------------|
| \*<br/>      | " \\ 2a"<br/>          |
| (<br/>       | " \\ 28"<br/>          |
| )<br/>       | " \\ 29"<br/>          |
| \\<br/>      | " \\ 5C"<br/>          |
| **NUL**<br/> | " \\ 00"<br/>          |



 

Inoltre, i dati binari arbitrari possono essere rappresentati utilizzando la sintassi della sequenza di escape codificando ogni byte di dati binari con la barra rovesciata seguita da due cifre esadecimali. Ad esempio, il valore a quattro byte 0x00000004 è codificato come " \\ 00 \\ 00 \\ 00 \\ 04" in una stringa di filtro.

## <a name="examples"></a>Esempio

Nella stringa di query seguente vengono cercati tutti gli oggetti di tipo "computer".


```C++
(objectCategory=computer)
```



Nella stringa di query seguente vengono cercati tutti gli oggetti di tipo "computer" con un nome che inizia con "desktop".


```C++
(&(objectCategory=computer)(name=desktop*))
```



Nella stringa di query seguente vengono cercati tutti gli oggetti di tipo "computer" con un nome che inizia con "desktop" o un nome che inizia con "notebook".


```C++
(&(objectCategory=computer)(|(name=desktop*)(name=notebook*)))
```



La stringa di query seguente Cerca tutti gli oggetti di tipo "User" con un numero di telefono dell'abitazione.


```C++
(&(objectCategory=user)(homePhone=*))
```



Per ulteriori informazioni sulle stringhe di filtro della query e sugli esempi di utilizzo, vedere:

-   [Ricerca di oggetti per classe](finding-objects-by-class.md)
-   [Ricerca di oggetti in base al nome](finding-objects-by-name.md)
-   [Ricerca di un elenco di attributi su cui eseguire una query](finding-a-list-of-attributes-to-query.md)
-   [Verifica della sintassi del filtro query](checking-the-query-filter-syntax.md)
-   [Come specificare i valori di confronto](how-to-specify-comparison-values.md)

 

 





