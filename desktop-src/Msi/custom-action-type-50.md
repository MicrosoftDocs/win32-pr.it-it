---
description: Gli sviluppatori di Windows installer possono scegliere di usare un tipo di azione personalizzata 50 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: fc8a875d-21e3-452a-8455-80835b52b256
title: Tipo di azione personalizzata 50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b17c6b512e53bb085c23f6ad0e8af412f6f9de44da3cc70c7153dbef7fb99e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119263251"
---
# <a name="custom-action-type-50"></a>Tipo di azione personalizzata 50

Questa azione personalizzata chiama un eseguibile avviato con una riga di comando.

Vedere anche [File eseguibili](executable-files.md).

## <a name="source"></a>Source (Sorgente)

L'eseguibile viene generato da un file esistente. Il campo Source della [tabella CustomAction](customaction-table.md) contiene una chiave per la tabella [Property](property-table.md) per una proprietà che contiene il percorso completo del file eseguibile.

## <a name="type-value"></a>Valore del tipo

Includere il valore seguente nella colonna Tipo della tabella [CustomAction per](customaction-table.md) specificare il tipo numerico di base.



| Costanti                                                        | Valore esadecimale | Decimal |
|------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty** | 0x032       | 50      |



 

## <a name="target"></a>Destinazione

La colonna Target della [tabella CustomAction contiene](customaction-table.md) la stringa della riga di comando per il file eseguibile identificato nella colonna Source.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

Includere i bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di elaborazione restituite. Per una descrizione delle opzioni e dei valori, vedere [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere i bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano l'esecuzione multipla di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare un'opzione di esecuzione nello script. Queste opzioni copiano il codice azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Le azioni personalizzate che sono [file eseguibili](executable-files.md) devono restituire il valore 0 per l'esito positivo. Il programma di installazione interpreta qualsiasi altro valore restituito come errore. Per ignorare i valori restituiti, impostare il flag di bit **msidbCustomActionTypeContinue** nel campo Tipo della tabella CustomAction.

## <a name="remarks"></a>Commenti

Un'azione personalizzata che avvia un eseguibile accetta una riga di comando, che in genere contiene proprietà designate in modo dinamico. Se si tratta [](deferred-execution-custom-actions.md)anche di un'azione personalizzata di esecuzione posticipata, il programma di installazione usa CreateProcessAsUser o CreateProcess per creare il processo quando l'azione personalizzata viene richiamata dallo script di installazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni \_ personalizzate](custom-actions.md)
</dt> </dl>

 

 



