---
description: ICE60 convalida la tabella File di un database Windows Installer.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce8d2cbf9136ea6195a138c586d4408dc0d2e5ff411b52fd73fec8a569c5d186
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044031"
---
# <a name="ice60"></a>ICE60

ICE60 verifica che i file nella tabella File soddisfino la condizione seguente: [](file-table.md)

-   Se il file non è un tipo di carattere e ha una versione, deve avere una lingua.
-   ICE60 verifica che nessun file con versione sia elencato nella [tabella MsiFileHash](msifilehash-table.md).

La mancata correzione di un avviso segnalato da ICE60 comporta in genere la reinstallazione non necessaria di un file al termine di un ripristino del prodotto. Ciò si verifica perché il file da installare nel ripristino e il file esistente su disco hanno la stessa versione (sono lo stesso file) ma lingue diverse. La tabella file elenca la lingua come Null, ma il file stesso ha un valore di lingua nella risorsa. In base alle [regole di controllo delle](file-versioning-rules.md)versioni dei file , il programma di installazione favorisce l'installazione del file, quindi viene ricopiato in modo non necessario.

## <a name="result"></a>Risultato

ICE60 invia un avviso o un errore se un file nella tabella [File](file-table.md) che non è un tipo di carattere e ha una versione, non ha una lingua.

ICE60 pubblica l'errore seguente se un file elencato nella tabella MsiFileHash ha il controllo delle versioni.

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a>Esempio

ICE60 segnala l'errore e l'avviso seguenti per l'esempio illustrato. Il file B è un tipo di carattere, gli altri file no.

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

FileA ha sia una versione che una lingua. pertanto non viene generato alcun avviso o errore.

FileB ha una versione ma non un linguaggio. Non viene tuttavia generato alcun avviso o errore perché si tratta di un tipo di carattere.

FileC è un riferimento complementare, pertanto non deve avere un linguaggio. Non viene generato alcun avviso o errore.

FileD non ha una versione, quindi non deve avere una lingua. Non viene generato alcun avviso o errore.

FileE ha una versione ma non un linguaggio. Viene pertanto generato un avviso.

Per correggere l'avviso, aggiungere una lingua a FileE.

I file devono avere valori di lingua archiviati nella risorsa della versione quando possibile. Se un file è indipendente dalla lingua, usare [LANGID](column-data-types.md) 0.

[Tabella file](file-table.md) (FileB è un tipo di carattere, gli altri file non lo sono).



| File  | Versione | Linguaggio |
|-------|---------|----------|
| FileA | 1.0     | 1033     |
| FileB | 1.0     |          |
| FileC | FileA   |          |
| Archiviato |         |          |
| FileE | 1.0     |          |



 

[Tabella dei tipi di carattere](font-table.md)



| File  | FontTitle  |
|-------|------------|
| FileB | Titolo carattere |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



