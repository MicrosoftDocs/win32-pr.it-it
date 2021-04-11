---
description: Tutti i dizionari applicazione vengono implementati utilizzando l'oggetto WordList.
ms.assetid: 805788ec-1672-462a-b188-c680f56c2641
title: Informazioni sugli elenchi di parole, contesto di riconoscimento e factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27f15d64f353b8702695b0067f13857427fc34e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232088"
---
# <a name="understanding-word-lists-recognizer-context-and-factoids"></a>Informazioni sugli elenchi di parole, contesto di riconoscimento e factoids

Tutti i dizionari applicazione vengono implementati utilizzando l'oggetto [**WordList**](inkwordlist-class.md) . L'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) gestisce il riconoscimento, in parte tramite la proprietà [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) di tale oggetto. L'oggetto **RecognizerContext** passa l'elenco di parole al riconoscimento. È possibile abilitare un dizionario dell'applicazione in qualsiasi oggetto **RecognizerContext** nell'applicazione impostando la proprietà **WordList** dell'oggetto **RecognizerContext** . Per rendere disponibile l'elenco di parole per l'intera applicazione, è necessario impostare la proprietà **WordList** di ogni oggetto **RecognizerContext** nell'applicazione.

A livello di riconoscimento, tutti i dizionari ad eccezione del dizionario di sistema vengono implementati come elenchi di parole. Tuttavia, il riconoscimento può avere un solo elenco di parole attive alla volta. Ciò significa che non è possibile disporre contemporaneamente di un dizionario dell'applicazione e di un dizionario utente. D'altra parte, il dizionario di sistema è sempre disponibile, a meno che non sia impostato un controllo dell'oggetto che disattiva il dizionario di sistema.

Il dizionario utente è l'elenco di parole che l'utente ha aggiunto al Tablet PC. Se la proprietà [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) di [**RecognizerContext**](inkrecognizercontext-class.md) non è impostata, l'oggetto **RecognizerContext** passa il dizionario utente come un elenco di parole al riconoscimento. Tuttavia, se la proprietà **WordList** dell'oggetto **RecognizerContext** è impostata, l'elenco di parole viene passato al riconoscimento anziché al dizionario utente.

> [!Note]  
> Prima di impostare la proprietà [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) , la proprietà [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) deve essere vuota. Se la proprietà **Strokes** non è vuota, viene generata un'eccezione. Non è mai possibile aggiungere parole a un elenco di parole dopo che è stato assegnato a un oggetto **RecognizerContext** .

 

L'impostazione di un controllo del controllo sull'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) influisca anche sul modo in cui i dizionari applicazioni vengono usati dal riconoscimento. I factoids che influiscono sul comportamento dei dizionari sono:

-   **Elenco delle parole**
-   **SystemDictionary**
-   **Nessuno**

Dal punto di controllo più utile per i dizionari delle applicazioni è il controllo dell' **ordine dei vocaboli** . Il controllo dell'elenco **di parole polarizza** il riconoscitore verso la restituzione solo delle parole trovate nell'elenco di parole. Questo controllo del controllo Disattiva tutti gli altri dizionari ad eccezione dell'elenco di parole. Se il controllo dell'elenco di **parole** è impostato e non è specificato alcun elenco di parole nel contesto del riconoscimento, il dizionario utente viene usato come elenco di parole.

Se, ad esempio, si progetta un'applicazione di parti del velivolo con un campo che accetta uno dei dieci nomi delle parti specializzate, è possibile creare un elenco di parole contenente solo questi nomi di parte. L'impostazione del controllo dell' **ordine dei vocaboli** per il campo migliora notevolmente il riconoscimento delle parole immesse in quel campo. Il riconoscimento non deve scegliere tra parole nel dizionario di sistema e parole nell'elenco di parole.

Il controllo dell'oggetto **SystemDictionary** Abilita solo il dizionario di sistema. Il controllo del controllo **None** Disabilita tutti i dizionari. Questi due factoids vengono usati per aumentare l'accuratezza del riconoscimento in determinate istanze. Tuttavia, poiché disabilitano i dizionari applicazione, vengono usati raramente insieme ai dizionari applicazione.

Per ulteriori informazioni sul modo in cui factoids influisce sul riconoscimento, vedere [utilizzo del contesto per migliorare la precisione](using-context-to-improve-accuracy.md).

Per ulteriori informazioni su **SystemDictionary** e **None** factoids, vedere [Supported Factoids dalla versione 1](supported-factoids-from-version-1.md).

 

 



