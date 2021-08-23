---
description: Gli sviluppatori di Windows installer possono scegliere di usare un tipo di azione personalizzata 54 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: ab348a8e-f5df-4e03-a1b7-1ab1a7fbcb3b
title: Tipo di azione personalizzata 54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c206eec715982e1fd23978a04393b6036f77abf4c18807d2e5d43d27755640c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520081"
---
# <a name="custom-action-type-54"></a>Tipo di azione personalizzata 54

Questa azione personalizzata è scritta in VBScript. Vedere anche [Script.](scripts.md)

## <a name="source"></a>Source (Sorgente)

Il campo Source della [tabella CustomAction contiene](customaction-table.md) un nome di proprietà o una chiave per la tabella [Property](property-table.md) per una proprietà contenente il testo dello script.

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.



| Costanti                                                             | Valore esadecimale | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty** | 0x036       | 54      |



 

Windows Il programma di installazione può usare azioni personalizzate a 64 bit nei sistemi operativi a 64 bit. Un'azione personalizzata a 64 bit basata su script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico. Per informazioni, vedere [Azioni personalizzate a 64 bit.](64-bit-custom-actions.md) Includere il valore seguente nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.



| Costanti                                                                                                    | Valore esadecimale | Decimal |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript** | 0x0001036   | 4150    |



 

## <a name="target"></a>Destinazione

Il campo Target della [tabella CustomAction contiene](customaction-table.md) una funzione script facoltativa. L'elaborazione invia prima di tutto lo script per l'analisi e quindi chiama la funzione script facoltativa.

## <a name="return-processing-options"></a>Opzioni di elaborazione dei valori restituiti

Includere bit di flag facoltativi nella colonna Type della [tabella CustomAction per](customaction-table.md) specificare le opzioni di elaborazione restituite. Per una descrizione delle opzioni e dei valori, vedere [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano l'esecuzione multipla di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

Includere bit di flag facoltativi nella colonna Type della [tabella CustomAction per](customaction-table.md) specificare un'opzione di esecuzione nello script. Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Le funzioni facoltative scritte nello script devono restituire uno dei valori descritti in Valori restituiti di [JScript e azioni personalizzate VBScript.](return-values-of-jscript-and-vbscript-custom-actions.md)

## <a name="remarks"></a>Commenti

Un'azione personalizzata scritta in JScript o VBScript richiede l'oggetto [**Session di**](session-object.md) installazione. Il programma di installazione collega **l'oggetto sessione** allo script con il nome *Session*. [Poiché](obtaining-context-information-for-deferred-execution-custom-actions.md) l'oggetto **Session** potrebbe non esistere durante un rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione Recupero di informazioni di contesto per le azioni personalizzate di esecuzione posticipata per recuperarne il contesto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni \_ personalizzate](custom-actions.md)
</dt> </dl>

 

 



