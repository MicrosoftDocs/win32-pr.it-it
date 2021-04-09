---
description: Sebbene le parole e le regole linguistiche differiscano notevolmente, esistono alcune considerazioni, ad esempio numeri, date e ore, che vengono gestite in modo coerente in tutti i Word breaker.
ms.assetid: 62545566-f0ba-4876-93da-e6c2b9c23484
title: Normalizzazione del form della superficie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b058be00e046ffc17ebd6c13178313267a47079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128487"
---
# <a name="surface-form-normalization"></a>Normalizzazione del form della superficie

Sebbene le parole e le regole linguistiche differiscano notevolmente, esistono alcune considerazioni, ad esempio numeri, date e ore, che vengono gestite in modo coerente in tutti i Word breaker. In questo argomento vengono documentate le considerazioni sulla normalizzazione che possono influire sull'implementazione del Word breaker.

Questo argomento è organizzato nel modo seguente:

-   [Sillabazione](#hyphenation)
-   [Possessivi](#possessives)
-   [Diacritici](#diacritics)
-   [Clitici](#clitics)

## <a name="hyphenation"></a>Sillabazione

I trattini (-) vengono usati tra le parti di una parola o di un nome composto. Vengono inoltre utilizzate tra le sillabe di una parola quando la parola viene divisa alla fine di una riga di testo. In inglese, le parole sono unite da trattini per indicare una relazione speciale nel contesto, ma tali parole potrebbero non essere in genere sillabate in altri contesti; ad esempio, "Step-by-Step". Durante la creazione dell'indice, il Word breaker deve considerare il segno meno come separatore di parole. Ad esempio, "data-base" verrebbe archiviato come "data" più "base". In fase di query, una frase con sillabazione deve essere sostituita con due alternative: la variante a due parole e il composto vero e proprio. Ad esempio, "data-base" verrebbe sostituito da "data" più "base" e "database". Questa differenza tra l'indice e il tempo di query aumenta le combinazioni di rappresentazioni per le parole sillabate e rende più semplice la corrispondenza delle parole in una query.

Nella tabella seguente viene illustrato come il trattamento dei trattini come separatori di parola nella lingua inglese aumenta il numero di termini di query corrispondenti per ogni termine incluso nell'indice.



| Termini inclusi nell'indice | Corrispondenze in fase di query   |
|-----------------------------|----------------------|
| Data base                   | base dati, data-base |
| Data-base                   | base dati, data-base |
| Database                    | base dati, database  |



 

## <a name="possessives"></a>Possessivi

Possessivi sono variazioni in un sostantivo che indicano il possesso. I possessivi inglesi sono rappresentati mediante l'aggiunta di un apostrofo (') o di un apostrofo e di una (' s') a una parola. Per indicare, ad esempio, il possesso, la parola "Mary" viene rappresentata come "Maria". Il Word breaker genera i form apostrofo e apostrofo-s in fase di query. Le query per "Mary" devono corrispondere sia a "Mary" sia a "Mary".

## <a name="diacritics"></a>Diacritici

I segni diacritici sono contrassegni aggiunti a una lettera o a un fonema per indicare un particolare valore fonetico per la pronuncia. I segni diacritici possono distinguere le parole che sono altrimenti identiche graficamente. ad esempio, "Resume" e "curriculum" in inglese. Tuttavia, il salvataggio dei segni diacritici nell'indice aumenta il numero di chiavi di parola univoche nell'indice, rallentando le prestazioni di esecuzione delle query. Se i segni diacritici vengono utilizzati solo in modo minimo in una lingua, il Word breaker per tale lingua deve rimuoverli durante la creazione dell'indice e l'esecuzione di query. Ad esempio, il Word breaker per la lingua inglese genera "Resume" durante l'elaborazione di "curriculum", causando solo un effetto minimo sulla pertinenza dei risultati della query.

## <a name="clitics"></a>Clitici

Un clitoride è una parola non stressata che non è in grado di essere autonoma e si collega a una parola sottolineata per formare una singola unità. Clitici non può essere facilmente classificato come fonologico, sintattico o morfologico. Clitici sono disponibili in due tipi: *proclitics* e *enclitics*. Proclitics si connette all'inizio di una parola. Enclitics si alleghino alla fine di una parola.

Clitici sono più difficili da analizzare in linguaggi come lo spagnolo. Un verbo spagnolo può generare molti form della superficie, a seconda del tempo. È necessario tenere presenti alcune considerazioni tra la rimozione del clitoride durante la creazione dell'indice e la generazione dei form della superficie tramite lo stemming in fase di query. La rimozione di clitici nei casi in cui la morfologia della composizione clitoridea è ambigua può causare risultati imprevedibili. La generazione di un numero elevato di forme di superficie per una parola aumenta le dimensioni dell'indice full-text e può rallentare le prestazioni delle query. È consigliabile che lo stemmer generi solo un numero ridotto di forme di superficie.

 

 



