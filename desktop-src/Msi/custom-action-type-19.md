---
description: Gli sviluppatori di Windows installer possono scegliere di usare un'azione personalizzata di tipo 19 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Tipo di azione personalizzata 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cbbef4ec07d805e41c0de25c371f995782ce3d8df66a89ee93363afa05f55b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075061"
---
# <a name="custom-action-type-19"></a>Tipo di azione personalizzata 19

Questa azione personalizzata visualizza un messaggio di errore specificato, restituisce un errore e quindi termina l'installazione. Il messaggio di errore visualizzato può essere fornito come stringa o come indice nella [tabella Error](error-table.md).

## <a name="source"></a>Source (Sorgente)

Lasciare vuota la colonna Source [della tabella CustomAction.](customaction-table.md)

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della tabella CustomAction per specificare il tipo numerico di base.



| Costanti                                                               | Valore esadecimale | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeSourceFile** | 0x013       | 19      |



 

## <a name="target"></a>Destinazione

La colonna Target della [tabella CustomAction](customaction-table.md) contiene una stringa di testo formattata usando la funzionalità specificata in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (senza gli identificatori di campo numerico). I parametri da sostituire sono racchiusi tra parentesi quadre, ... e possono essere proprietà, variabili di ambiente (prefisso %), percorsi di file (prefisso) o percorsi di \[ \] directory dei componenti \# (prefisso $). Se dopo la formattazione della stringa viene restituito un numero intero, tale intero viene utilizzato come indice nella tabella [Error](error-table.md) per recuperare il messaggio da visualizzare. Se dopo la formattazione della stringa sono contenuti caratteri non numerici, la stringa stessa viene visualizzata come messaggio.

## <a name="return-processing-options"></a>Opzioni di elaborazione dei valori restituiti

L'azione personalizzata non usa alcuna opzione.

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

L'azione personalizzata non usa alcuna opzione.

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

L'azione personalizzata non usa alcuna opzione.

## <a name="return-values"></a>Valori restituiti

Vedere [Valori restituiti dell'azione personalizzata.](custom-action-return-values.md)

## <a name="remarks"></a>Commenti

Ad esempio, le azioni personalizzate CAError1, CAError2, CAError3 e CAError4 restituiscono questi messaggi.

[Tabella CustomAction](customaction-table.md)



| Azione   | Tipo | Source (Sorgente) | Destinazione                              |
|----------|------|--------|-------------------------------------|
| ERRORE CA1 | 19   |        | \[Prop1\]                           |
| ERRORE CA2 | 19   |        | Errore di installazione a causa dell'errore 2. |
| Errore CA3 | 19   |        | 25000                               |
| ERRORE CA4 | 19   |        | \[Prop2\]                           |



 

[Tabella delle proprietà](property-table.md)



| Proprietà | Valore                                 |
|----------|---------------------------------------|
| Prop1    | "Errore di installazione causato da Error1". |
| Prop2    | "25100"                               |



 

[Tabella degli errori](error-table.md)



| Codice  | Message                             |
|-------|-------------------------------------|
| 25000 | Errore di installazione a causa dell'errore 3. |
| 25100 | Errore di installazione a causa dell'errore 4. |



 

Queste azioni personalizzate restituiscono i messaggi di errore seguenti:



| Azione personalizzata | Stringa di messaggio restituita             |
|---------------|-------------------------------------|
| ERRORE CA1      | Errore di installazione dovuto a Error1. |
| ERRORE CA2      | Errore di installazione a causa dell'errore 2. |
| Errore CA3      | Errore di installazione a causa dell'errore 3. |
| ERRORE CA4      | Errore di installazione a causa dell'errore 4. |



 

Si noti che poiché l'ordine di valutazione delle condizioni di avvio non può essere garantito mediante la creazione della tabella [LaunchCondition](launchcondition-table.md), è consigliabile usare azioni personalizzate di tipo azione personalizzata 19 nell'installazione per valutare le condizioni in un ordine specifico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni \_ personalizzate](custom-actions.md)
</dt> </dl>

 

 



