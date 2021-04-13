---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 17 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: Tipo di azione personalizzata 17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53d0046cb7515d701eb1bae3d10de0570ee5843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349001"
---
# <a name="custom-action-type-17"></a>Tipo di azione personalizzata 17

Questa azione personalizzata chiama una libreria a collegamento dinamico (DLL) scritta in C o C++.

## <a name="source"></a>Source (Sorgente)

La DLL viene installata con l'applicazione durante la sessione corrente. Il campo di origine della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella dei file](file-table.md). Il percorso del codice dell'azione personalizzata è determinato dalla risoluzione del percorso di destinazione per il file. di conseguenza, questa azione personalizzata deve essere chiamata dopo che il file è stato installato e prima che venga rimosso.

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base.



| Costanti                                                          | Valore esadecimale | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  +  **msidbCustomActionTypeSourceFile** | 0x011       | 17      |



 

## <a name="target"></a>Destinazione

La DLL viene chiamata tramite il punto di ingresso denominato nel campo di destinazione della [tabella CustomAction](customaction-table.md), passando un solo argomento che rappresenta l'handle della sessione di installazione corrente. Il nome del punto di ingresso specificato nella tabella deve corrispondere a quello esportato dalla DLL. Si noti che se la funzione entry non è specificata da un oggetto. File DEF o con una specifica/EXPORT: linker, il nome può avere un carattere di sottolineatura e un @4 suffisso "". La funzione chiamata deve specificare la \_ \_ convenzione di chiamata stdcall.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione. Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano la multipla esecuzione di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opzioni di esecuzione In-Script

Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script. Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Vedere [valori restituiti dell'azione personalizzata](custom-action-return-values.md).

## <a name="remarks"></a>Commenti

Un'azione personalizzata che chiama una libreria a collegamento dinamico (DLL) richiede un handle per la sessione di installazione. Se si tratta anche di un'azione personalizzata di esecuzione posticipata, la sessione potrebbe non esistere più durante l'esecuzione dello script di installazione. Per informazioni sul modo in cui un'azione personalizzata di questo tipo può ottenere informazioni sul contesto, vedere [ottenere informazioni sul contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md).

Le azioni personalizzate vengono eseguite in un thread separato e possono avere accesso limitato al sistema. Le azioni personalizzate che vengono eseguite in modo asincrono bloccano il thread principale alla chiusura della sequenza corrente o della sessione di installazione fino a quando non vengono restituite.

Le azioni personalizzate che fanno riferimento a un file installato come origine, ad esempio il tipo di azione personalizzato 17 (DLL), devono rispettare le restrizioni di sequenziazione seguenti:

-   L'azione personalizzata deve essere sequenziata dopo l' [azione CostFinalize secondo](costfinalize-action.md). In questo modo l'azione personalizzata può risolvere il percorso necessario per individuare la DLL.
-   Se il file di origine non è già installato nel computer, le azioni personalizzate posticipate (in-script) di questo tipo devono essere sequenziate dopo l' [azione InstallFiles](installfiles-action.md).
-   Se il file di origine non è già installato nel computer, le azioni personalizzate non posticipate di questo tipo devono essere sequenziate dopo l' [azione InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_Azioni personalizzate](custom-actions.md)
</dt> <dt>

[Azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md)
</dt> <dt>

[Librerie a collegamento dinamico](dynamic-link-libraries.md)
</dt> </dl>

 

 



