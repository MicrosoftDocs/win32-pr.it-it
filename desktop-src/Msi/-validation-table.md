---
description: La tabella Validation è una tabella di sistema che contiene i nomi delle colonne e i valori delle colonne per \_ tutte le tabelle nel database.
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: _Validation tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a42fbe2a2f8da4abceb04912eee2a12edd708ff88d979fbf45f7de8051dc80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640446"
---
# <a name="_validation-table"></a>\_Tabella di convalida

La tabella Validation è una tabella di sistema che contiene i nomi delle colonne e i valori delle colonne per \_ tutte le tabelle nel database. Viene usato durante il processo di convalida del database per garantire che tutte le colonne siano rappresentate e che i valori siano corretti. Questa tabella non viene fornita con il database del programma di installazione.

Nella \_ tabella Convalida sono disponibili le colonne seguenti.



| Colonna      | Tipo                               | Chiave | Nullable |
|-------------|------------------------------------|-----|----------|
| Tabella       | [Identificatore](identifier.md)       | S   | N        |
| Colonna      | [Identificatore](identifier.md)       | S   | N        |
| Nullable    | [Text](text.md)                   | N   | N        |
| Minvalue    | [DoubleInteger](doubleinteger.md) | N   | S        |
| MaxValue    | [DoubleInteger](doubleinteger.md) | N   | S        |
| KeyTable    | [Identificatore](identifier.md)       | N   | S        |
| KeyColumn   | [Integer](integer.md)             | N   | S        |
| Category    | [Text](text.md)                   | N   | S        |
| Impostazione         | [Text](text.md)                   | N   | S        |
| Descrizione | [Text](text.md)                   | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo
</dt> <dd>

Utilizzato per identificare una tabella specifica. Questa chiave e la chiave di colonna formano la chiave primaria della \_ tabella Validation.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Colonna
</dt> <dd>

Consente di identificare una colonna specifica della tabella. Questa chiave e la chiave table formano la chiave primaria della \_ tabella Validation.

</dd> <dt>

<span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable
</dt> <dd>

Identifica se la colonna può contenere un valore Null.

Questa colonna può avere uno dei valori seguenti.



| string | Significato                                   |
|--------|-------------------------------------------|
| S      | Sì, la colonna può avere un valore Null.    |
| N      | No, la colonna potrebbe non avere un valore Null. |



 

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>Minvalue
</dt> <dd>

Questo campo si applica alle colonne con valore numerico. Il campo contiene il valore minimo consentito. Può trattarsi del valore minimo per un numero intero o del valore minimo per una stringa di data o versione.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>Maxvalue
</dt> <dd>

Questo campo si applica alle colonne con valore numerico. Il campo è il valore massimo consentito. Può trattarsi del valore massimo per un numero intero o del valore massimo per una stringa di data o versione.

</dd> <dt>

<span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable
</dt> <dd>

Questo campo si applica alle colonne che sono chiavi esterne. Il campo identificato in Column deve essere correlato al numero di colonna specificato da KeyColumn nella tabella denominata in KeyTable. Può trattarsi di un elenco di tabelle separate da punti e virgola.

</dd> <dt>

<span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn
</dt> <dd>

Questo campo si applica alle colonne della tabella che sono chiavi esterne. Il campo identificato in Column deve essere correlato al numero di colonna specificato da KeyColumn nella tabella denominata in KeyTable. L'intervallo consentito del campo KeyColumn è compreso tra 1 e 32.

</dd> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria
</dt> <dd>

Si tratta del tipo di dati contenuti nel campo del database specificato dalle colonne Table e Column della \_ tabella Validation. Se si tratta di un tipo con un valore numerico, ad esempio [Integer](integer.md), [DoubleInteger](doubleinteger.md) o [Time/Date](time-date.md), immettere null in questo campo e specificare l'intervallo del valore usando le colonne MinValue e MaxValue . Usare la colonna Categoria per specificare i tipi di dati non numerici descritti in [Tipi di dati delle colonne](column-data-types.md).

</dd> <dt>

<span id="Set"></span><span id="set"></span><span id="SET"></span>Impostare
</dt> <dd>

Si tratta di un elenco di valori consentiti per questo campo separati da punti e virgola. Questo campo viene in genere usato per le enumerazioni.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione dei dati archiviati nella colonna.

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

## <a name="remarks"></a>Commenti

Il campo Categoria di questa tabella si applica solo ai dati stringa. Se il campo Colonna fa riferimento a una colonna con dati binari, è necessario specificare il tipo di dati binary nel campo Categoria . Dati Integer I tipi di colonna ignorano il campo Categoria durante la convalida.

 

 



