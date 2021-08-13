---
description: Si tratta di una tabella temporanea di sola lettura usata per visualizzare le trasformazioni con la modalità di visualizzazione trasformazione. Questa tabella non viene mai mantenuta dal programma di installazione.
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: _TransformView tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b3254c7419ed5d4964377a466ecd557429a22450a9ba84fdd892822fca86c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640466"
---
# <a name="_transformview-table"></a>\_Tabella TransformView

Si tratta di una tabella temporanea di sola lettura usata per visualizzare le trasformazioni con la modalità di visualizzazione trasformazione. Questa tabella non viene mai mantenuta dal programma di installazione.

Per richiamare la modalità di visualizzazione di trasformazione, ottenere un handle e aprire il database di riferimento. Vedere [Recupero di un handle di database](obtaining-a-database-handle.md). Chiamare [**MsiDatabaseApplyTransform con**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) MSITRANSFORM \_ ERROR \_ VIEWTRANSFORM. In questo modo la trasformazione non viene applicata al database ed esegue il dump del contenuto della trasformazione nella \_ tabella TransformView. È possibile accedere ai dati nella tabella usando SQL query. Vedere [Uso delle query](working-with-queries.md).

La \_ tabella TransformView non viene cancellata quando viene applicata un'altra trasformazione. La tabella riflette l'effetto cumulativo delle applicazioni successive. Per visualizzare le trasformazioni separatamente, è necessario rilasciare la tabella.

La \_ tabella TransformView include le colonne seguenti.



| Colonna  | Tipo                         | Chiave | Nullable |
|---------|------------------------------|-----|----------|
| Tabella   | [Identificatore](identifier.md) | S   | N        |
| Colonna  | [Text](text.md)             | S   | N        |
| Riga     | [Text](text.md)             | S   | S        |
| Dati    | [Text](text.md)             | N   | S        |
| Corrente | [Text](text.md)             | N   | S        |



 

## <a name="column"></a>Colonna

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo
</dt> <dd>

Nome di una tabella di database modificata.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Colonna
</dt> <dd>

Nome di una colonna di tabella modificata o INSERT, DELETE, CREATE o DROP.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Riga
</dt> <dd>

Elenco dei valori di chiave primaria separati da tabulazioni. I valori di chiave primaria Null sono rappresentati da un singolo spazio. Un valore Null in questa colonna indica una modifica dello schema.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati
</dt> <dd>

Dati, nome di un flusso di dati o definizione di colonna.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Corrente
</dt> <dd>

Valore corrente del database di riferimento o colonna di un numero.

</dd> </dl>

## <a name="remarks"></a>Commenti

\_TransformView viene mantenuto in memoria da un conteggio dei blocchi, che può essere rilasciato con il comando SQL seguente.

"ALTER TABLE \_ TransformView FREE".

È possibile accedere ai dati nella tabella usando SQL query. Il linguaggio SQL ha due divisioni principali: Data Definition Language (DDL) che viene usato per definire tutti gli oggetti in un database SQL e Data Manipulation Language (DML) usato per selezionare, inserire, aggiornare ed eliminare i dati negli oggetti definiti tramite DDL.

Le operazioni di trasformazione DML (Data Manipulation Language) sono indicate come segue. Data Manipulation Language (DML) sono istruzioni in SQL che modificano, anziché definire, i dati.



| Operazione di trasformazione | SQL risultato                                    |
|---------------------|-----------------------------------------------|
| Modificare i dati         | {table} {column} {row} {data} {valore corrente} |
| Inserimento di una riga          | {table} "INSERT" {row} NULL              |
| Elimina riga          | {table} "DELETE" {row} NULL              |



 

Le operazioni di trasformazione DDL (Data Definition Language) sono indicate come segue. Data Definition Language (DDL) sono istruzioni in SQL che definiscono, anziché manipolare, i dati.



| Operazione di trasformazione | SQL risultato                                   |
|---------------------|----------------------------------------------|
| Aggiungere una colonna          | {table} {column} NULL {defn} {numero di colonna} |
| Aggiungi tabella           | {table} "CREATE" NULL NULL              |
| Eliminare una tabella          | {table} "DROP" NULL NULL                |



 

Quando l'applicazione di una trasformazione aggiunge questa tabella, il campo Dati riceve testo che può essere interpretato come valore intero a 16 bit. Il valore descrive la colonna denominata nel campo Colonna. È possibile confrontare il valore integer con le costanti nella tabella seguente per determinare la definizione della colonna modificata.



| bit                                                                                                       | Descrizione                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bit 0 7<br/>         | Esadecimale: 0x0000 0x0100<br/> Decimale: 0 255<br/> Larghezza colonna<br/>                                                                                                                                                                                                                                  |
| <span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8<br/>                  | Esadecimale: 0x0100<br/> Decimale: 256<br/> Colonna persistente. Zero indica una colonna temporanea. <br/>                                                                                                                                                                                                   |
| <span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9<br/>                  | Esadecimale: 0x0200<br/> Decimale: 1023<br/> Colonna localizzabile. Zero indica che la colonna non può essere localizzata.<br/>                                                                                                                                                                                      |
| <span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bit 10 11<br/> | Esadecimale: 0x0000<br/> Decimale: 0<br/> Long integer<br/> Esadecimale: 0x0400<br/> Decimale: 1024<br/> Numero intero breve<br/> Esadecimale: 0x0800<br/> Decimale: 2048<br/> Oggetto binario<br/> Esadecimale: 0x0C00<br/> Decimale: 3072<br/> string<br/> |
| <span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12<br/>              | Esadecimale: 0x1000<br/> Decimale: 4096<br/> Colonna nullable. Zero indica che la colonna non ammette valori Null.<br/>                                                                                                                                                                                               |
| <span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13<br/>              | Esadecimale: 0x2000<br/> Decimale: 8192<br/> Colonna chiave primaria. Zero indica che questa colonna non è una chiave primaria.<br/>                                                                                                                                                                                      |
| <span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bit 14 15<br/> | Esadecimale: 0x4000 0x8000<br/> Decimale: 16384 32768<br/> Riservato<br/>                                                                                                                                                                                                                                |



 

Per un esempio di script che illustra la \_ tabella TransformView, vedere [Visualizzare una trasformazione](view-a-transform.md).

 

 




