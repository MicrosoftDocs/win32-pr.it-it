---
title: Unità di testo per Automazione interfaccia utente
description: Questo argomento descrive le unità di testo supportate da automazione interfaccia utente Microsoft \ 32; Pattern di controllo TextRange. I provider di automazione interfaccia utente e i client utilizzano unità di testo per specificare la quantità in base alla quale spostare o modificare le dimensioni di un intervallo di testo.
ms.assetid: 3ec43a81-c4f1-4c73-865f-a60c751fc3fb
keywords:
- Automazione interfaccia utente, unità di testo
- unità di testo, informazioni
- Automazione interfaccia utente, elenco di unità di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ff4257c70b34cea01a149b30dff2bf2fbe691a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337654"
---
# <a name="ui-automation-text-units"></a>Unità di testo di automazione interfaccia utente

Questo argomento descrive le unità di testo supportate dal pattern di controllo [TextRange](uiauto-implementingtextandtextrange.md) di automazione interfaccia utente Microsoft. I provider di automazione interfaccia utente e i client utilizzano unità di testo per specificare la quantità in base alla quale spostare o modificare le dimensioni di un intervallo di testo.

-   [Elementi API unità di testo](#text-unit-api-elements)
-   [Descrizioni di unità di testo](#text-unit-descriptions)
    -   [Carattere](#character)
    -   [Formato](#format)
    -   [Word](#word)
    -   [Linea](#line)
    -   [Paragraph](#paragraph)
    -   [Page](#page)
    -   [Documento](#document)
-   [Altri intervalli potenziali](#other-potential-ranges)
-   [Argomenti correlati](#related-topics)

## <a name="text-unit-api-elements"></a>Elementi API unità di testo

L'API di automazione interfaccia utente include i metodi seguenti che richiedono la specifica di un'unità di testo:

-   [**ITextRangeProvider:: Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)
-   [**ITextRangeProvider:: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit)
-   [**ITextRangeProvider:: MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)
-   [**IUIAutomationTextRange:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)
-   [**IUIAutomationTextRange:: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit)
-   [**IUIAutomationTextRange:: MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)

L'enumerazione [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) definisce le unità di testo supportate dagli intervalli di testo di automazione interfaccia utente. Per specificare l'unità di testo, un membro dell'enumerazione [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) viene specificato in una chiamata a un metodo [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) o [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) . Le unità di testo, dal più piccolo al più grande, sono le seguenti:

-   [**\_Carattere TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Formato TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Parola TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Linea TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Paragrafo TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Pagina TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Documento TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)

Se un particolare controllo basato su testo non supporta l'unità di testo specificata, il provider deve rispondere sostituendo l'unità di testo più grande successiva supportata dal controllo. Se, ad esempio, il [**\_ paragrafo TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) è specificato ma non è supportato, il metodo può sostituire la [**\_ pagina TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) o il [**\_ documento TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit).

Le caratteristiche linguistiche del testo di origine possono rendere difficile per un provider determinare i limiti del testo in base all'unità di testo specificata. Per informazioni su come determinare i limiti del testo, un provider può usare le funzioni dell'API Uniscribe, ad esempio [**ScriptBreak**](/windows/desktop/api/usp10/nf-usp10-scriptbreak). Per ulteriori informazioni, vedere [Uniscribe](/windows/desktop/Intl/uniscribe) nel sito Web MSDN.

## <a name="endpoint-inclusivity"></a>Inclusione endpoint

Un endpoint di unità di testo può fungere sia da endpoint [iniziale](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) che da endpoint [finale](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) per intervalli di testo adiacenti dello stesso tipo. Se la fine di un'unità di testo è anche l'inizio di un'altra unità di testo, l'intervallo contenente l'endpoint [finale](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) non condivide gli attributi o gli oggetti dell'intervallo adiacente contenente l'endpoint [iniziale](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) .

Ad esempio, un flusso di testo, "Hello **World**", contiene due unità di parole con attributi di spessore carattere diversi (normale e grassetto). In questo caso, l'endpoint [finale](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) della parola Unit "Hello" e l'endpoint di [avvio](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) della parola unità "**World**" sono gli stessi, il che comporta quanto segue:

- L'intervallo di "Hello" non condivide l'attributo grassetto dell'unità di Word "World" e non restituisce il valore dell'attributo misto per l'attributo di testo del tipo di carattere.
- L'intervallo di "**World**" ha un singolo spessore del carattere (in grassetto) e non condivide lo spessore del carattere dell'unità di Word precedente "Hello".

Ecco un altro esempio in cui un flusso di testo contiene due unità di parole, una delle quali è un collegamento: `[Foo]() Bar` . In questo caso, l'endpoint [finale](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) dell'unità di Word `[Foo]()` e l'endpoint [iniziale](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) della "barra" della parola sono gli stessi, il che comporta quanto segue:

- Il collegamento appartiene all'intervallo di testo che contiene "foo".
- Il collegamento è un elemento figlio dell'intervallo di testo "foo" ed è racchiuso da [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).
- L'intervallo di testo "barra" non ha elementi figlio e è racchiuso da [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).

**Note aggiuntive:**

> Un intervallo degenerato (vuoto) in corrispondenza di un limite di unità di testo con un intervallo di testo dello stesso tipo presuppone le proprietà dell'unità di testo immediatamente adiacente.
>
> La chiamata a [IUIAutomationTextRange:: ExpandToEnclosingUnit](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit
) su un intervallo degenerato in corrispondenza di un limite di unità di testo con un intervallo di testo dello stesso tipo, espande l'intervallo degenerate alla seguente unità di testo.

## <a name="text-unit-descriptions"></a>Descrizioni di unità di testo

Questa sezione descrive ogni unità di testo supportata dall'automazione interfaccia utente.

### <a name="character"></a>Carattere

[**TextUnit \_ Character**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) è un'unità linguistica di testo che rappresenta un singolo carattere. La definizione linguistica di un carattere varia in base alla lingua. Per l'inglese (Stati Uniti), un carattere viene in genere associato da uno spazio o da un altro carattere, ad esempio un segno di punteggiatura, un numero o una lettera.

I caratteri di controllo come i ritorni a capo e il contrassegno da sinistra a destra (LTM) Unicode non devono essere considerati come caratteri, ma possono essere inclusi in un intervallo di testo normalizzato in base all'unità di testo del carattere.

I segni di punteggiatura e i caratteri di Word Break come gli spazi devono essere considerati caratteri.

### <a name="format"></a>Formato

[**TextUnit \_ Format**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) viene usato per posizionare il limite di un intervallo di testo in base agli attributi di formattazione del testo. Se, ad esempio, un intervallo di testo è attualmente posizionato in corrispondenza di un singolo carattere di una parola, specificando il **\_ formato TextUnit** in una chiamata a [**IUIAutomationTextRange:: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) , l'intervallo di testo verrà espanso in modo da includere tutto il testo che condivide tutti gli stessi attributi del singolo carattere. È possibile che l'intervallo di testo risultante non includa l'intera parola. Inoltre, l'utilizzo dell'unità di testo formato non espanderà un intervallo di testo oltre il limite di un oggetto incorporato, ad esempio un'immagine o un collegamento ipertestuale.

Diversamente dalle altre unità di testo, che includono le unità di testo più piccole di se stesse, il [**\_ formato TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) può essere minore o maggiore di quello delle altre unità. Se, ad esempio, un intero documento condivide gli stessi attributi di testo e non contiene oggetti incorporati, l'espansione di un intervallo di testo in base al **\_ formato TextUnit** creerebbe un nuovo intervallo che include l'intero documento, espandendo l'intervallo di testo in base a [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) creerebbe un intervallo inferiore.

### <a name="word"></a>Word

[**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) è un'unità linguistica di testo che rappresenta una singola parola intera. La definizione linguistica di una parola varia a seconda della lingua. Per l'inglese (Stati Uniti), le parole sono in genere delimitate da spazi o segni di punteggiatura.

Quando si usa [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) per impostare il limite di un intervallo di testo, l'intervallo di testo risultante deve includere tutti i caratteri di Word break presenti alla fine della parola, ma prima dell'inizio della parola successiva.

### <a name="line"></a>Linea

[**TextUnit \_ La riga**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) è un'unità di testo che rappresenta una singola riga di testo visualizzata nel viewport del controllo. Quando si usa la **\_ riga TextUnit** per impostare il limite di un intervallo di testo, un provider deve impostare il limite immediatamente dopo il punto in cui un carattere di controllo interrompe la riga o dove il viewport del controllo esegue il wrapping del testo in una nuova riga. Il limite deve essere impostato in cui viene avviata una nuova riga.

### <a name="paragraph"></a>Paragraph

[**TextUnit \_ Il paragrafo**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) è un'unità linguistica di testo che rappresenta un paragrafo completo. Un paragrafo deve iniziare immediatamente prima del primo carattere di un paragrafo e in genere deve terminare subito dopo l'ultimo carattere. Tutte le righe vuote che seguono un paragrafo devono essere unite nel paragrafo, a meno che un elemento nell'origine di testo non indichi diversamente. In genere, il limite finale di un paragrafo contrassegna anche il limite finale di un'unità di testo della [**\_ linea TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) .

### <a name="page"></a>Pagina

[**TextUnit \_ La pagina**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) rappresenta una pagina di testo completa di un documento. I limiti di una pagina devono essere impostati nei punti immediatamente in cui viene avviata e terminata una pagina.

### <a name="document"></a>Documento

[**TextUnit \_ Document**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) rappresenta l'intero contenuto di un documento supportato dal pattern di controllo [Text](uiauto-implementingtextandtextrange.md) . Non deve esistere testo all'esterno di un intervallo di testo che contiene un documento. Tutti gli oggetti inseriti in un documento, ad esempio le note di annotazione che superano un limite di pagina, devono essere considerati come oggetti incorporati del documento e non appartenenti al contenuto di testo del documento.

## <a name="other-potential-ranges"></a>Altri intervalli potenziali

La specifica corrente del pattern di controllo [TextRange](uiauto-implementingtextandtextrange.md) non consente l'aggiunta di nuovi valori di unità di testo all'enumerazione [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) , né consente di ridefinire i valori delle unità di testo esistenti. Per esporre altri intervalli potenziali, ad esempio intestazioni e annotazioni, un provider deve esporre questi intervalli come oggetti incorporati con un intervallo di testo associato. In questo modo, è anche possibile aggiungere il supporto per i pattern di controllo appropriati. Questa soluzione è più flessibile ed estendibile rispetto alla definizione di nuove unità di testo.

## <a name="related-topics"></a>Argomenti correlati

### <a name="reference"></a>Riferimento

[TextPatternRangeEndpoint](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)

[ITextRangeProvider:: GetChildren](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-getchildren)





### <a name="conceptual"></a>Informazioni concettuali

[Supporto di automazione interfaccia utente per contenuto testuale](uiauto-ui-automation-textpattern-overview.md)

[Utilizzo di controlli basati su testo](uiauto-workingwithtextbasedcontrols.md)