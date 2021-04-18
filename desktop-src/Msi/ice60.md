---
description: ICE60 convalida la tabella file di un database Windows Installer.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26c6f296fd514f582a699a5f839a7e145169e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314794"
---
# <a name="ice60"></a>ICE60

ICE60 verifica che i file nella [tabella file](file-table.md) soddisfino la condizione seguente:

-   Se il file non è un tipo di carattere e presenta una versione, è necessario che disponga di una lingua.
-   ICE60 verifica che non siano elencati file con versione nella [tabella MsiFileHash](msifilehash-table.md).

Se si verifica un errore durante la correzione di un avviso segnalato da ICE60, in genere il file viene reinstallato inutilmente quando viene eseguito un ripristino del prodotto. Questo problema si verifica perché il file da installare nel ripristino e il file esistente sul disco hanno la stessa versione (si tratta dello stesso file) ma linguaggi diversi. La tabella file elenca la lingua come null, ma il file ha un valore di lingua nella risorsa. In base alle [regole di controllo delle versioni dei file](file-versioning-rules.md), il programma di installazione predilige il file da installare, quindi viene ricopiato inutilmente.

## <a name="result"></a>Risultato

ICE60 Invia un avviso o un errore se un file nella [tabella file](file-table.md) che non è un tipo di carattere e ha una versione, non dispone di un linguaggio.

ICE60 invia il seguente errore se un file elencato nella tabella MsiFileHash è sottoposto a controllo delle versioni.

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a>Esempio

ICE60 segnala l'errore e l'avviso seguenti per l'esempio illustrato. Il file B è un tipo di carattere. gli altri file non lo sono.

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

Filea ha una versione e un linguaggio; pertanto non viene generato alcun avviso o errore.

FileB dispone di una versione ma non di un linguaggio. Tuttavia, non viene generato alcun avviso o errore perché è un tipo di carattere.

FileC è un riferimento complementare, pertanto non è necessario disporre di un linguaggio. Non viene generato alcun avviso o errore.

Il file archiviato non ha una versione, quindi non è necessario disporre di un linguaggio. Non viene generato alcun avviso o errore.

Il file ha una versione ma nessuna lingua. Viene pertanto generato un avviso.

Per correggere il problema, aggiungere una lingua al file.

I file devono avere i valori della lingua archiviati nella risorsa di versione laddove possibile. Se un file è indipendente dalla lingua, usare [LangID](column-data-types.md) 0.

[File table](file-table.md) (fileB è un tipo di carattere; gli altri file non lo sono).



| File  | Versione | Linguaggio |
|-------|---------|----------|
| FileA | 1.0     | 1033     |
| FileB | 1.0     |          |
| FileC | FileA   |          |
| Campo |         |          |
| File | 1.0     |          |



 

[Tabella dei tipi di carattere](font-table.md)



| File  | FontTitle  |
|-------|------------|
| FileB | Titolo carattere |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



