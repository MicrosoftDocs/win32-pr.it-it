---
description: Si tratta di una tabella temporanea di sola lettura utilizzata per visualizzare le trasformazioni con la modalità di visualizzazione trasforma. Questa tabella non viene mai resa permanente dal programma di installazione.
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: Tabella _TransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cc513b1aae388d01cda178bfbefdc88874f6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528884"
---
# <a name="_transformview-table"></a>\_Tabella transformview

Si tratta di una tabella temporanea di sola lettura utilizzata per visualizzare le trasformazioni con la modalità di visualizzazione trasforma. Questa tabella non viene mai resa permanente dal programma di installazione.

Per richiamare la modalità di visualizzazione trasformazione, ottenere un handle e aprire il database di riferimento. Vedere [recupero di un handle di database](obtaining-a-database-handle.md). Chiamare [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) con \_ errore MSITRANSFORM \_ VIEWTRANSFORM. In questo modo viene arrestata l'applicazione della trasformazione al database e viene eseguito il dump del contenuto della trasformazione nella \_ tabella transformview. È possibile accedere ai dati nella tabella tramite query SQL. Vedere [utilizzo delle query](working-with-queries.md).

La \_ tabella transformview non viene cancellata quando viene applicata un'altra trasformazione. La tabella riflette l'effetto cumulativo delle applicazioni successive. Per visualizzare le trasformazioni separatamente è necessario rilasciare la tabella.

La \_ tabella transformview include le colonne seguenti.



| Colonna  | Tipo                         | Chiave | Nullable |
|---------|------------------------------|-----|----------|
| Tabella   | [Identificatore](identifier.md) | S   | N        |
| Colonna  | [Text](text.md)             | S   | N        |
| Riga     | [Text](text.md)             | S   | S        |
| Data    | [Text](text.md)             | N   | S        |
| Corrente | [Text](text.md)             | N   | S        |



 

## <a name="column"></a>Colonna

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo
</dt> <dd>

Nome di una tabella di database modificata.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Colonna
</dt> <dd>

Nome di una colonna di tabella modificata o di inserimento, eliminazione, creazione o eliminazione.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Riga
</dt> <dd>

Elenco dei valori di chiave primaria separati da tabulazioni. I valori di chiave primaria null sono rappresentati da un singolo carattere di spazio. Un valore null in questa colonna indica una modifica dello schema.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati
</dt> <dd>

Dati, nome di un flusso di dati o definizione di colonna.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Corrente
</dt> <dd>

Valore corrente dal database di riferimento o da un numero di colonna.

</dd> </dl>

## <a name="remarks"></a>Commenti

La \_ transformview viene mantenuta in memoria da un conteggio dei blocchi, che può essere rilasciato con il comando SQL seguente.

"ALTER TABLE \_ Transformview Free".

È possibile accedere ai dati nella tabella tramite query SQL. Il linguaggio SQL è costituito da due divisioni principali: DDL (Data Definition Language) utilizzato per definire tutti gli oggetti in un database SQL e DML (Data Manipulation Language) utilizzato per selezionare, inserire, aggiornare ed eliminare dati negli oggetti definiti mediante DDL.

Le operazioni di trasformazione DML (Data Manipulation Language) sono indicate di seguito. I dati DML (Data Manipulation Language) sono istruzioni in SQL che consentono di modificare, anziché definire i dati.



| Operazione di trasformazione | Risultato SQL                                    |
|---------------------|-----------------------------------------------|
| Modificare i dati         | tabella colonna riga dati {valore corrente} |
| Inserimento di una riga          | tabella "INSERT" {Row} NULL NULL              |
| Elimina riga          | tabella "DELETE" {Row} NULL NULL              |



 

Le operazioni di trasformazione DDL (Data Definition Language) sono indicate di seguito. I dati DDL (Data Definition Language) sono istruzioni in SQL che definiscono, anziché modificare, i dati.



| Operazione di trasformazione | Risultato SQL                                   |
|---------------------|----------------------------------------------|
| Aggiungere una colonna          | tabella colonna NULL {defn} {numero di colonna} |
| Aggiungi tabella           | tabella "CREATE" NULL NULL NULL              |
| Eliminare una tabella          | tabella "DROP" NULL NULL NULL                |



 

Quando l'applicazione di una trasformazione aggiunge questa tabella, il campo dati riceve testo che può essere interpretato come valore integer a 16 bit. Il valore descrive la colonna denominata nel campo colonna. È possibile confrontare il valore integer con le costanti nella tabella seguente per determinare la definizione della colonna modificata.



| bit                                                                                                       | Descrizione                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>BITS 0 7<br/>         | Esadecimale: 0x0000 0x0100<br/> Decimale: 0 255<br/> Larghezza colonna<br/>                                                                                                                                                                                                                                  |
| <span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8<br/>                  | Esadecimale: 0x0100<br/> Decimale: 256<br/> Una colonna persistente. Zero indica una colonna temporanea. <br/>                                                                                                                                                                                                   |
| <span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9<br/>                  | Esadecimale: 0x0200<br/> Decimale: 1023<br/> Colonna localizzabile. Zero indica che la colonna non può essere localizzata.<br/>                                                                                                                                                                                      |
| <span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11<br/> | Esadecimale: 0x0000<br/> Decimale: 0<br/> Long integer<br/> Esadecimale: 0x0400<br/> Decimale: 1024<br/> Valore short Integer<br/> Esadecimale: 0x0800<br/> Decimale: 2048<br/> Oggetto binario<br/> Esadecimale: 0x0C00<br/> Decimale: 3072<br/> string<br/> |
| <span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12<br/>              | Esadecimale: 0x1000<br/> Decimale: 4096<br/> Colonna nullable. Zero indica che la colonna è non nullable.<br/>                                                                                                                                                                                               |
| <span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13<br/>              | Esadecimale: 0x2000<br/> Decimale: 8192<br/> Colonna chiave primaria. Zero indica che questa colonna non è una chiave primaria.<br/>                                                                                                                                                                                      |
| <span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>BITS 14 15<br/> | Esadecimale: 0x4000 0x8000<br/> Decimale: 16384 32768<br/> Riservato<br/>                                                                                                                                                                                                                                |



 

Per uno script di esempio che illustra la \_ tabella transformview, vedere [visualizzare una trasformazione](view-a-transform.md).

 

 




