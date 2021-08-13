---
description: Gli sviluppatori di Windows installer possono scegliere di usare un'azione personalizzata di tipo 22 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 6838f59b-e1bc-42c6-a7fe-3d32791adfac
title: Tipo di azione personalizzata 22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fe14690ec1d966abfe1ead0b7856360270570f30e2aaf2e93ea81181962ec8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637905"
---
# <a name="custom-action-type-22"></a>Tipo di azione personalizzata 22

Questa azione personalizzata è scritta in VBScript. Vedere anche [Script.](scripts.md)

## <a name="source"></a>Source (Sorgente)

Lo script viene installato con l'applicazione durante la sessione corrente. Il campo Source della [tabella CustomAction contiene](customaction-table.md) una chiave per la [tabella File](file-table.md). Il percorso del codice dell'azione personalizzata è determinato dalla risoluzione del percorso di destinazione per questo file. pertanto questa azione personalizzata deve essere chiamata dopo l'installazione del file e prima della rimozione.

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.



| Costanti                                                               | Valore esadecimale | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeSourceFile** | 0x016       | 22      |



 

Windows Il programma di installazione può usare azioni personalizzate a 64 bit nei sistemi operativi a 64 bit. Un'azione personalizzata a 64 bit basata su script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico. Per informazioni, vedere [Azioni personalizzate a 64 bit.](64-bit-custom-actions.md) Includere il valore seguente nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.



| Costanti                                                                                                      | Valore esadecimale | Decimal |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeSourceFile**  +  **msidbCustomActionType64BitScript** | 0x0001016   | 4118    |



 

## <a name="target"></a>Destinazione

Il campo Target della [tabella CustomAction contiene](customaction-table.md) una funzione script facoltativa. L'elaborazione invia prima di tutto lo script per l'analisi e quindi chiama la funzione script facoltativa.

## <a name="return-processing-options"></a>Opzioni di elaborazione dei valori restituiti

Includere bit di flag facoltativi nella colonna Type della [tabella CustomAction per](customaction-table.md) specificare le opzioni di elaborazione restituite. Per una descrizione delle opzioni e dei valori, vedere [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano l'esecuzione multipla di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

Includere bit di flag facoltativi nella colonna Type della [tabella CustomAction per](customaction-table.md) specificare un'opzione di esecuzione nello script. Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Le funzioni facoltative scritte nello script devono restituire uno dei valori descritti in Valori restituiti di JScript [e azioni personalizzate VBScript.](return-values-of-jscript-and-vbscript-custom-actions.md)

## <a name="remarks"></a>Commenti

Un'azione personalizzata scritta in JScript o VBScript richiede l'installazione [**dell'oggetto sessione**](session-object.md). Questo è di tipo **Oggetto sessione e** il programma di installazione lo collega allo script con il nome "Session". [Poiché](obtaining-context-information-for-deferred-execution-custom-actions.md) l'oggetto **Session** potrebbe non esistere durante un rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione Recupero di informazioni di contesto per le azioni personalizzate di esecuzione posticipata per recuperarne il contesto.

Le azioni personalizzate che fanno riferimento a un file installato come origine, ad esempio Custom Action Type 22 (VBcript), devono rispettare le restrizioni di sequenziazione seguenti:

-   L'azione personalizzata deve essere sequenziata dopo [l'azione CostFinalize](costfinalize-action.md). In questo modo l'azione personalizzata può risolvere il percorso necessario per individuare il file di origine contenente VBScript.
-   Se il file di origine non è già installato nel computer, le azioni personalizzate posticipate (nello script) di questo tipo devono essere sequenziate dopo [l'azione InstallFiles](installfiles-action.md).
-   Se il file di origine non è già installato nel computer, le azioni personalizzate non posticipate di questo tipo devono essere sequenziate dopo l'azione [InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni \_ personalizzate](custom-actions.md)
</dt> </dl>

 

 



