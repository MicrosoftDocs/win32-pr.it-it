---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 19 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Tipo di azione personalizzata 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695f86db0848bd65884ce5e233b4d9a249275c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319973"
---
# <a name="custom-action-type-19"></a>Tipo di azione personalizzata 19

Questa azione personalizzata Visualizza un messaggio di errore specificato, restituisce un errore e quindi termina l'installazione. Il messaggio di errore visualizzato può essere fornito come stringa o come indice nella tabella degli [errori](error-table.md).

## <a name="source"></a>Source (Sorgente)

Lasciare vuota la colonna di origine della [tabella CustomAction](customaction-table.md) .

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della tabella CustomAction per specificare il tipo numerico di base.



| Costanti                                                               | Valore esadecimale | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeSourceFile** | 0x013       | 19      |



 

## <a name="target"></a>Destinazione

La colonna di destinazione della [tabella CustomAction](customaction-table.md) contiene una stringa di testo formattata utilizzando la funzionalità specificata in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (senza gli identificatori dei campi numerici). I parametri da sostituire sono racchiusi tra parentesi quadre, \[ ... \] e possono essere proprietà, variabili di ambiente (% prefix), percorsi di file ( \# prefisso) o percorsi di directory dei componenti ($ prefix). Se dopo la formattazione la stringa restituisce un valore integer, tale integer viene utilizzato come indice nella tabella degli [errori](error-table.md) per recuperare il messaggio da visualizzare. Se dopo la formattazione la stringa contiene caratteri non numerici, la stringa stessa viene visualizzata come messaggio.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

L'azione personalizzata non usa alcuna opzione.

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

L'azione personalizzata non usa alcuna opzione.

## <a name="in-script-execution-options"></a>Opzioni di esecuzione In-Script

L'azione personalizzata non usa alcuna opzione.

## <a name="return-values"></a>Valori restituiti

Vedere [valori restituiti dell'azione personalizzata](custom-action-return-values.md).

## <a name="remarks"></a>Commenti

Ad esempio, le azioni personalizzate CAError1, CAError2, CAError3 e CAError4 restituiscono questi messaggi.

[Tabella CustomAction](customaction-table.md)



| Azione   | Tipo | Source (Sorgente) | Destinazione                              |
|----------|------|--------|-------------------------------------|
| CAError1 | 19   |        | \[Prop1\]                           |
| CAError2 | 19   |        | Errore di installazione dovuto a Error2. |
| CAError3 | 19   |        | 25000                               |
| CAError4 | 19   |        | \[Prop2\]                           |



 

[Tabella delle proprietà](property-table.md)



| Proprietà | Valore                                 |
|----------|---------------------------------------|
| Prop1    | "Errore di installazione dovuto a Error1". |
| Prop2    | "25100"                               |



 

[Tabella degli errori](error-table.md)



| Codice  | Message                             |
|-------|-------------------------------------|
| 25000 | Errore di installazione dovuto a Error3. |
| 25100 | Errore di installazione dovuto a Error4. |



 

Queste azioni personalizzate restituiscono i messaggi di errore seguenti:



| Azione personalizzata | Stringa di messaggio restituita             |
|---------------|-------------------------------------|
| CAError1      | Errore di installazione dovuto a Error1. |
| CAError2      | Errore di installazione dovuto a Error2. |
| CAError3      | Errore di installazione dovuto a Error3. |
| CAError4      | Errore di installazione dovuto a Error4. |



 

Si noti che poiché non è possibile garantire l'ordine di valutazione delle condizioni di avvio mediante la creazione della [tabella LaunchCondition](launchcondition-table.md), è consigliabile utilizzare il tipo di azione personalizzata 19 azioni personalizzate nell'installazione per valutare le condizioni in un ordine specifico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_Azioni personalizzate](custom-actions.md)
</dt> </dl>

 

 



