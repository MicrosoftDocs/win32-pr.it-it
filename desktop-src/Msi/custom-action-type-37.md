---
description: Gli sviluppatori di Windows installer possono scegliere di usare un'azione personalizzata di tipo 37 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 1c1e4f4f-1ccb-444c-940a-a1963d97714d
title: Tipo di azione personalizzata 37
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1595279d2c8f66e1b899ad88ad6a9d5c164c2727b5c905ce66700479ed32446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996820"
---
# <a name="custom-action-type-37"></a>Tipo di azione personalizzata 37

Questa azione personalizzata è scritta in JScript, ad esempio ECMA 262. Windows Il programma di installazione non supporta JScript 1.0. Per altre informazioni, vedere [Script.](scripts.md)

## <a name="source"></a>Source (Sorgente)

Il campo Source della [tabella CustomAction contiene](customaction-table.md) il valore Null. Il codice script per l'azione personalizzata viene archiviato come stringa di testo dello script letterale nel campo Destinazione.

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.



| Costanti                                                             | Valore esadecimale | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory** | 0x025       | 37      |



 

Windows Il programma di installazione può usare azioni personalizzate a 64 bit nei sistemi operativi a 64 bit. Un'azione personalizzata a 64 bit basata su script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico. Per informazioni, vedere [Azioni personalizzate a 64 bit.](64-bit-custom-actions.md) Includere il valore seguente nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.



| Costanti                                                                                                    | Valore esadecimale | Decimal |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript** | 0x0001025   | 4133    |



 

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

 

 



