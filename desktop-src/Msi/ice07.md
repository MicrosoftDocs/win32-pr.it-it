---
description: ICE07 verifica che il pacchetto di installazione specifichi che i caratteri siano installati in FontsFolder. Se un tipo di carattere viene installato in una cartella diversa da FontsFolder, il programma di installazione crea un collegamento anziché installare effettivamente il tipo di carattere.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a79bcb681a57bb09ff235b35a5287492a4f39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314244"
---
# <a name="ice07"></a>ICE07

ICE07 verifica che il pacchetto di installazione specifichi che i caratteri siano installati in FontsFolder. Se un tipo di carattere viene installato in una cartella diversa da FontsFolder, il programma di installazione crea un collegamento anziché installare effettivamente il tipo di carattere.

L'azione personalizzata ICE07 esegue le operazioni seguenti per ogni tipo di carattere della [tabella dei tipi di carattere](font-table.md).

1.  Trova il file del tipo di carattere a cui appartiene ogni titolo del carattere usando la [tabella dei tipi di carattere](font-table.md).
2.  Esegue una query sulla \_ colonna componente della [tabella file](file-table.md) per il componente che controlla ogni file.
3.  Esegue una query sulla \_ colonna di directory della [tabella dei componenti](component-table.md) per ottenere una chiave nella tabella di directory.
4.  Risolve la tabella di [directory](directory-table.md) per determinare il nome della cartella in cui il programma di installazione deve installare il file del tipo di carattere
5.  Invia un errore se il file del tipo di carattere viene installato in una cartella diversa da FontsFolder.

## <a name="result"></a>Risultato

ICE07 Invia un errore se rileva che il database specifica che un file del tipo di carattere deve essere installato in una cartella diversa da FontsFolder.

## <a name="example"></a>Esempio

IC07 invia il messaggio di errore seguente per l'esempio illustrato.

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[Tabella dei tipi di carattere](font-table.md)



| file\_ | FontTitle |
|--------|-----------|
| Myrtle | Tahoma    |



 

[Tabella file](file-table.md) (parziale)



| File   | Componente\_   |
|--------|---------------|
| Myrtle | Myrtle \_ Beach |



 

[Tabella componenti](component-table.md) (parziale)



| Componente     | Directory\_ |
|---------------|-------------|
| Myrtle \_ Beach | SandBar     |



 

In questo esempio, il tipo di carattere Tahoma esegue il mapping al file del tipo di carattere Myrtle. Il file Myrtle appartiene al componente Myrtle \_ Beach. La risoluzione della tabella di directory mostra che tutti i file appartenenti a Myrtle \_ Beach devono essere installati nella cartella di sabbia. Poiché non è FontsFolder, ICE07 pubblica un messaggio di errore.

Si noti che se il componente Myrtle \_ Beach appartiene realmente alla cartella del banco di sabbia e non al FontsFolder, il tipo di carattere Tahoma potrebbe non appartenere a Myrtle \_ Beach. Una possibile correzione per l'errore consiste nell'includere Tahoma in un altro componente che viene installato nella directory FontsFolder.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



