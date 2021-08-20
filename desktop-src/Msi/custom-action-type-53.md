---
description: Gli sviluppatori di Windows pacchetti del programma di installazione possono scegliere di usare un tipo di azione personalizzata 53 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: d024c73e-c2dc-4187-a8ae-ed96dc7c107e
title: Tipo di azione personalizzata 53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b78c2dbc8aa233175eeacfa8d16521968dfceeb6b97504e639946c6284b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947892"
---
# <a name="custom-action-type-53"></a>Tipo di azione personalizzata 53

Questa azione personalizzata è scritta in JScript, ad esempio ECMA 262. Windows Il programma di installazione non supporta JScript 1.0. Per altre informazioni, vedere [Script](scripts.md).

## <a name="source"></a>Source (Sorgente)

Il campo Source della [tabella CustomAction](customaction-table.md) contiene un nome di proprietà o una chiave per la tabella [Property](property-table.md) per una proprietà contenente il testo dello script.

## <a name="type-value"></a>Valore del tipo

Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.



| Costanti                                                            | Valore esadecimale | Decimal |
|----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **MsidbCustomActionTypeProperty** | 0x035       | 53      |



 

Windows Il programma di installazione può usare azioni personalizzate a 64 bit nei sistemi operativi a 64 bit. Un'azione personalizzata a 64 bit basata su script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico. Per informazioni, vedere [Azioni personalizzate a 64 bit.](64-bit-custom-actions.md) Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.



| Costanti                                                                                                   | Valore esadecimale | Decimal |
|-------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript** | 0x0001035   | 4149    |



 

## <a name="target"></a>Destinazione

Il campo Target della [tabella CustomAction contiene](customaction-table.md) una funzione script facoltativa. L'elaborazione invia prima lo script per l'analisi e quindi chiama la funzione script facoltativa.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

Includere i bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di elaborazione restituite. Per una descrizione delle opzioni e dei valori, vedere [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano l'esecuzione multipla di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare un'opzione di esecuzione nello script. Queste opzioni copiano il codice azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Le funzioni facoltative scritte nello script devono restituire uno dei valori descritti in Valori restituiti di JScript [e azioni personalizzate VBScript.](return-values-of-jscript-and-vbscript-custom-actions.md)

## <a name="remarks"></a>Commenti

Un'azione personalizzata scritta in JScript richiede l'oggetto [**Session di**](session-object.md) installazione. Poiché **l'oggetto Session** potrebbe non esistere durante un rollback dell'installazione, un'azione personalizzata posticipata scritta nello script usa uno dei metodi descritti in Ottenere informazioni di contesto per le azioni personalizzate di esecuzione [posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni \_ personalizzate](custom-actions.md)
</dt> </dl>

 

 



