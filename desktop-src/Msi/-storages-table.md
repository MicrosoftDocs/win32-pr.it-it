---
description: La \_ tabella Storages elenca le risorse di archiviazione dei dati OLE incorporate. Si tratta di una tabella temporanea, creata solo quando viene fatto riferimento da un'istruzione SQL tabella.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: _Storages tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee16db075df86e5c5a9c794d3320b49052cf746023bd70e02305d6ce079dbbf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146074"
---
# <a name="_storages-table"></a>\_Tabella Storages

La \_ tabella Storages elenca le risorse di archiviazione dei dati OLE incorporate. Si tratta di una tabella temporanea, creata solo quando viene fatto riferimento da un'istruzione SQL tabella.



| Colonna | Tipo                 | Chiave | Nullable |
|--------|----------------------|-----|----------|
| Nome   | [Text](text.md)     | S   | N        |
| Dati   | [Binario](binary.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Chiave univoca che identifica l'archiviazione. La lunghezza massima di Name è di 31 caratteri.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati
</dt> <dd>

Dati binari non formattati.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per aggiungere un'archiviazione OLE a un database, creare un nuovo record nella tabella Storages e immettere il nome dell'archiviazione \_ nella colonna Nome. Usare [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) per copiare i dati nella colonna Data di questo record. Usare infine [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il record nella \_ tabella Storages.

I dati non possono essere letti dalla \_ tabella Storages. È tuttavia possibile eseguire query sulla tabella Storages per \_ verificare l'esistenza di una risorsa di archiviazione specifica. Ciò significa che non è possibile spostare un'archiviazione OLE da un database a un altro. È invece necessario importare il file di archiviazione originale nel nuovo database. Per eliminare un archivio OLE, recuperare il record contenente i dati binari, impostare la colonna Dati nella tabella \_ Storages su Null e quindi aggiornare il record. Un metodo alternativo consiste semplicemente nell'eliminare il record usando [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o una query SQL query.

Per rinominare un archivio OLE, aggiornare la colonna Nome del record.

Se un blocco viene inserito in questa tabella usando SQL (ALTER TABLE <table> HOLD) o viene aggiunta una colonna con HOLD, la tabella deve essere rilasciata usando FREE. Le risorse di archiviazione non vengono scritte fino al rilascio o al commit della tabella.

 

 



