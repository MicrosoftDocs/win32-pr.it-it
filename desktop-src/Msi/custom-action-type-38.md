---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 38 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: bb50fcbf-3de5-4f5a-b799-cec5d68fdd9d
title: Tipo di azione personalizzata 38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9372cd5035d27c02feaef3ed455ddeb756c449
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968018"
---
# <a name="custom-action-type-38"></a>Tipo di azione personalizzata 38

Questa azione personalizzata è scritta in VBScript. Vedere anche [script](scripts.md).

## <a name="source"></a>Source (Sorgente)

Il campo di origine della [tabella CustomAction](customaction-table.md) contiene il valore null. Il codice di script per l'azione personalizzata viene archiviato come una stringa di testo letterale di script nel campo di destinazione.

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.



| Costanti                                                              | Valore esadecimale | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeDirectory** | 0x026       | 38      |



 

Windows Installer possibile utilizzare azioni personalizzate a 64 bit sui sistemi operativi a 64 bit. Un'azione personalizzata a 64 bit basata sugli script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico. Per informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md). Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.



| Costanti                                                                                                     | Valore esadecimale | Decimal |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript** | 0x0001026   | 4134    |



 

## <a name="target"></a>Destinazione

Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene il codice di script per l'azione personalizzata come una stringa di testo di script letterali.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione. Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano la multipla esecuzione di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opzioni di esecuzione In-Script

Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script. Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Questo tipo di azione personalizzata restituisce sempre success.

## <a name="remarks"></a>Commenti

Un'azione personalizzata scritta in JScript o VBScript richiede l'oggetto [**sessione**](session-object.md) di installazione. Il programma di installazione associa l' **oggetto sessione** allo script con il nome "Session". Poiché l'oggetto **Session** potrebbe non esistere durante il rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione recupero delle [informazioni di contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md) per recuperare il contesto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_Azioni personalizzate](custom-actions.md)
</dt> </dl>

 

 



