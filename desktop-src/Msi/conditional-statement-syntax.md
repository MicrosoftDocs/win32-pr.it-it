---
description: In questa sezione viene descritta la sintassi delle istruzioni condizionali utilizzate dalla funzione MsiEvaluateCondition e dalle tabelle di sequenza delle azioni. Per ulteriori informazioni, vedere, esempi di sintassi delle istruzioni condizionali.
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: Sintassi dell'istruzione condizionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0548a71756faff654bfe2b49e14c0581a6248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881053"
---
# <a name="conditional-statement-syntax"></a>Sintassi dell'istruzione condizionale

In questa sezione viene descritta la sintassi delle istruzioni condizionali utilizzate dalla funzione [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) e dalle [tabelle di sequenza](using-a-sequence-table.md)delle azioni. Per ulteriori informazioni, vedere, [esempi di sintassi delle istruzioni condizionali](examples-of-conditional-statement-syntax.md).

## <a name="summary-of-conditional-statement-syntax"></a>Riepilogo della sintassi delle istruzioni condizionali

Questa tabella e l'elenco seguente riepilogano la sintassi da usare nelle espressioni condizionali.



| Elemento                | Sintassi                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| Valore               | valore \| letterale \| Integer simbolo                                                                                    |
| operatore di confronto | < \| > \| <= \| >= \| = \| <>                                                                 |
| Termine                | valore valore \| confronto-valore operatore \| (espressione)\|                                                    |
| Fattore booleano      | termine \| **non** termine                                                                                            |
| Termine booleano        | Booleano-Factor \| -fattore **e** termine                                                                   |
| expression          | Espressione booleana a termine booleano \| **o** espressione                                                                  |
| simbolo              | proprietà \| % Environment-variable \| $Component-Action \| ? stato componente \| &funzionalità-azione \| ! funzionalità-stato |



 

-   Per i nomi dei simboli e i valori viene fatta distinzione tra maiuscole
-   Per i nomi delle variabili di ambiente non viene fatta distinzione tra maiuscole
-   Il testo letterale deve essere racchiuso tra virgolette ("testo").
    > [!Note]  
    > Impossibile utilizzare il testo letterale contenente virgolette nelle istruzioni condizionali perché non esiste alcun carattere di escape per le virgolette all'interno del testo letterale. Per eseguire un confronto con il testo letterale contenente virgolette, il testo letterale deve essere inserito in una proprietà. Per verificare, ad esempio, che la proprietà SERVERNAME non contenga virgolette, definire una proprietà denominata VIRGOLETte nella [tabella delle proprietà](property-table.md) con il valore "e modificare la condizione in not ServerName><virgolette.

     

-   I valori di proprietà inesistenti vengono considerati come stringhe vuote.
-   I valori numerici a virgola mobile non sono supportati.
-   Gli operatori e la precedenza sono identici a quelli dei linguaggi BASIC e SQL.
-   Gli operatori aritmetici non sono supportati.
-   Le parentesi possono essere utilizzate per eseguire l'override della precedenza degli operatori.
-   Gli operatori non fanno distinzione tra maiuscole e minuscole.
-   Per i confronti di stringhe, un valore tilde "~" con prefisso per l'operatore esegue un confronto senza distinzione tra maiuscole e minuscole.
-   Il confronto di un numero intero con un valore di stringa o di proprietà che non può essere convertito in un Integer è sempre **msiEvaluateConditionFalse**, ad eccezione dell'operatore di confronto "<>", che restituisce **msiEvaluateConditionTrue**.

## <a name="access-prefixes"></a>Prefissi di accesso

La tabella seguente illustra i prefissi da usare per accedere a diverse informazioni di sistema e di installazione da usare nelle espressioni condizionali.



| Tipo di simbolo          | Prefisso | Valore                                                     |
|----------------------|--------|-----------------------------------------------------------|
| Proprietà Installer   | (nessuna) | Valore della tabella Property ([Property](property-table.md)). |
| Variabile di ambiente | %      | Valore della variabile di ambiente.                            |
| Chiave tabella componenti  | $      | Stato dell'azione del componente.                            |
| Chiave tabella componenti  | ?      | Stato di installazione del componente.                         |
| Chiave della tabella delle funzionalità    | &      | Stato dell'azione della funzionalità.                              |
| Chiave della tabella delle funzionalità    | !      | Stato di installazione della funzionalità.                           |



 

## <a name="logical-operators"></a>Operatori logici

Nella tabella seguente vengono illustrati gli operatori logici nelle espressioni condizionali, in ordine di precedenza alto-a-basso.



| Operatore | Significato                                                 |
|----------|---------------------------------------------------------|
| Not      | Operatore unario prefix; inverte lo stato del termine seguente. |
| e      | TRUE se entrambi i termini sono TRUE.                            |
| Oppure       | TRUE se uno o entrambi i termini sono TRUE.                  |
| Xor      | TRUE se uno o entrambi i termini sono TRUE.             |
| Eqv      | TRUE se entrambi i termini sono TRUE o se entrambi i termini sono FALSE.    |
| IMP      | TRUE se il termine sinistro è FALSE o il termine corretto è TRUE.       |



 

