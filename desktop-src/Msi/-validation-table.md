---
description: La \_ tabella di convalida è una tabella di sistema che contiene i nomi delle colonne e i valori delle colonne per tutte le tabelle del database.
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: Tabella _Validation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666f00ccccda11706dce6a8d7e04e0efea91b7cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881186"
---
# <a name="_validation-table"></a>\_Tabella di convalida

La \_ tabella di convalida è una tabella di sistema che contiene i nomi delle colonne e i valori delle colonne per tutte le tabelle del database. Viene utilizzato durante il processo di convalida del database per garantire che tutte le colonne siano contabilizzate e dispongano dei valori corretti. Questa tabella non è inclusa nel database del programma di installazione.

La \_ tabella di convalida include le colonne seguenti.



| Colonna      | Tipo                               | Chiave | Nullable |
|-------------|------------------------------------|-----|----------|
| Tabella       | [Identificatore](identifier.md)       | S   | N        |
| Colonna      | [Identificatore](identifier.md)       | S   | N        |
| Nullable    | [Text](text.md)                   | N   | N        |
| MinValue    | [DoubleInteger](doubleinteger.md) | N   | S        |
| MaxValue    | [DoubleInteger](doubleinteger.md) | N   | S        |
| KeyTable    | [Identificatore](identifier.md)       | N   | S        |
| KeyColumn   | [Integer](integer.md)             | N   | S        |
| Category    | [Text](text.md)                   | N   | S        |
| Set         | [Text](text.md)                   | N   | S        |
| Descrizione | [Text](text.md)                   | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo
</dt> <dd>

Utilizzato per identificare una tabella specifica. Questa chiave e la chiave della colonna formano la chiave primaria della \_ tabella di convalida.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Colonna
</dt> <dd>

Utilizzato per identificare una colonna specifica della tabella. Questa chiave e la chiave della tabella formano la chiave primaria della \_ tabella di convalida.

</dd> <dt>

<span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable
</dt> <dd>

Indica se la colonna può contenere un valore null.

Questa colonna può avere uno dei valori seguenti.



| string | Significato                                   |
|--------|-------------------------------------------|
| S      | Sì, la colonna potrebbe avere un valore null.    |
| N      | No, la colonna non può avere un valore null. |



 

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue
</dt> <dd>

Questo campo si applica alle colonne con valore numerico. Il campo contiene il valore minimo consentito. Può trattarsi del valore minimo per un numero intero o del valore minimo per una stringa di data o di versione.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue
</dt> <dd>

Questo campo si applica alle colonne con valore numerico. Il campo è il valore massimo consentito. Può trattarsi del valore massimo per un numero intero o del valore massimo per una stringa di data o di versione.

</dd> <dt>

<span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable
</dt> <dd>

Questo campo si applica alle colonne che sono chiavi esterne. Il campo identificato nella colonna deve essere collegato al numero di colonna specificato da colonna colonna nella tabella denominata in tabella. Può trattarsi di un elenco di tabelle separate da punti e virgola.

</dd> <dt>

<span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn
</dt> <dd>

Questo campo si applica alle colonne della tabella che sono chiavi esterne. Il campo identificato nella colonna deve essere collegato al numero di colonna specificato da colonna colonna nella tabella denominata in tabella. L'intervallo consentito del campo colonna colonna è 1-32.

</dd> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria
</dt> <dd>

Questo è il tipo di dati contenuti nel campo del database specificato dalle colonne della tabella e della colonna della \_ tabella di convalida. Se si tratta di un tipo con un valore numerico, ad esempio [Integer](integer.md), [DoubleInteger](doubleinteger.md) o [time/date](time-date.md), immettere null in questo campo e specificare l'intervallo del valore utilizzando le colonne MinValue e MaxValue. Utilizzare la colonna Categoria per specificare i tipi di dati non numerici descritti in [tipi di dati di colonna](column-data-types.md).

</dd> <dt>

<span id="Set"></span><span id="set"></span><span id="SET"></span>Set
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

Il campo categoria di questa tabella si applica solo ai dati stringa. Se il campo colonna fa riferimento a una colonna con dati binari, è necessario specificare il tipo di dati binario nel campo categoria. I tipi di colonna di dati Integer ignorano il campo categoria durante la convalida.

 

 



