---
description: I predicati di profondità della cartella controllano l'ambito di una ricerca specificando un percorso e se eseguire un attraversamento profondo o superficiale.
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: Predicati SCOPE e DIRECTORY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f221ba4048f1ab7f5096321cc00aed209acb5ca3e5616e6e6a4fbbc516dfc28b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462470"
---
# <a name="scope-and-directory-predicates"></a>Predicati SCOPE e DIRECTORY

I predicati di profondità della cartella controllano l'ambito di una ricerca specificando un percorso e se eseguire un attraversamento profondo o superficiale. Di seguito viene illustrata la sintassi dei predicati di profondità della cartella:


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



Il predicato è seguito da un segno di uguale. Il percorso viene chiuso tra virgolette singole e deve iniziare con un protocollo e i due punti (ad esempio, `file:` `mapi:` , o `csc:` ). Il predicato SCOPE esegue un attraversamento completo del percorso, incluse tutte le sottocartelle, mentre il predicato DIRECTORY esegue un attraversamento superficiale solo della cartella specificata. Analogamente ad Structured Query Language restrizioni (SQL), è possibile specificare più restrizioni di profondità della cartella in una singola query.

Per eseguire una query sul catalogo locale di un computer remoto, includere il nome del computer prima del catalogo e un percorso Universal Naming Convention (UNC) nel computer remoto nella clausola SCOPE o DIRECTORY.

## <a name="examples"></a>Esempio


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



Il primo esempio scope cerca nella cartella C: \\ Files Reports e in tutte le relative \\ sottocartelle. Nell'esempio DIRECTORY viene eseguita la ricerca solo nella cartella radice C: \\ Files \\ Reports.

> [!Note]  
> Le file system barre rovesciate ( ) diventano barre di tipo URL (talvolta denominate \\ barre) (/).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Clausola FROM](-search-sql-from.md)
</dt> <dt>

[Clausola WHERE](-search-sql-where.md)
</dt> </dl>

 

 



