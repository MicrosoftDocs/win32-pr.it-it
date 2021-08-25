---
description: Questa sezione descrive la sintassi delle istruzioni condizionali usate dalla funzione MsiEvaluateCondition e dalle tabelle della sequenza di azioni. Per altre informazioni, vedere Esempi di sintassi delle istruzioni condizionali.
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: Sintassi delle istruzioni condizionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dfea7ec31cecbe9c72dee9c660b0e6ee9d07cee2f1818941d036a781c104a93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077961"
---
# <a name="conditional-statement-syntax"></a>Sintassi delle istruzioni condizionali

Questa sezione descrive la sintassi delle istruzioni condizionali usate dalla funzione [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) e dalle tabelle della sequenza [di azioni](using-a-sequence-table.md). Per altre informazioni, vedere Esempi [di sintassi delle istruzioni condizionali.](examples-of-conditional-statement-syntax.md)

## <a name="summary-of-conditional-statement-syntax"></a>Riepilogo della sintassi delle istruzioni condizionali

Questa tabella e l'elenco seguente riepilogano la sintassi da usare nelle espressioni condizionali.



| Elemento                | Sintassi                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| Valore               | symbol \| literal \| integer                                                                                    |
| operatore di confronto | < \| > \| <= \| >= \| = \| <>                                                                 |
| Termine                | value \| value comparison-operator value \| ( expression )\|                                                    |
| Fattore booleano      | termine \| **NOT** termine                                                                                            |
| Boolean-term        | Boolean-factor \| Boolean-factor **AND** term                                                                   |
| expression          | Boolean-term \| Boolean-term **OR** expression                                                                  |
| simbolo              | proprietà \| %environment-variable \| $component-action \| ?component-state \| &feature-action \| !feature-state |



 

-   Per i nomi e i valori dei simboli viene fatto distinzione tra maiuscole e minuscole.
-   I nomi delle variabili di ambiente non supportano la distinzione tra maiuscole e minuscole.
-   Il testo letterale deve essere racchiuso tra virgolette ("text").
    > [!Note]  
    > Il testo letterale contenente virgolette non può essere usato nelle istruzioni condizionali perché non è presente alcun carattere di escape per le virgolette all'interno del testo letterale. Per eseguire un confronto con testo letterale contenente virgolette, il testo letterale deve essere inserito in una proprietà . Ad esempio, per verificare che la proprietà SERVERNAME non contenga virgolette, definire una proprietà denominata QUOTES nella tabella [Property](property-table.md) con il valore " e modificare la condizione in NOT SERVERNAME><QUOTES.

     

-   I valori di proprietà inesistenti vengono considerati come stringhe vuote.
-   I valori numerici a virgola mobile non sono supportati.
-   Gli operatori e la precedenza sono gli stessi dei linguaggi BASIC SQL base.
-   Gli operatori aritmetici non sono supportati.
-   Le parentesi possono essere usate per eseguire l'override della precedenza degli operatori.
-   Gli operatori non supportano la distinzione tra maiuscole e minuscole.
-   Per i confronti tra stringhe, una tilde "~" preceduta dall'operatore esegue un confronto senza distinzione tra maiuscole e minuscole.
-   Il confronto di un intero con una stringa o un valore di proprietà che non può essere convertito in un integer è sempre **msiEvaluateConditionFalse**, ad eccezione dell'operatore di confronto "<>", che restituisce **msiEvaluateConditionTrue**.

## <a name="access-prefixes"></a>Prefissi di accesso

La tabella seguente illustra i prefissi da usare per accedere a varie informazioni sul sistema e sul programma di installazione da usare nelle espressioni condizionali.



| Tipo di simbolo          | Prefisso | Valore                                                     |
|----------------------|--------|-----------------------------------------------------------|
| Installer - proprietà   | (nessuna) | Valore della tabella property ([Property](property-table.md)). |
| Variabile di ambiente | %      | Valore della variabile di ambiente.                            |
| Chiave della tabella dei componenti  | $      | Stato dell'azione del componente.                            |
| Chiave della tabella dei componenti  | ?      | Stato di installazione del componente.                         |
| Chiave della tabella delle funzionalità    | &      | Stato dell'azione della funzionalità.                              |
| Chiave della tabella delle funzionalità    | !      | Stato di installazione della funzionalità.                           |



 

## <a name="logical-operators"></a>Operatori logici

Nella tabella seguente vengono illustrati gli operatori logici nelle espressioni condizionali, in ordine di precedenza da alto a basso.



| Operatore | Significato                                                 |
|----------|---------------------------------------------------------|
| Not      | Operatore unario prefisso; inverte lo stato del termine seguente. |
| e      | TRUE se entrambi i termini sono TRUE.                            |
| Oppure       | TRUE se uno o entrambi i termini sono TRUE.                  |
| Xor      | TRUE se entrambi i termini sono TRUE, ma non entrambi.             |
| Eqv      | TRUE se entrambi i termini sono TRUE o entrambi i termini sono FALSE.    |
| Imp      | TRUE se il termine sinistro è FALSE o il termine destro è TRUE.       |



 

## <a name="comparative-operators"></a>Operatori comparativi

