---
description: Gli sviluppatori di Windows installer possono scegliere di usare un'azione personalizzata di tipo 38 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: bb50fcbf-3de5-4f5a-b799-cec5d68fdd9d
title: Tipo di azione personalizzata 38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361da558a6b1cf9d483d5cdb84d3a4290f9d25fb88ed844d564a26228378a14e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947942"
---
# <a name="custom-action-type-38"></a>Tipo di azione personalizzata 38

Questa azione personalizzata è scritta in VBScript. Vedere anche [Script.](scripts.md)

## <a name="source"></a>Source (Sorgente)

Il campo Source della [tabella CustomAction contiene](customaction-table.md) il valore Null. Il codice script per l'azione personalizzata viene archiviato come stringa di testo dello script letterale nel campo Destinazione.

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.



| Costanti                                                              | Valore esadecimale | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeDirectory** | 0x026       | 38      |



 

Windows Il programma di installazione può usare azioni personalizzate a 64 bit nei sistemi operativi a 64 bit. Un'azione personalizzata a 64 bit basata su script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico. Per informazioni, vedere [Azioni personalizzate a 64 bit.](64-bit-custom-actions.md) Includere il valore seguente nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.



| Costanti                                                                                                     | Valore esadecimale | Decimal |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript** | 0x0001026   | 4134    |



 

## <a name="target"></a>Destinazione

Il campo Target della tabella [CustomAction contiene](customaction-table.md) il codice script per l'azione personalizzata sotto forma di stringa di testo letterale dello script.

## <a name="return-processing-options"></a>Opzioni di elaborazione dei valori restituiti

Includere bit di flag facoltativi nella colonna Type della [tabella CustomAction per](customaction-table.md) specificare le opzioni di elaborazione restituite. Per una descrizione delle opzioni e dei valori, vedere [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano l'esecuzione multipla di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

Includere bit di flag facoltativi nella colonna Type della [tabella CustomAction per](customaction-table.md) specificare un'opzione di esecuzione nello script. Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Questo tipo di azione personalizzata restituisce sempre l'esito positivo.

## <a name="remarks"></a>Commenti

Un'azione personalizzata scritta in JScript o VBScript richiede l'oggetto [**Session di**](session-object.md) installazione. Il programma di installazione collega **l'oggetto sessione** allo script con il nome "Session". [Poiché](obtaining-context-information-for-deferred-execution-custom-actions.md) l'oggetto **Session** potrebbe non esistere durante un rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione Recupero di informazioni di contesto per le azioni personalizzate di esecuzione posticipata per recuperarne il contesto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni \_ personalizzate](custom-actions.md)
</dt> </dl>

 

 