## <a name="comparative-operators"></a>Operatori comparati

Nella tabella seguente vengono illustrati gli operatori di confronto utilizzati nelle espressioni condizionali. Questi operatori di confronto possono essere presenti solo tra due valori.



| Operatore | Significato                                                     |
|----------|-------------------------------------------------------------|
| =        | TRUE se il valore di sinistra è uguale a quello a destra.                 |
| <> | TRUE se il valore di sinistra non è uguale al valore di destra.             |
| >     | TRUE se il valore a sinistra è maggiore del valore a destra.             |
| >=    | TRUE se il valore a sinistra è maggiore o uguale al valore a destra. |
| <     | TRUE se il valore a sinistra è minore del valore a destra.                |
| <=    | TRUE se il valore di sinistra è minore o uguale al valore a destra.    |



 

## <a name="substring-operators"></a>Operatori di sottostringhe

Nella tabella seguente vengono illustrati gli operatori di sottostringa utilizzati nelle espressioni condizionali. Gli operatori di sottostringhe possono essere presenti tra due valori di stringa.



| Operatore | Significato                                           |
|----------|---------------------------------------------------|
| >< | TRUE se la stringa a sinistra contiene la stringa a destra.    |
| << | TRUE se la stringa a sinistra inizia con la stringa a destra. |
| >> | TRUE se la stringa a sinistra termina con la stringa a destra.   |



 

## <a name="bitwise-numeric-operators"></a>Operatori numerici bit per bit

Nella tabella seguente vengono illustrati gli operatori numerici bit per bit nelle espressioni condizionali. Questi operatori possono verificarsi tra due valori integer.



| Operatore | Significato                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | AND bit per bit, TRUE se gli Integer a sinistra e a destra hanno bit in comune.    |
| << | True se i 16 bit alti dell'intero a sinistra sono uguali all'intero a destra. |
| >> | True se i 16 bit bassi dell'intero a sinistra sono uguali all'intero a destra.  |



 

## <a name="feature-and-component-state-values"></a>Valori dello stato delle funzionalità e dei componenti

Nella tabella seguente viene indicato dove è possibile utilizzare i simboli di operatore feature e Component.



| Operatore <state> | Dove questa sintassi è valida                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| $component-azione      | Nella tabella [Condition](condition-table.md) e nelle tabelle [Sequence](using-a-sequence-table.md) , dopo l'azione [CostFinalize secondo](costfinalize-action.md) . |
| Funzionalità &-azione        | Nella tabella [Condition](condition-table.md) e nelle tabelle [Sequence](using-a-sequence-table.md) , dopo l'azione [CostFinalize secondo](costfinalize-action.md) . |
| ! stato della funzionalità         | Nella tabella [Condition](condition-table.md) e nelle tabelle [Sequence](using-a-sequence-table.md) , dopo l'azione [CostFinalize secondo](costfinalize-action.md) . |
| ? componente-stato       | Nella tabella [Condition](condition-table.md) e nelle tabelle [Sequence](using-a-sequence-table.md) , dopo l'azione [CostFinalize secondo](costfinalize-action.md) . |



 

Nella tabella seguente vengono illustrati i valori relativi allo stato delle funzionalità e dei componenti utilizzati nelle espressioni condizionali. Questi Stati non vengono impostati fino a quando non viene chiamato [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) , direttamente o dall'azione [CostFinalize secondo](costfinalize-action.md) .



| State                    | Valore | Significato                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| INSTALLSTATE \_ sconosciuto    | -1    | Nessuna azione da intraprendere per la funzionalità o il componente.              |
| INSTALLSTATE \_ annunciata | 1     | Funzionalità annunciata. Questo stato non è disponibile per i componenti di. |
| INSTALLSTATE \_ assente     | 2     | La funzionalità o il componente non è presente.                            |
| INSTALLSTATE \_ locale      | 3     | Funzionalità o componente nel computer locale.                     |
| \_origine InstallState     | 4     | Funzionalità o componente eseguiti dall'origine.                       |



 

Ad esempio, l'espressione condizionale "&la funzionalità = 3" restituisce true solo se la funzionalità è cambiata dallo stato corrente allo stato di installazione nel computer locale, INSTALLSTATE \_ locale.

Si noti che non è necessario basarsi sulla condizione $Component 1 = 3 per verificare se Component1 è installato localmente nel computer. Questa operazione può avere esito negativo se Component1 è installato da più di un prodotto. Dopo che Component1 è stato installato localmente da product1, il programma di installazione valuta la condizione $Component 1 = 3 come false durante l'installazione di Product2. Questo perché il programma di installazione determina la versione del componente usando il percorso della chiave del componente e contrassegna il componente per l'installazione se la relativa versione è maggiore o uguale al componente installato.

Si noti che il programma di installazione non esegue confronti diretti del tipo di dati [Version](version.md) nelle istruzioni condizionali. Ad esempio, non è possibile utilizzare operatori comparative per confrontare versioni quali "01,10" e "1,010" in un'istruzione condizionale. Usare invece un metodo valido per cercare una versione, come descritto in [ricerca di applicazioni esistenti, file, voci del registro di sistema o voci di file ini](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md), quindi impostare una proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



