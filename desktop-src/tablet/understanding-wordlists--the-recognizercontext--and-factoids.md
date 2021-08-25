---
description: Tutti i dizionari dell'applicazione vengono implementati usando l'oggetto WordList.
ms.assetid: 805788ec-1672-462a-b188-c680f56c2641
title: Informazioni su elenchi di parole, contesto di riconoscimento e factoid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60fbfc7a3a3099a1146307637d20e777cca416789a61f5dd034f9d86911f1a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842811"
---
# <a name="understanding-word-lists-recognizer-context-and-factoids"></a>Informazioni su elenchi di parole, contesto di riconoscimento e factoid

Tutti i dizionari dell'applicazione vengono implementati usando [**l'oggetto WordList.**](inkwordlist-class.md) [**L'oggetto RecognizerContext**](inkrecognizercontext-class.md) gestisce il riconoscimento, in parte tramite la proprietà [**WordList di tale**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) oggetto. **L'oggetto RecognizerContext** passa l'elenco di parole al riconoscitore. È possibile abilitare un dizionario applicazioni in **qualsiasi RecognizerContext** nell'applicazione impostando la **proprietà WordList** dell'oggetto **RecognizerContext.** Per rendere disponibile l'elenco di parole per l'intera applicazione, è necessario impostare la proprietà **WordList** di ogni **oggetto RecognizerContext** nell'applicazione.

A livello di sistema di riconoscimento, tutti i dizionari ad eccezione del dizionario di sistema vengono implementati come elenchi di parole. Tuttavia, il riconoscitore può avere un solo elenco di parole attive alla volta. Ciò significa che non è possibile avere sia un dizionario dell'applicazione che il dizionario utente attivi contemporaneamente. D'altra parte, il dizionario di sistema è sempre disponibile, a meno che non sia impostato un factoid che disattiva il dizionario di sistema.

Il dizionario utente è l'elenco di parole che l'utente ha aggiunto al tablet PC. Se la [**proprietà WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) di [**RecognizerContext**](inkrecognizercontext-class.md) non è impostata, **RecognizerContext** passa il dizionario utente come elenco di parole al riconoscitore. Tuttavia, se la **proprietà WordList** dell'oggetto **RecognizerContext** è impostata, l'elenco di parole viene passato al riconoscimento anziché al dizionario utente.

> [!Note]  
> La [**proprietà Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) deve essere vuota prima di impostare la [**proprietà WordList.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) Se la **proprietà Strokes** non è vuota, viene generata un'eccezione. Le parole non devono mai essere aggiunte a un elenco di parole dopo essere state assegnate a un **oggetto RecognizerContext.**

 

L'impostazione di un factoid [**nell'oggetto RecognizerContext**](inkrecognizercontext-class.md) influisce anche sul modo in cui i dizionari dell'applicazione vengono usati dal riconoscitore. I factoid che influiscono sul comportamento dei dizionari sono:

-   **Wordlist**
-   **SystemDictionary**
-   **Nessuno**

Di gran lunga, il factoid più utile per i dizionari dell'applicazione è il factoid **WordList.** Il **factoid WordList** biasimo il riconoscimento per restituire solo le parole trovate nell'elenco di parole. Questo factoid disattiva tutti gli altri dizionari ad eccezione dell'elenco di parole. Se il **factoid WordList** è impostato e non viene specificato alcun elenco di parole nel contesto del riconoscimento, il dizionario utente viene usato come elenco di parole.

Ad esempio, se si sta progettando un'applicazione di parti di aereo con un campo che accetta uno dei dieci nomi di parti specializzate, è possibile creare un elenco di parole che contenga solo questi nomi di parti. L'impostazione del factoid **WordList** per il campo migliora notevolmente il riconoscimento per le parole immesse in tale campo. Il riconoscitore non deve scegliere tra le parole nel dizionario di sistema e le parole nell'elenco di parole.

Il **factoid SystemDictionary** abilita solo il dizionario di sistema. Il **factoid None** disabilita tutti i dizionari. Questi due factoid vengono usati per aumentare l'accuratezza del riconoscimento in determinati casi. Tuttavia, poiché disabilitano i dizionari delle applicazioni, raramente vengono usati insieme ai dizionari dell'applicazione.

Per altre informazioni sull'effetto dei factoid sul riconoscimento, vedere [Uso del contesto per migliorare l'accuratezza.](using-context-to-improve-accuracy.md)

Per altre informazioni sui **factoid SystemDictionary** e **None,** vedere [Factoid supportati dalla versione 1.](supported-factoids-from-version-1.md)

 

 