Nella tabella seguente vengono illustrati gli operatori di confronto utilizzati nelle espressioni condizionali. Questi operatori di confronto possono verificarsi solo tra due valori.



| Operatore | Significato                                                     |
|----------|-------------------------------------------------------------|
| =        | TRUE se il valore a sinistra è uguale al valore di destra.                 |
| <> | TRUE se il valore a sinistra non è uguale al valore a destra.             |
| >     | TRUE se il valore a sinistra è maggiore del valore di destra.             |
| >=    | TRUE se il valore a sinistra è maggiore o uguale al valore di destra. |
| <     | TRUE se il valore a sinistra è minore del valore a destra.                |
| <=    | TRUE se il valore a sinistra è minore o uguale al valore a destra.    |



 

## <a name="substring-operators"></a>Operatori di sottostringa

Nella tabella seguente vengono illustrati gli operatori di sottostringa usati nelle espressioni condizionali. Gli operatori di sottostringa possono verificarsi tra due valori stringa.



| Operatore | Significato                                           |
|----------|---------------------------------------------------|
| >< | TRUE se la stringa a sinistra contiene la stringa a destra.    |
| << | TRUE se la stringa a sinistra inizia con la stringa a destra. |
| >> | TRUE se la stringa a sinistra termina con la stringa a destra.   |



 

## <a name="bitwise-numeric-operators"></a>Operatori numerici bit per bit

Nella tabella seguente vengono illustrati gli operatori numerici bit per bit nelle espressioni condizionali. Questi operatori possono verificarsi tra due valori interi.



| Operatore | Significato                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | AND bit per bit, TRUE se gli interi sinistro e destro hanno bit in comune.    |
| << | True se i 16 bit alti dell'intero a sinistra sono uguali all'intero a destra. |
| >> | True se i 16 bit bassi dell'intero a sinistra sono uguali all'intero a destra.  |



 

## <a name="feature-and-component-state-values"></a>Valori dello stato di funzionalità e componenti

Nella tabella seguente viene illustrato dove è possibile utilizzare i simboli degli operatori di funzionalità e componenti.



| Operatore <state> | Dove questa sintassi è valida                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| $component-action      | Nella tabella [Condizione](condition-table.md) e nelle tabelle di [sequenza,](using-a-sequence-table.md) dopo l'azione [CostFinalize.](costfinalize-action.md) |
| &feature-action        | Nella tabella [Condizione](condition-table.md) e nelle tabelle di [sequenza,](using-a-sequence-table.md) dopo l'azione [CostFinalize.](costfinalize-action.md) |
| !feature-state         | Nella tabella [Condizione](condition-table.md) e nelle tabelle di [sequenza,](using-a-sequence-table.md) dopo l'azione [CostFinalize.](costfinalize-action.md) |
| ?component-state       | Nella tabella [Condizione](condition-table.md) e nelle tabelle di [sequenza,](using-a-sequence-table.md) dopo l'azione [CostFinalize.](costfinalize-action.md) |



 

La tabella seguente illustra i valori di stato della funzionalità e del componente usati nelle espressioni condizionali. Questi stati non vengono impostati fino a quando non viene chiamato [**MsiSetInstallLevel,**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) direttamente o [dall'azione CostFinalize.](costfinalize-action.md)



| State                    | Valore | Significato                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| INSTALLSTATE \_ UNKNOWN    | -1    | Nessuna azione da eseguire sulla funzionalità o sul componente.              |
| INSTALLSTATE \_ ANNUNCIATO | 1     | Funzionalità annunciata. Questo stato non è disponibile per i componenti. |
| INSTALLSTATE \_ ABSENT     | 2     | Funzionalità o componente non presente.                            |
| INSTALLSTATE \_ LOCAL      | 3     | Funzionalità o componente nel computer locale.                     |
| ORIGINE \_ INSTALLSTATE     | 4     | Funzionalità o componente eseguiti dall'origine.                       |



 

Ad esempio, l'espressione condizionale "&MyFeature=3" restituisce True solo se MyFeature cambia dallo stato corrente allo stato di installazione nel computer locale, INSTALLSTATE \_ LOCAL.

Si noti che non è necessario dipendere dalla condizione $Component 1=3 per verificare se Component1 è installato localmente nel computer. Questa operazione può non riuscire se Component1 è installato da più di un prodotto. Dopo che Component1 è stato installato localmente da Product1, il programma di installazione valuta la condizione $Component 1=3 come False durante l'installazione di Product2. Questo perché il programma di installazione determina la versione del componente usando il percorso della chiave del componente e contrassegna il componente per l'installazione se la versione è maggiore o uguale al componente installato.

Si noti che il programma di installazione non farà confronti diretti del tipo di dati [Version](version.md) nelle istruzioni condizionali. Ad esempio, non è possibile usare operatori comparativi per confrontare versioni come "01.10" e "1.010" in un'istruzione condizionale. Usare invece un metodo valido per cercare una versione, ad esempio come descritto in Ricerca di [applicazioni, file,](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)voci del Registro di sistema o voci di file .ini esistenti, quindi impostare una proprietà .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



