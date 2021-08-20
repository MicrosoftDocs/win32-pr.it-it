---
description: La \_ Flussi tabella elenca i flussi di dati OLE incorporati. Si tratta di una tabella temporanea, creata solo quando viene fatto riferimento da un'SQL istruzione .
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: _Streams tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23f3796a3abb402027dc9985991a6ba673f5381d8f35657e7d80b0714c40f1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013339"
---
# <a name="_streams-table"></a>\_Flussi tavolo

La \_ Flussi tabella elenca i flussi di dati OLE incorporati. Si tratta di una tabella temporanea, creata solo quando viene fatto riferimento da un'SQL istruzione .



| Colonna | Tipo                 | Chiave | Nullable |
|--------|----------------------|-----|----------|
| Nome   | [Text](text.md)     | S   | N        |
| Dati   | [Binario](binary.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Chiave univoca che identifica il flusso. La lunghezza massima di Name è di 62 caratteri.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati
</dt> <dd>

Dati binari non formattati.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per copiare un flusso di dati OLE (ad esempio, un oggetto di tipo [Binary)](binary.md) da un file in un database, creare un record nella tabella Flussi e immettere il nome del flusso di dati nella colonna Nome del record e copiare i dati dal file nella colonna Dati usando \_ [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama). Usare [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il nuovo record nella tabella.

Per leggere un flusso di dati binari incorporato in un database, usare una query SQL per trovare e recuperare il record contenente i dati binari. Usare [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) per leggere i dati binari in un buffer.

Per spostare un flusso di dati binari da un database a un altro, esportare prima i dati in un file. Usare una query SQL per trovare il flusso di dati nel file e [**usare MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) per copiare i dati dal file nella colonna Data Flussi \_ tabella del secondo database. In questo modo si garantisce che ogni database abbia una propria copia dei dati binari. Non è possibile spostare dati binari da un database a un altro semplicemente recuperando un record con i dati dal primo database e inserendolo nel secondo database.

Per eliminare un flusso di dati, recuperare il record e impostare la colonna Dati su Null prima di aggiornare il record. Un altro metodo è rimuovere il record dalla tabella, eliminandolo usando [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o una query SQL semplice. Un flusso non deve essere recuperato in un record se il flusso viene eliminato dalla tabella.

Per rinominare un flusso di dati OLE, aggiornare la colonna "Nome" del record.

Se viene inserito un blocco in questa tabella usando SQL (ALTER TABLE <table> HOLD) o viene aggiunta una colonna con HOLD, la tabella deve essere rilasciata usando FREE. Flussi vengono scritti solo dopo il rilascio o il commit della tabella.

 

 



