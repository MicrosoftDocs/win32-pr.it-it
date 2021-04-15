---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 54 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: ab348a8e-f5df-4e03-a1b7-1ab1a7fbcb3b
title: Tipo di azione personalizzata 54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623e8d4ffe955c73ef95a5948aa6e043702a35f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485492"
---
# <a name="custom-action-type-54"></a>Tipo di azione personalizzata 54

Questa azione personalizzata è scritta in VBScript. Vedere anche [script](scripts.md).

## <a name="source"></a>Source (Sorgente)

Il campo di origine della [tabella CustomAction](customaction-table.md) contiene un nome di proprietà o una chiave per la [tabella](property-table.md) delle proprietà per una proprietà contenente il testo dello script.

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.



| Costanti                                                             | Valore esadecimale | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty** | 0x036       | 54      |



 

Windows Installer possibile utilizzare azioni personalizzate a 64 bit sui sistemi operativi a 64 bit. Un'azione personalizzata a 64 bit basata sugli script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico. Per informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md). Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.



| Costanti                                                                                                    | Valore esadecimale | Decimal |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript** | 0x0001036   | 4150    |



 

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

Un'azione personalizzata scritta in JScript o VBScript richiede l'oggetto [**sessione**](session-object.md) di installazione. Il programma di installazione associa l' **oggetto sessione** allo script con la *sessione* del nome. Poiché l'oggetto **Session** potrebbe non esistere durante il rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione recupero delle [informazioni di contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md) per recuperare il contesto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_Azioni personalizzate](custom-actions.md)
</dt> </dl>

 

 



