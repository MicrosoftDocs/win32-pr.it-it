---
description: ICE35 verifica che i componenti contenenti file compressi archiviati in un file CAB non siano impostati per l'esecuzione dall'origine. Con Windows Installer 2.0 o versione successiva, questa restrizione è stata rimossa.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee42f97a049b165d41fef7391f0031836865dbf7bafec6b1b5e2fb868e75a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528561"
---
# <a name="ice35"></a>ICE35

ICE35 verifica che i componenti contenenti file compressi archiviati in un [file CAB](cabinet-files.md) non siano impostati per l'esecuzione dall'origine. Con Windows Installer 2.0 o versione successiva, questa restrizione è stata rimossa.

ICE35 esegue una query sulla colonna Cabinet della [tabella Media per](media-table.md) determinare quali file vengono compressi e archiviati in un file CAB. Esegue una query [sulla tabella File](file-table.md) per determinare quali componenti contengono questi file. Infine, controlla la [tabella Component per](component-table.md) determinare se i bit di esecuzione dall'origine sono impostati nella colonna Attributi.

## <a name="result"></a>Risultato

ICE35 invia un messaggio di errore se è presente un file compresso archiviato in un file CAB appartenente a un componente con il bit msidbComponentAttributesSourceOnly impostato nella colonna Attributi della tabella [Component](component-table.md). Con Windows Installer 2.0 o versione successiva, questo viene modificato da errore a messaggio di avviso. Un pacchetto che supporta solo Windows Installer 2.0 e versioni successive ha la proprietà PID PAGECOUNT del flusso di informazioni di riepilogo impostata su un valore di \_ almeno 200.

ICE35 invia un messaggio di avviso se è presente un file compresso archiviato in un file CAB appartenente a un componente con il bit msidbComponentAttributesOptional impostato nella colonna Attributi della tabella [Component](component-table.md). Questo messaggio di avviso è stato rimosso con Windows Installer 2.0 e versioni successive.

Se più file in un componente sono in un file CAB, ICE35 segnala gli errori per ogni file per cui è impostata l'esecuzione dal bit di origine.

## <a name="example"></a>Esempio

ICE35 segnala gli errori e gli avvisi seguenti per l'esempio illustrato usando una versione precedente a Windows Installer versione 2.0.



| Errore ICE35                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRORE: Il componente Component3 non può essere eseguito solo dall'origine perché il relativo file membro 'File3' è compresso. | È presente un file compresso archiviato in un file CAB e questo file appartiene a un componente con il bit SourceOnly impostato nella colonna Attributi della [tabella Component](component-table.md). Per correggere l'errore, modificare i 2 bit inferiori del valore Attributi di Component2 in "00", ovvero Solo locale, oppure rimuovere File4 dal file CAB.<br/>                                                                                                                                                                         |
| ERRORE: Il componente Component3 non può essere eseguito solo dall'origine perché il relativo file membro 'File3' è compresso. | È presente un file compresso archiviato in un file CAB e questo file appartiene a un componente con il bit SourceOnly impostato nella colonna Attributi della [tabella Component](component-table.md). Poiché i file in un componente non devono avere tutti origine dallo stesso supporto, ICE35 segnala gli errori per ogni file nel componente che si trova in un archivio.<br/> Per correggere l'errore, modificare i 2 bit inferiori del valore Attributi di Component2 in "00", ovvero Solo locale, oppure rimuovere File4 dal file CAB.<br/> |



 

[Media Table](media-table.md) (partial)



| DiskID | LastSequence | armadietto   |
|--------|--------------|-----------|
| 1      | 2            |           |
| 2      | 4            | One.cab   |
| 3      | 5            | \#Two.cab |



 

[Tabella file](file-table.md) (parziale)



| File  | Componente\_ | Sequenza |
|-------|-------------|----------|
| File1 | Componente1  | 1        |
| File2 | Componente2  | 2        |
| File3 | Componente2  | 3        |
| File4 | Componente3  | 4        |
| File5 | Componente3  | 5        |



 

[Tabella dei componenti](component-table.md) (parziale)



| Componente  | Attributi |
|------------|------------|
| Componente1 | 0          |
| Componente2 | 2          |
| Componente3 | 1          |



 

[Tabella dei collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Icona\_ |
|-----------|--------|
| Collegamento1 | Icona2  |



 

Si noti che i file possono anche essere contrassegnati come compressi usando la [**proprietà Riepilogo**](word-count-summary.md) conteggio parole del flusso di informazioni [di riepilogo](summary-information-stream.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




