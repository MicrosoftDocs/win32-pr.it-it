---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 22 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 6838f59b-e1bc-42c6-a7fe-3d32791adfac
title: Tipo di azione personalizzata 22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00b4772b1d2532c0291223cc5c4b6a63ead9324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350631"
---
# <a name="custom-action-type-22"></a>Tipo di azione personalizzata 22

Questa azione personalizzata è scritta in VBScript. Vedere anche [script](scripts.md).

## <a name="source"></a>Source (Sorgente)

Lo script viene installato con l'applicazione durante la sessione corrente. Il campo di origine della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella dei file](file-table.md). Il percorso del codice dell'azione personalizzata è determinato dalla risoluzione del percorso di destinazione per il file. Pertanto, questa azione personalizzata deve essere chiamata dopo l'installazione del file e prima della rimozione.

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.



| Costanti                                                               | Valore esadecimale | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeSourceFile** | 0x016       | 22      |



 

Windows Installer possibile utilizzare azioni personalizzate a 64 bit sui sistemi operativi a 64 bit. Un'azione personalizzata a 64 bit basata sugli script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico. Per informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md). Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.



| Costanti                                                                                                      | Valore esadecimale | Decimal |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeSourceFile**  +  **msidbCustomActionType64BitScript** | 0x0001016   | 4118    |



 

## <a name="target"></a>Destinazione

Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene una funzione script facoltativa. L'elaborazione invia innanzitutto lo script per l'analisi e quindi chiama la funzione script facoltativa.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione. Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano la multipla esecuzione di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opzioni di esecuzione In-Script

Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script. Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Le funzioni facoltative scritte nello script devono restituire uno dei valori descritti in [valori restituiti di azioni personalizzate JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).

## <a name="remarks"></a>Commenti

Un'azione personalizzata scritta in JScript o VBScript richiede l' [**oggetto sessione**](session-object.md)di installazione. Si tratta dell' **oggetto Session** del tipo e il programma di installazione lo connette allo script con il nome "Session". Poiché l'oggetto **Session** potrebbe non esistere durante il rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione recupero delle [informazioni di contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md) per recuperare il contesto.

Le azioni personalizzate che fanno riferimento a un file installato come origine, ad esempio il tipo di azione personalizzata 22 (VBcript), devono rispettare le restrizioni di sequenziazione seguenti:

-   L'azione personalizzata deve essere sequenziata dopo l' [azione CostFinalize secondo](costfinalize-action.md). In questo modo l'azione personalizzata può risolvere il percorso necessario per individuare il file di origine contenente VBScript.
-   Se il file di origine non è già installato nel computer, le azioni personalizzate posticipate (in-script) di questo tipo devono essere sequenziate dopo l' [azione InstallFiles](installfiles-action.md).
-   Se il file di origine non è già installato nel computer, le azioni personalizzate non posticipate di questo tipo devono essere sequenziate dopo l' [azione InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_Azioni personalizzate](custom-actions.md)
</dt> </dl>

 

 



