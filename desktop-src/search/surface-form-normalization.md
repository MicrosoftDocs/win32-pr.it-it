---
description: Anche se le parole e le regole linguistiche differiscono notevolmente, esistono alcune considerazioni, ad esempio numeri, date e ore, che vengono gestite in modo coerente in tutti i word breaker.
ms.assetid: 62545566-f0ba-4876-93da-e6c2b9c23484
title: Normalizzazione della forma della superficie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f96ce5c90075c49608ad386b64514e4d003e5b5b4c6fc582441fd7e110d1921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862435"
---
# <a name="surface-form-normalization"></a>Normalizzazione della forma della superficie

Anche se le parole e le regole linguistiche differiscono notevolmente, esistono alcune considerazioni, ad esempio numeri, date e ore, che vengono gestite in modo coerente in tutti i word breaker. Questo argomento illustra alcune considerazioni sulla normalizzazione che possono influire sull'implementazione del word breaker.

Questo argomento è organizzato come segue:

-   [Sillabazione](#hyphenation)
-   [Possessivi](#possessives)
-   [Segni diacritici](#diacritics)
-   [Clitici](#clitics)

## <a name="hyphenation"></a>Sillabazione

I trattini (-) vengono usati tra le parti di una parola o di un nome composto. Vengono inoltre usati tra le sillabe di una parola quando la parola è divisa alla fine di una riga di testo. In inglese, le parole vengono unite con trattini per indicare una relazione speciale nel contesto, ma tali parole in genere non possono essere sillabate in altri contesti; ad esempio "step-by-step". Durante la creazione dell'indice, il word breaker deve considerare il trattino come separatore di parole. Ad esempio, "data-base" verrebbe archiviato come "data" più "base". In fase di query, una frase con trattino deve essere sostituita con due alternative: la variante a due parole e la vera composta. Ad esempio, "data-base" verrebbe sostituito da "data" più "base" e "database". Questa differenza tra tempo di indice e tempo di query aumenta le combinazioni di rappresentazioni per le parole con trattino e semplifica la corrispondenza delle parole in una query.

Nella tabella seguente viene illustrato come considerare i trattini come separatori di parole nella lingua inglese aumenta il numero di termini di query corrispondenti per ogni termine incluso nell'indice.



| Termini inclusi nell'indice | Corrispondenze in fase di query   |
|-----------------------------|----------------------|
| Data base                   | data base, data-base |
| Base dati                   | data base, data-base |
| Database                    | data-base, database  |



 

## <a name="possessives"></a>Possessivi

I possessivi sono variazioni in un sostantivo che indicano il possesso. I possessivi inglesi sono rappresentati aggiungendo un apostrofo (') o un apostrofo e uno (') a una parola. Ad esempio, per indicare il possesso, la parola "Mary" è rappresentata come "maria". Il word breaker genera sia l'apostrofo che il formato apostrofo-s in fase di query. Le query per "Mary" devono corrispondere sia a "Mary" che a "Mary".

## <a name="diacritics"></a>Segni diacritici

I segni diacritici sono contrassegni aggiunti a una lettera o a un fonema per indicare un valore fonetico speciale per la pronuncia. I segni diacritici possono distinguere le parole che sono altrimenti identiche graficamente; ad esempio "resume" e "resumé" in inglese. Tuttavia, il salvataggio dei segni diacritici nell'indice aumenta il numero di chiavi di parole univoche nell'indice, rallentando le prestazioni delle query. Se i segni diacritici vengono usati solo minimamente in una lingua, il word breaker per tale lingua deve rimuoverli sia durante la creazione dell'indice che durante l'esecuzione di query. Ad esempio, il word breaker inglese genera "resume" durante l'elaborazione di "resumé", causando solo un impatto minimo sulla pertinenza dei risultati della query.

## <a name="clitics"></a>Clitici

Un clitico è una parola nonstressed che non è in grado di essere in proprio e si collega a una parola stressata per formare una singola unità. L'interfaccia della riga di comando non può essere facilmente classificata come fonetica, sintattica o morfica. L'interfaccia della riga di comando è di due tipi: *proclitica* *ed enclitica.* Le procedure si collegano all'inizio di una parola. Le enclitiche si collegano alla fine di una parola.

I clitic sono più difficili da analizzare in lingue come lo spagnolo. Un verbo spagnolo può generare molte forme di superficie, a seconda del tempo. È necessario tenere in considerazione la rimozione dell'interfaccia della riga di comando durante la creazione dell'indice e la generazione dei formati di superficie tramite stemming in fase di query. La rimozione dell'interfaccia della riga di comando nei casi in cui la morfica della composizione clitica è ambigua può causare risultati imprevedibili. La generazione di un numero elevato di forme di superficie per una parola aumenta le dimensioni dell'indice full-text e può rallentare le prestazioni delle query. È consigliabile che lo stemmer generi solo un numero ridotto di forme di superficie.

 

 



