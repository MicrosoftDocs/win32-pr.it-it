---
description: La \_ tabella Columns è una tabella di sistema di sola lettura che contiene il catalogo delle colonne. Vengono elencate le colonne per tutte le tabelle. È possibile eseguire una query su questa tabella per determinare se esiste una determinata colonna.
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: Tabella _Columns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d896f330e5fc2e13b5f172581341eb11a09617d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311119"
---
# <a name="_columns-table"></a>\_Tabella colonne

La \_ tabella Columns è una tabella di sistema di sola lettura che contiene il catalogo delle colonne. Vengono elencate le colonne per tutte le tabelle. È possibile eseguire una query su questa tabella per determinare se esiste una determinata colonna.

La \_ tabella Columns contiene le colonne seguenti.



| Colonna | Tipo                   | Chiave | Nullable |
|--------|------------------------|-----|----------|
| Tabella  | [Text](text.md)       | S   | N        |
| Number | [Integer](integer.md) | S   | N        |
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

Poiché la \_ tabella Columns è una tabella di sistema che non può essere modificata tramite query SQL, non è possibile ottenere le chiavi primarie con la funzione [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) o la [**Proprietà PrimaryKeys**](database-primarykeys.md).

Nella tabella Columns sono archiviate solo le colonne permanenti \_ . Per determinare se esiste una colonna temporanea, è necessario creare una vista usando un'istruzione SELECT sulla \* tabella, quindi eseguire il ciclo di tutti i campi di un record restituito dalla funzione [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) con l' \_ opzione MSICOLINFO names.

 

 



