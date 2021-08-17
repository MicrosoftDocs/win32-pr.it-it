---
description: Gli sviluppatori Windows pacchetti del programma di installazione possono scegliere di usare un'azione personalizzata di tipo 18 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 8a7311a6-41c6-431e-982d-60bacf06454e
title: Tipo di azione personalizzata 18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3befbb614e9ee78961cf5b8ef969bdb3d6e7b6c0cb713a267cab3d09b4588d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379277"
---
# <a name="custom-action-type-18"></a>Tipo di azione personalizzata 18

Questa azione personalizzata chiama un eseguibile avviato con una riga di comando.

## <a name="source"></a>Source (Sorgente)

L'eseguibile viene generato da un file installato con l'applicazione. Il campo Source della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella File](file-table.md). Il percorso del codice di azione personalizzata è determinato dalla risoluzione del percorso di destinazione per questo file. pertanto questa azione personalizzata deve essere chiamata dopo l'installazione del file e prima della rimozione.

## <a name="type-value"></a>Valore del tipo

Includere il valore seguente nella colonna Tipo della tabella [CustomAction per](customaction-table.md) specificare il tipo numerico di base.



| Costanti                                                          | Valore esadecimale | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile** | 0x012       | 18      |



 

## <a name="target"></a>Destinazione

La colonna Target della [tabella CustomAction contiene](customaction-table.md) la stringa della riga di comando per il file eseguibile identificato nella colonna Source.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

Includere i bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di elaborazione restituite. Per una descrizione delle opzioni e dei valori, vedere [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano l'esecuzione multipla di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare un'opzione di esecuzione nello script. Queste opzioni copiano il codice azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Le azioni personalizzate che sono [file eseguibili](executable-files.md) devono restituire il valore 0 per l'esito positivo. Il programma di installazione interpreta qualsiasi altro valore restituito come errore. Per ignorare i valori restituiti, impostare il flag di bit **msidbCustomActionTypeContinue** nel campo Tipo della tabella CustomAction.

## <a name="remarks"></a>Commenti

Un'azione personalizzata che avvia un eseguibile accetta una riga di comando, che in genere contiene proprietà designate dinamicamente. Se si tratta [](deferred-execution-custom-actions.md)anche di un'azione personalizzata di esecuzione posticipata, il programma di installazione usa [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) per creare il processo quando l'azione personalizzata viene richiamata dallo script di installazione.

Le azioni personalizzate che fanno riferimento a un file installato come origine, ad esempio il tipo di azione personalizzata 18 (EXE), devono rispettare le restrizioni di sequenziazione seguenti:

-   L'azione personalizzata deve essere sequenziata dopo [l'azione CostFinalize](costfinalize-action.md). In questo modo l'azione personalizzata può risolvere il percorso necessario per individuare il file EXE.
-   Se il file di origine non è già installato nel computer, le azioni personalizzate posticipate (nello script) di questo tipo devono essere sequenziate dopo [l'azione InstallFiles](installfiles-action.md).
-   Se il file di origine non è già installato nel computer, le azioni personalizzate non posticipate di questo tipo devono essere sequenziate dopo [l'azione InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni \_ personalizzate](custom-actions.md)
</dt> <dt>

[File eseguibili](executable-files.md)
</dt> </dl>

 

 
