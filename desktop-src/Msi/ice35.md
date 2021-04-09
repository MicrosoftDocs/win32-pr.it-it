---
description: ICE35 convalida che i componenti contenenti file compressi archiviati in un file CAB non siano impostati per l'esecuzione dall'origine. Con Windows Installer 2,0 o versione successiva, questa restrizione è stata rimossa.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea6a98079d3c57e0c796332cf0cd5f11045a07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967790"
---
# <a name="ice35"></a>ICE35

ICE35 convalida che i componenti contenenti file compressi archiviati in un [file CAB](cabinet-files.md) non siano impostati per l'esecuzione dall'origine. Con Windows Installer 2,0 o versione successiva, questa restrizione è stata rimossa.

ICE35 esegue una query sulla colonna CAB della [tabella dei supporti](media-table.md) per determinare quali file vengono compressi e archiviati in un file CAB. Viene eseguita una query sulla [tabella file](file-table.md) per determinare quali componenti contengono questi file. Infine, viene controllata la [tabella dei componenti](component-table.md) per determinare se i bit dell'esecuzione dall'origine sono impostati nella colonna attributi.

## <a name="result"></a>Risultato

ICE35 Invia un messaggio di errore se è presente un file compresso archiviato in un file CAB appartenente a un componente con il bit msidbComponentAttributesSourceOnly impostato nella colonna attributi della [tabella dei componenti](component-table.md). Con Windows Installer 2,0 o versioni successive, questo valore viene modificato da un errore in un messaggio di avviso. Un pacchetto che supporta solo Windows Installer 2,0 e versioni successive presenta la \_ Proprietà PID PageCount del flusso di informazioni di riepilogo impostato su un valore pari ad almeno 200.

ICE35 Invia un messaggio di avviso se è presente un file compresso archiviato in un file CAB appartenente a un componente con il bit msidbComponentAttributesOptional impostato nella colonna attributi della [tabella dei componenti](component-table.md). Questo messaggio di avviso è stato rimosso con Windows Installer 2,0 e versioni successive.

Se più file in un componente si trovano in un file CAB, ICE35 segnala gli errori per ogni file con l'esecuzione dal set di bit di origine.

## <a name="example"></a>Esempio

ICE35 segnala gli errori e gli avvisi seguenti per l'esempio illustrato con una versione precedente alla Windows Installer versione 2,0.



| Errore ICE35                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRORE: il componente Component3 non può essere eseguito solo dall'origine perché il file membro ' file3' è compresso. | È presente un file compresso archiviato in un file CAB e questo file appartiene a un componente con il bit SourceOnly impostato nella colonna attributi della tabella dei [componenti](component-table.md). Per correggere questo errore, modificare i 2 bit inferiori del valore degli attributi Component2's in "00", vale a dire solo locale, oppure rimuovere file4 dal file CAB.<br/>                                                                                                                                                                         |
| ERRORE: il componente Component3 non può essere eseguito solo dall'origine perché il file membro ' file3' è compresso. | È presente un file compresso archiviato in un file CAB e questo file appartiene a un componente con il bit SourceOnly impostato nella colonna attributi della tabella dei [componenti](component-table.md). Poiché i file in un componente non devono essere tutti originati dallo stesso supporto, ICE35 segnala gli errori per ogni file nel componente che si trova in un file CAB.<br/> Per correggere questo errore, modificare i 2 bit inferiori del valore degli attributi Component2's in "00", vale a dire solo locale, oppure rimuovere file4 dal file CAB.<br/> |



 

[Tabella media](media-table.md) (parziale)



| DiskID | LastSequence | CAB   |
|--------|--------------|-----------|
| 1      | 2            |           |
| 2      | 4            | One.cab   |
| 3      | 5            | \#Two.cab |



 

[Tabella file](file-table.md) (parziale)



| File  | Componente\_ | Sequenza |
|-------|-------------|----------|
| File1 | Component1  | 1        |
| File2 | Component2  | 2        |
| File3 | Component2  | 3        |
| File4 | Component3  | 4        |
| File5 | Component3  | 5        |



 

[Tabella componenti](component-table.md) (parziale)



| Componente  | Attributi |
|------------|------------|
| Component1 | 0          |
| Component2 | 2          |
| Component3 | 1          |



 

[Tabella collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Icona\_ |
|-----------|--------|
| Shortcut1 | Icon2  |



 

Si noti che i file possono anche essere contrassegnati come compressi usando la proprietà di [**Riepilogo di Word Count**](word-count-summary.md) del [flusso di informazioni di riepilogo](summary-information-stream.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




