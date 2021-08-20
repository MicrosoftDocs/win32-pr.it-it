---
description: Gli sviluppatori di Windows installer possono scegliere di usare un'azione personalizzata di tipo 17 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: Tipo di azione personalizzata 17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c54d19f99c552b731d88ab62926212539381f40e202a044c31a41fd906a7c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947989"
---
# <a name="custom-action-type-17"></a>Tipo di azione personalizzata 17

Questa azione personalizzata chiama una libreria a collegamento dinamico (DLL) scritta in C o C++.

## <a name="source"></a>Source (Sorgente)

La DLL viene installata con l'applicazione durante la sessione corrente. Il campo Source della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella File](file-table.md). Il percorso del codice di azione personalizzata è determinato dalla risoluzione del percorso di destinazione per questo file. pertanto questa azione personalizzata deve essere chiamata dopo che il file è stato installato e prima che venga rimosso.

## <a name="type-value"></a>Valore del tipo

Includere il valore seguente nella colonna Tipo della tabella [CustomAction per](customaction-table.md) specificare il tipo numerico di base.



| Costanti                                                          | Valore esadecimale | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  +  **msidbCustomActionTypeSourceFile** | 0x011       | 17      |



 

## <a name="target"></a>Destinazione

La DLL viene chiamata tramite il punto di ingresso denominato nel campo Target della [tabella CustomAction](customaction-table.md), passando un singolo argomento che rappresenta l'handle alla sessione di installazione corrente. Il nome del punto di ingresso specificato nella tabella deve corrispondere a quello esportato dalla DLL. Si noti che se la funzione entry non è specificata da un oggetto . File DEF o tramite una specifica del linker /EXPORT: il nome può avere un carattere di sottolineatura iniziale e un suffisso " @4 ". La funzione chiamata deve specificare la \_ \_ convenzione di chiamata stdcall.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

Includere i bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di elaborazione restituite. Per una descrizione delle opzioni e dei valori, vedere [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano l'esecuzione multipla di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare un'opzione di esecuzione nello script. Queste opzioni copiano il codice azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Vedere [Valori restituiti dell'azione personalizzata](custom-action-return-values.md).

## <a name="remarks"></a>Commenti

Un'azione personalizzata che chiama una libreria a collegamento dinamico (DLL) richiede un handle per la sessione di installazione. Se si tratta anche di un'azione personalizzata di esecuzione posticipata, la sessione potrebbe non esistere più durante l'esecuzione dello script di installazione. Per informazioni sul modo in cui un'azione personalizzata di questo tipo può ottenere informazioni sul contesto, vedere Recupero di informazioni sul contesto per le azioni personalizzate [di esecuzione posticipata.](obtaining-context-information-for-deferred-execution-custom-actions.md)

Le azioni personalizzate vengono eseguite in un thread separato e possono avere accesso limitato al sistema. Le azioni personalizzate eseguite in modo asincrono bloccano il thread principale alla fine della sequenza corrente o della sessione di installazione fino a quando non vengono restituite.

Le azioni personalizzate che fanno riferimento a un file installato come origine, ad esempio il tipo di azione personalizzata 17 (DLL), devono rispettare le restrizioni di sequenziazione seguenti:

-   L'azione personalizzata deve essere sequenziata dopo [l'azione CostFinalize](costfinalize-action.md). In questo modo l'azione personalizzata può risolvere il percorso necessario per individuare la DLL.
-   Se il file di origine non è già installato nel computer, le azioni personalizzate posticipate (nello script) di questo tipo devono essere sequenziate dopo [l'azione InstallFiles](installfiles-action.md).
-   Se il file di origine non è già installato nel computer, le azioni personalizzate non posticipate di questo tipo devono essere sequenziate dopo [l'azione InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni \_ personalizzate](custom-actions.md)
</dt> <dt>

[Azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md)
</dt> <dt>

[Librerie a collegamento dinamico](dynamic-link-libraries.md)
</dt> </dl>

 

 



