---
description: La \_ tabella Streams elenca i flussi di dati OLE incorporati. Si tratta di una tabella temporanea, creata solo quando si fa riferimento a un'istruzione SQL.
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: Tabella _Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9607097b32acc8a3c2350a00db0b9721a4aa353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311115"
---
# <a name="_streams-table"></a>\_Tabella flussi

La \_ tabella Streams elenca i flussi di dati OLE incorporati. Si tratta di una tabella temporanea, creata solo quando si fa riferimento a un'istruzione SQL.



| Colonna | Tipo                 | Chiave | Nullable |
|--------|----------------------|-----|----------|
| Nome   | [Text](text.md)     | S   | N        |
| Data   | [Binario](binary.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Chiave univoca che identifica il flusso. La lunghezza massima del nome è di 62 caratteri.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati
</dt> <dd>

Dati binari non formattati.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per copiare un flusso di dati OLE, ad esempio un oggetto con tipo di dati [Binary](binary.md) , da un file in un database, creare un record nella \_ tabella Streams e immettere il nome del flusso di dati nella colonna Name del record e copiare i dati dal file nella colonna di dati tramite [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama). Usare [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il nuovo record nella tabella.

Per leggere un flusso di dati binario incorporato in un database, usare una query SQL per trovare e recuperare il record contenente i dati binari. Usare [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) per leggere i dati binari in un buffer.

Per spostare un flusso di dati binari da un database a un altro, esportare prima i dati in un file. Usare una query SQL per trovare il flusso di dati nel file e usare [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) per copiare i dati dal file nella colonna di dati della \_ tabella dei flussi del secondo database. In questo modo si garantisce che ogni database disponga di una propria copia dei dati binari. Non è possibile spostare i dati binari da un database a un altro semplicemente recuperando un record con i dati del primo database e inserendoli nel secondo database.

Per eliminare un flusso di dati, recuperare il record e impostare la colonna di dati su null prima di aggiornare il record. Un altro metodo consiste nel rimuovere il record dalla tabella, eliminarlo utilizzando [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o una query SQL semplice. Un flusso non deve essere recuperato in un record se il flusso viene eliminato dalla tabella.

Per rinominare un flusso di dati OLE, aggiornare la colonna ' name ' del record.

Se in questa tabella viene posizionata un'attesa utilizzando SQL (ALTER TABLE <table> In attesa) o viene aggiunta una colonna con l'ESENZIONe, la tabella deve essere rilasciata usando FREE. I flussi non vengono scritti finché la tabella non viene rilasciata o sottoposta a commit.

 

 



