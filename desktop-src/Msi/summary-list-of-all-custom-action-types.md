---
description: La tabella seguente identifica i tipi di base di azioni personalizzate e Mostra i valori presenti nei campi tipo, origine e destinazione della tabella CustomAction per ogni tipo.
ms.assetid: 8713451e-c0e7-4bec-bfb6-dfe4125d5a44
title: Tipi di azione personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5b10ffd42d2f6fecf06e0732a8960c84bea2e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885101"
---
# <a name="custom-action-types"></a>Tipi di azione personalizzati

La tabella seguente identifica i tipi di base di azioni personalizzate e Mostra i valori presenti nei campi tipo, origine e destinazione della tabella [CustomAction](customaction-table.md) per ogni tipo. Le azioni personalizzate di base possono essere modificate includendo bit di flag facoltativi nella colonna tipo. Per le descrizioni delle opzioni e dei valori, vedere gli argomenti seguenti:

-   [Opzioni di elaborazione della restituzione dell'azione personalizzata](custom-action-return-processing-options.md)
-   [Opzioni di pianificazione dell'esecuzione di azioni personalizzate](custom-action-execution-scheduling-options.md)
-   [Opzioni di esecuzione In-Script azione personalizzata](custom-action-in-script-execution-options.md)
-   [Opzione di disinstallazione patch azione personalizzata](custom-action-patch-uninstall-option.md)

Usare i collegamenti al tipo di azione personalizzata di base per una descrizione e le opzioni disponibili per ogni tipo.



| Tipo di azione personalizzata di base                                                                                                                           | Tipo | Source (Sorgente)                                                                                                                              | Destinazione                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipo di azione personalizzata 1](custom-action-type-1.md) File DLL archiviato in un flusso di tabella binario.<br/>                                               | 1    | Da chiave a tabella [binaria](binary-table.md) .                                                                                            | Punto di ingresso della DLL.                                                                                                                           |
| [Tipo di azione personalizzata 2](custom-action-type-2.md) File EXE archiviato in un flusso di tabella binario.<br/>                                               | 2    | Da chiave a tabella [binaria](binary-table.md) .                                                                                            | Stringa della riga di comando.                                                                                                                       |
| [Tipo di azione personalizzata 5](custom-action-type-5.md) File JScript archiviato in un flusso di tabella binario.<br/>                                           | 5    | Da chiave a tabella [binaria](binary-table.md) .                                                                                            | Funzione JScript facoltativa che può essere chiamata.                                                                                           |
| [Tipo di azione personalizzata 6](custom-action-type-6.md) File VBScript archiviato in un flusso di tabella binario.<br/>                                          | 6    | Da chiave a tabella [binaria](binary-table.md) .                                                                                            | Funzione VBScript facoltativa che può essere chiamata.                                                                                          |
| [Tipo di azione personalizzata 17](custom-action-type-17.md) File DLL installato con un prodotto.<br/>                                            | 17   | Da chiave a tabella [file](file-table.md) .                                                                                                | Punto di ingresso della DLL.                                                                                                                           |
| [Tipo di azione personalizzata 18](custom-action-type-18.md) File EXE installato con un prodotto.<br/>                                            | 18   | Da chiave a tabella [file](file-table.md) .                                                                                                | Stringa della riga di comando.                                                                                                                       |
| [Tipo di azione personalizzata 19](custom-action-type-19.md) Visualizza un messaggio di errore specificato e restituisce un errore, terminando l'installazione.<br/> | 19   | Vuoto                                                                                                                               | Stringa di testo [formattato](formatted.md) . Messaggio letterale o indice nella tabella degli [errori](error-table.md) .                           |
| [Tipo di azione personalizzata 21](custom-action-type-21.md) File JScript installato con un prodotto.<br/>                                        | 21   | Da chiave a tabella [file](file-table.md) .                                                                                                | Funzione JScript facoltativa che può essere chiamata.                                                                                           |
| [Tipo di azione personalizzata 22](custom-action-type-22.md) File VBScript installato con un prodotto.<br/>                                       | 22   | Da chiave a tabella [file](file-table.md) .                                                                                                | Funzione VBScript facoltativa che può essere chiamata.                                                                                          |
| [Tipo di azione personalizzata 34](custom-action-type-34.md) File EXE con un percorso che fa riferimento a una directory.<br/>                                       | 34   | Chiave per la tabella [directory](directory-table.md) . Si tratta della directory di lavoro per l'esecuzione.                                         | La colonna di destinazione è [formattata](formatted.md) e contiene il percorso completo e il nome del file eseguibile seguito da argomenti facoltativi. |
| [Tipo di azione personalizzata 35](custom-action-type-35.md) Set di directory con testo formattato.<br/>                                                    | 35   | Chiave per la tabella di [directory](directory-table.md) . La directory designata viene impostata dalla stringa formattata nel campo di destinazione.   | Stringa di testo formattato.                                                                                                                   |
| [Tipo di azione personalizzata 37](custom-action-type-37.md) Testo JScript archiviato in questa tabella di sequenza.<br/>                                           | 37   | Null                                                                                                                                | Stringa di codice JScript.                                                                                                                  |
| [Tipo di azione personalizzata 38](custom-action-type-38.md) Testo VBScript archiviato in questa tabella di sequenza.<br/>                                          | 38   | Null                                                                                                                                | Stringa di codice VBScript.                                                                                                                 |
| [Tipo di azione personalizzata 50](custom-action-type-50.md) File EXE con un percorso specificato da un valore della proprietà.<br/>                                 | 50   | Nome o chiave della proprietà nella tabella delle [Proprietà](property-table.md) .                                                                       | Stringa della riga di comando.                                                                                                                       |
| [Tipo di azione personalizzata 51](custom-action-type-51.md) Set di proprietà con testo formattato.<br/>                                                     | 51   | Nome o chiave della proprietà nella tabella delle [Proprietà](property-table.md) . Questa proprietà viene impostata dalla stringa formattata nel campo di destinazione. | Stringa di testo formattato.                                                                                                                   |
| [Tipo di azione personalizzata 53](custom-action-type-53.md) Testo JScript specificato da un valore della proprietà.<br/>                                           | 53   | Nome o chiave della proprietà nella tabella delle [Proprietà](property-table.md) .                                                                       | Funzione JScript facoltativa che può essere chiamata.                                                                                           |
| [Tipo di azione personalizzata 54](custom-action-type-54.md) Testo VBScript specificato da un valore della proprietà.<br/>                                          | 54   | Nome o chiave della proprietà nella tabella delle [Proprietà](property-table.md) .                                                                       | Funzione VBScript facoltativa che può essere chiamata.                                                                                          |



 

Inoltre, con le installazioni simultanee vengono usati i tipi di azione personalizzati seguenti:

-   [Tipo di azione personalizzata 7](custom-action-type-7.md)
-   [Tipo di azione personalizzata 23](custom-action-type-23.md)
-   [Tipo di azione personalizzata 39](custom-action-type-39.md)

 

 




