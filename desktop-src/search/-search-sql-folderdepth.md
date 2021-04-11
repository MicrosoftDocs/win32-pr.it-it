---
description: I predicati di profondità della cartella controllano l'ambito di una ricerca specificando un percorso e se eseguire un attraversamento profondo o superficiale.
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: Predicati di ambito e DIRECTORY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2418b2149a5bf05bd000460c787b7f967856c5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128547"
---
# <a name="scope-and-directory-predicates"></a>Predicati di ambito e DIRECTORY

I predicati di profondità della cartella controllano l'ambito di una ricerca specificando un percorso e se eseguire un attraversamento profondo o superficiale. Di seguito viene illustrata la sintassi dei predicati di profondità della cartella:


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



Il predicato è seguito da un segno di uguale. Il percorso è exclosed tra virgolette singole e deve iniziare con un protocollo e due punti (ad esempio,, `file:` `mapi:` o `csc:` ). Il predicato di ambito esegue un attraversamento profondo del percorso, incluse tutte le sottocartelle, mentre il predicato di DIRECTORY esegue un attraversamento superficiale della sola cartella specificata. Analogamente ad altre restrizioni di Structured Query Language (SQL), è possibile specificare più di una restrizione di profondità di cartella in una singola query.

Per eseguire una query sul catalogo locale di un computer remoto, includere il nome del computer prima del catalogo e un percorso di Universal Naming Convention (UNC) nel computer remoto nella clausola SCOPE o DIRECTORY.

## <a name="examples"></a>Esempio


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



Nell'esempio primo ambito viene eseguita la ricerca \\ nella \\ cartella report C: files e in tutte le relative sottocartelle. L'esempio di DIRECTORY Cerca solo i report cartella radice C: \\ file \\ .

> [!Note]  
> Le barre rovesciate file system ( \\ ) diventano una barra di tipo URL (talvolta denominate barre) (/).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Clausola FROM](-search-sql-from.md)
</dt> <dt>

[Clausola WHERE](-search-sql-where.md)
</dt> </dl>

 

 



