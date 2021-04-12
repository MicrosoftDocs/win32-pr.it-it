---
description: La tabella degli errori viene utilizzata per cercare i modelli di formattazione dei messaggi di errore durante l'elaborazione degli errori con un codice di errore impostato ma senza un set di modelli di formattazione (situazione normale).
ms.assetid: 3c817468-cba7-46bf-9208-5e6699c02fb6
title: Tabella degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfcba5f68eb48621891c7a48aeedea2329996f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231874"
---
# <a name="error-table"></a>Tabella degli errori

La tabella degli errori viene utilizzata per cercare i modelli di formattazione dei messaggi di errore durante l'elaborazione degli errori con un codice di errore impostato ma senza un set di modelli di formattazione (situazione normale).

La tabella Error contiene le colonne seguenti.



| Colonna  | Tipo                     | Chiave | Nullable |
|---------|--------------------------|-----|----------|
| Errore   | [Integer](integer.md)   | S   | N        |
| Message | [Modello](template.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore
</dt> <dd>

Per un elenco dei numeri di errore e dei messaggi, vedere [Windows Installer messaggi di errore](windows-installer-error-messages.md) .

Il numero di errore deve essere un numero intero non negativo.

L'intervallo compreso tra 25000 e 30000 è riservato agli errori relativi alle azioni personalizzate. Gli autori di azioni personalizzate possono utilizzare questo intervallo per le azioni personalizzate.

</dd> <dt>

<span id="Message"></span><span id="message"></span><span id="MESSAGE"></span>Messaggio
</dt> <dd>

Questa colonna contiene il modello di formattazione dell'errore localizzabile. La tabella degli errori viene generata dal processo di compilazione iniziale per contenere i modelli di formato di debug.

Nella tabella seguente sono elencati i messaggi riservati. Per un elenco di codici di errore interni e di spedizione, vedere [Windows Installer messaggi di errore](windows-installer-error-messages.md).



| Errore | Message                                                    | Commenti                                                                                                                                                                                                      |
|-------|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | {{Errore irreversibile:}}                                          | Prefisso dell'intestazione per errori irreversibili (INSTALLMESSAGE \_ FATALEXIT). Il testo racchiuso tra parentesi graffe doppie {{text}} è visibile solo nel file di log. Il testo non viene visualizzato all'utente nell'interfaccia utente.                  |
| 1     | Errore \[ 1 \] .                                               | Prefisso dell'intestazione per gli errori ( \_ errore INSTALLMESSAGE)                                                                                                                                                             |
| 2     | Avviso \[ 1 \] .                                             | Prefisso dell'intestazione per gli avvisi ( \_ avviso INSTALLMESSAGE)                                                                                                                                                         |
| 3     |                                                            |                                                                                                                                                                                                              |
| 4     | Informazioni \[ 1 \] .                                                | Prefisso dell'intestazione per i messaggi informativi (INSTALLMESSAGE \_ info)                                                                                                                                              |
| 5     | Errore interno \[ 1 \] . \[2 \] {, \[ 3 \] } {, \[ 4 \] }              | Prefisso dell'intestazione per errori interni                                                                                                                                                                            |
| 6     |                                                            |                                                                                                                                                                                                              |
| 7     | {{Disco pieno:}}                                            | Prefisso dell'intestazione per gli errori di spazio su disco insufficiente (INSTALLMESSAGE \_ OUTOFDISKSPACE). Il testo racchiuso tra parentesi graffe doppie {{text}} è visibile solo nel file di log. Il testo non viene visualizzato all'utente nell'interfaccia utente. |
| 8     | \[Tempo azione \] : \[ 1 \] . \[2\]                              |                                                                                                                                                                                                              |
| 9     | \[ProductName\]                                            |                                                                                                                                                                                                              |
| 10    | { \[ 2 \] } {, \[ 3 \] } {, \[ 4 \] }                                  |                                                                                                                                                                                                              |
| 11    | Tipo di messaggio: \[ 1 \] , argomento: \[ 2\]                       |                                                                                                                                                                                                              |
| 12    | = = = Registrazione avviata: \[ data/ \] \[ ora\] ===                 |                                                                                                                                                                                                              |
| 13    | = = = Registrazione arrestata: \[ data/ \] \[ ora\] ===                 |                                                                                                                                                                                                              |
| 14    | Ora di inizio azione \[ \] : \[ 1\]                               |                                                                                                                                                                                                              |
| 15    | Ora di fine azione \[ \] : \[ 1 \] . Valore restituito \[ 2\]           |                                                                                                                                                                                                              |
| 16    | Tempo rimanente: { \[ 1 \] Min} { \[ 2 \] sec}                    |                                                                                                                                                                                                              |
| 17    | Memoria insufficiente. Arresta altre applicazioni prima di riprovare |                                                                                                                                                                                                              |
| 18    | Il programma di installazione non risponde più                          |                                                                                                                                                                                                              |
| 19    | Programma di installazione terminato in modo anomalo                           |                                                                                                                                                                                                              |
| 20    | Attendere mentre Windows configura \[ ProductName \] ...    |                                                                                                                                                                                                              |
| 21    | Raccolta delle informazioni necessarie...                          |                                                                                                                                                                                                              |
| 22    | Rimozione delle versioni precedenti dell'applicazione in corso...             |                                                                                                                                                                                                              |
| 23    | Preparazione della rimozione delle versioni precedenti dell'applicazione in corso...  |                                                                                                                                                                                                              |
| 32    | L' \[ installazione di {ProductName \] } è stata completata.            |                                                                                                                                                                                                              |
| 33    | L' \[ installazione di {ProductName \] } non è riuscita.                            |                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il modello non include la formattazione per il numero di errore nel campo 1. Quando si elabora l'errore, il programma di installazione connette un prefisso di intestazione al modello a seconda del tipo di messaggio. Queste intestazioni vengono inoltre archiviate nella tabella degli errori.

Il testo racchiuso tra parentesi graffe doppie {{text}} è visibile solo nel file di log. Il testo non viene visualizzato all'utente nell'interfaccia utente.

È possibile importare una tabella degli errori localizzata nel database usando Msidb.exe o [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). L'SDK include una tabella degli errori localizzata per ogni lingua elencata nella sezione [localizzazione dell'errore e delle tabelle ActionText](localizing-the-error-and-actiontext-tables.md) . Se la tabella degli errori non è popolata, il programma di installazione carica le stringhe localizzate per la lingua specificata dalla proprietà [**ProductLanguage**](productlanguage.md) .

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
</dl>

 

 



