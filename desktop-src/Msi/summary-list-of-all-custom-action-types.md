---
description: La tabella seguente identifica i tipi di base delle azioni personalizzate e mostra i valori presenti nei campi Tipo, Origine e Destinazione della tabella CustomAction per ogni tipo.
ms.assetid: 8713451e-c0e7-4bec-bfb6-dfe4125d5a44
title: Tipi di azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf0be8a9465c9a3567a867bab911d7539e8700219515c86bb5a8fc2b7d5eff68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624306"
---
# <a name="custom-action-types"></a>Tipi di azione personalizzata

La tabella seguente identifica i tipi di base delle azioni personalizzate e mostra i valori presenti nei campi Tipo, Origine e Destinazione della [tabella CustomAction](customaction-table.md) per ogni tipo. Le azioni personalizzate di base possono essere modificate includendo bit di flag facoltativi nella colonna Tipo. Per le descrizioni delle opzioni e dei valori, vedere quanto segue:

-   [Opzioni di elaborazione per la restituzione di azioni personalizzate](custom-action-return-processing-options.md)
-   [Opzioni di pianificazione dell'esecuzione di azioni personalizzate](custom-action-execution-scheduling-options.md)
-   [Opzioni di esecuzione In-Script azioni personalizzate](custom-action-in-script-execution-options.md)
-   [Opzione di disinstallazione della patch per azioni personalizzate](custom-action-patch-uninstall-option.md)

Usare i collegamenti al tipo di azione personalizzata di base per una descrizione e le opzioni disponibili per ogni tipo.



| Tipo di azione personalizzata di base                                                                                                                           | Tipo | Source (Sorgente)                                                                                                                              | Destinazione                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipo di azione personalizzata 1](custom-action-type-1.md) File DLL archiviato in un flusso di tabella binario.<br/>                                               | 1    | Chiave per [la tabella binaria.](binary-table.md)                                                                                            | Punto di ingresso DLL.                                                                                                                           |
| [Tipo di azione personalizzata 2](custom-action-type-2.md) File EXE archiviato in un flusso di tabella binario.<br/>                                               | 2    | Chiave per [la tabella binaria.](binary-table.md)                                                                                            | Stringa della riga di comando.                                                                                                                       |
| [Azione personalizzata Digitare 5 JScript](custom-action-type-5.md)file archiviato in un flusso di tabella binario.<br/>                                           | 5    | Chiave per [la tabella binaria.](binary-table.md)                                                                                            | Funzione JScript facoltativa che può essere chiamata.                                                                                           |
| [Tipo di azione personalizzata 6](custom-action-type-6.md) File VBScript archiviato in un flusso di tabella binario.<br/>                                          | 6    | Chiave per [la tabella binaria.](binary-table.md)                                                                                            | Funzione VBScript facoltativa che può essere chiamata.                                                                                          |
| [Tipo di azione personalizzata 17](custom-action-type-17.md) File DLL installato con un prodotto.<br/>                                            | 17   | Chiave della [tabella File.](file-table.md)                                                                                                | Punto di ingresso DLL.                                                                                                                           |
| [Tipo di azione personalizzata 18](custom-action-type-18.md) FILE EXE installato con un prodotto.<br/>                                            | 18   | Chiave della [tabella File.](file-table.md)                                                                                                | Stringa della riga di comando.                                                                                                                       |
| [Tipo di azione personalizzata 19](custom-action-type-19.md) Visualizza un messaggio di errore specificato e restituisce un errore, terminando l'installazione.<br/> | 19   | Vuoto                                                                                                                               | [Stringa di testo](formatted.md) formattata. Messaggio letterale o indice nella [tabella Error.](error-table.md)                           |
| [Azione personalizzata Digitare 21](custom-action-type-21.md)JScript file installato con un prodotto.<br/>                                        | 21   | Chiave della [tabella File.](file-table.md)                                                                                                | Funzione JScript facoltativa che può essere chiamata.                                                                                           |
| [Tipo di azione personalizzata 22](custom-action-type-22.md) File VBScript installato con un prodotto.<br/>                                       | 22   | Chiave della [tabella File.](file-table.md)                                                                                                | Funzione VBScript facoltativa che può essere chiamata.                                                                                          |
| [Tipo di azione personalizzata 34](custom-action-type-34.md) File EXE con un percorso che fa riferimento a una directory.<br/>                                       | 34   | Chiave della [tabella Directory.](directory-table.md) Si tratta della directory di lavoro per l'esecuzione.                                         | La colonna Target è [formattata](formatted.md) e contiene il percorso completo e il nome del file eseguibile seguito da argomenti facoltativi. |
| [Tipo di azione personalizzata 35](custom-action-type-35.md) Directory impostata con testo formattato.<br/>                                                    | 35   | Chiave della [tabella Directory.](directory-table.md) La directory designata viene impostata dalla stringa formattata nel campo Destinazione.   | Stringa di testo formattata.                                                                                                                   |
| [Azione personalizzata Digitare 37 JScript](custom-action-type-37.md)testo archiviato in questa tabella di sequenza.<br/>                                           | 37   | Null                                                                                                                                | Stringa di JScript codice.                                                                                                                  |
| [Tipo di azione personalizzata 38](custom-action-type-38.md) Testo VBScript archiviato in questa tabella di sequenza.<br/>                                          | 38   | Null                                                                                                                                | Stringa di codice VBScript.                                                                                                                 |
| [Tipo di azione personalizzata 50](custom-action-type-50.md) FILE EXE con un percorso specificato da un valore di proprietà.<br/>                                 | 50   | Nome della proprietà o chiave della [tabella](property-table.md) Property.                                                                       | Stringa della riga di comando.                                                                                                                       |
| [Tipo di azione personalizzata 51](custom-action-type-51.md) Proprietà impostata con testo formattato.<br/>                                                     | 51   | Nome della proprietà o chiave della [tabella](property-table.md) Property. Questa proprietà viene impostata dalla stringa formattata nel campo Destinazione. | Stringa di testo formattata.                                                                                                                   |
| [Tipo di azione personalizzata 53](custom-action-type-53.md)JScript testo specificato da un valore di proprietà.<br/>                                           | 53   | Nome della proprietà o chiave della [tabella](property-table.md) Property.                                                                       | Funzione JScript facoltativa che può essere chiamata.                                                                                           |
| [Tipo di azione personalizzata 54](custom-action-type-54.md) Testo VBScript specificato da un valore di proprietà.<br/>                                          | 54   | Nome della proprietà o chiave della [tabella](property-table.md) Property.                                                                       | Funzione VBScript facoltativa che può essere chiamata.                                                                                          |



 

Inoltre, con le installazioni simultanee vengono usati i tipi di azione personalizzati seguenti:

-   [Tipo di azione personalizzata 7](custom-action-type-7.md)
-   [Tipo di azione personalizzata 23](custom-action-type-23.md)
-   [Tipo di azione personalizzata 39](custom-action-type-39.md)

 

 




