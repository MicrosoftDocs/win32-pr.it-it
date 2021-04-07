---
description: La \_ tabella Storages elenca le archiviazioni di dati OLE embedded. Si tratta di una tabella temporanea, creata solo quando si fa riferimento a un'istruzione SQL.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: Tabella _Storages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27995dd61c7d25100fc0e1ae2297695e361f44f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881193"
---
# <a name="_storages-table"></a>\_Tabella Storages

La \_ tabella Storages elenca le archiviazioni di dati OLE embedded. Si tratta di una tabella temporanea, creata solo quando si fa riferimento a un'istruzione SQL.



| Colonna | Tipo                 | Chiave | Nullable |
|--------|----------------------|-----|----------|
| Nome   | [Text](text.md)     | S   | N        |
| Data   | [Binario](binary.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Chiave univoca che identifica l'archiviazione. La lunghezza massima del nome è 31 caratteri.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati
</dt> <dd>

Dati binari non formattati.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per aggiungere una risorsa di archiviazione OLE a un database, creare un nuovo record nella \_ tabella Storages e immettere il nome della risorsa di archiviazione nella colonna nome. Usare [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) per copiare i dati nella colonna di dati del record. Infine, usare [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il record nella \_ tabella storages.

Non è possibile leggere i dati dalla \_ tabella storages. \_È tuttavia possibile eseguire una query sulla tabella Storages per verificare l'esistenza di una risorsa di archiviazione specifica. Ciò significa che non è possibile spostare una risorsa di archiviazione OLE da un database a un altro. È invece necessario importare il file di archiviazione originale nel nuovo database. Per eliminare una risorsa di archiviazione OLE, recuperare il record contenente i dati binari, impostare la colonna di dati nella \_ tabella Storages su null, quindi aggiornare il record. Un metodo alternativo consiste nel semplicemente eliminare il record utilizzando [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o una query SQL semplice.

Per rinominare una risorsa di archiviazione OLE, aggiornare la colonna Name del record.

Se in questa tabella viene posizionata un'attesa utilizzando SQL (ALTER TABLE <table> In attesa) o viene aggiunta una colonna con l'ESENZIONe, la tabella deve essere rilasciata usando FREE. Le archiviazioni non vengono scritte finché la tabella non viene rilasciata o sottoposta a commit.

 

 



