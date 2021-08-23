---
description: ICE07 convalida che il pacchetto di installazione specifica che i tipi di carattere devono essere installati nella cartella FontsFolder. Se un tipo di carattere viene installato in una cartella diversa da FontsFolder, il programma di installazione crea un collegamento anziché installare effettivamente il tipo di carattere.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4226a0e555a35c7d5735abe0b14520d000bfeea8c888488ce37b15a78674ff9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581291"
---
# <a name="ice07"></a>ICE07

ICE07 convalida che il pacchetto di installazione specifica che i tipi di carattere devono essere installati nella cartella FontsFolder. Se un tipo di carattere viene installato in una cartella diversa da FontsFolder, il programma di installazione crea un collegamento anziché installare effettivamente il tipo di carattere.

L'azione personalizzata ICE07 esegue le operazioni seguenti per ogni tipo di carattere nella [tabella Font](font-table.md).

1.  Trova il file del tipo di carattere a cui appartiene ogni titolo del tipo di carattere usando la [tabella Font](font-table.md).
2.  Esegue una query \_ nella colonna Componente della tabella [File](file-table.md) per il componente che controlla ogni file.
3.  Esegue una query \_ nella colonna Directory della tabella Component [per](component-table.md) ottenere una chiave nella tabella Directory.
4.  Risolve la tabella [Directory per](directory-table.md) determinare il nome della cartella in cui il programma di installazione deve installare il file del tipo di carattere
5.  Invia un errore se il file del tipo di carattere viene installato in una cartella diversa da FontsFolder.

## <a name="result"></a>Risultato

ICE07 invia un errore se rileva che il database specifica che un file del tipo di carattere deve essere installato in una cartella diversa da FontsFolder.

## <a name="example"></a>Esempio

IC07 pubblica il messaggio di errore seguente per l'esempio illustrato.

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[Tabella dei tipi di carattere](font-table.md)



| file\_ | CarattereTitle |
|--------|-----------|
| Myrtle | Tahoma    |



 

[Tabella file](file-table.md) (parziale)



| File   | Componente\_   |
|--------|---------------|
| Myrtle | Myrtle \_ Beach |



 

[Tabella dei componenti](component-table.md) (parziale)



| Componente     | Directory\_ |
|---------------|-------------|
| Myrtle \_ Beach | Sandbar     |



 

In questo esempio, il tipo di carattere Tahoma viene mappato al file del tipo di carattere Myrtle. Il file Myrtle appartiene al componente Myrtle \_ Beach. La risoluzione della tabella Directory indica che tutti i file appartenenti a Myrtle Beach devono essere installati \_ nella cartella Sandbar. Poiché non si tratta di FontsFolder, ICE07 invia un messaggio di errore.

Si noti che se il componente Myrtle Beach appartiene effettivamente alla cartella Sandbar e non a FontsFolder, il tipo di carattere Tahoma potrebbe non appartenere \_ a Myrtle \_ Beach. Una possibile correzione dell'errore potrebbe essere includere Tahoma in un altro componente installato nella directory FontsFolder.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



