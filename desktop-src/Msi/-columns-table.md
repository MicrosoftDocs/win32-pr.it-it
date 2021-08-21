---
description: La tabella Columns è una tabella di sistema di sola \_ lettura che contiene il catalogo di colonne. Elenca le colonne per tutte le tabelle. È possibile eseguire una query su questa tabella per determinare se esiste una determinata colonna.
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: _Columns tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7cbb603c077d7873cdfbea88070e555902883ba579b422627b2581aca04745b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640476"
---
# <a name="_columns-table"></a>\_Tabella Columns

La tabella Columns è una tabella di sistema di sola \_ lettura che contiene il catalogo di colonne. Elenca le colonne per tutte le tabelle. È possibile eseguire una query su questa tabella per determinare se esiste una determinata colonna.

La \_ tabella Columns include le colonne seguenti.



| Colonna | Tipo                   | Chiave | Nullable |
|--------|------------------------|-----|----------|
| Tabella  | [Text](text.md)       | S   | N        |
| Numero | [Integer](integer.md) | S   | N        |
| Nome   | [Text](text.md)       | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo
</dt> <dd>

Nome della tabella che contiene la colonna.

</dd> <dt>

<span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Numero
</dt> <dd>

Ordine della colonna all'interno della tabella.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Nome della colonna.

</dd> </dl>

## <a name="remarks"></a>Commenti

Poiché la tabella Columns è una tabella di sistema che non può essere modificata tramite query SQL, non è possibile ottenere le chiavi primarie con la funzione \_ [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) o la [**proprietà PrimaryKeys**](database-primarykeys.md).

Nella tabella Columns vengono archiviate solo \_ le colonne permanenti. Per determinare se esiste una colonna temporanea, è necessario creare una vista usando un'istruzione SELECT sulla tabella, quindi eseguire un ciclo in tutti i campi di un record restituito dalla funzione \* [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) con l'opzione MSICOLINFO \_ NAMES.

 

 



