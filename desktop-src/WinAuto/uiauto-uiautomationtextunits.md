---
title: Unità di testo per Automazione interfaccia utente
description: Questo argomento descrive le unità di testo supportate da Microsoft Automazione interfaccia utente \ 32; Pattern di controllo TextRange. Automazione interfaccia utente provider e client usano unità di testo per specificare la quantità in base alla quale spostare o modificare le dimensioni di un intervallo di testo.
ms.assetid: 3ec43a81-c4f1-4c73-865f-a60c751fc3fb
keywords:
- Automazione interfaccia utente,unità di testo
- unità di testo, informazioni
- Automazione interfaccia utente,elenco di unità di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc5c40604f3c524c1e9f3bcdb36458e099563eb7279fa61133dcfa7ea3fde90b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118824164"
---
# <a name="ui-automation-text-units"></a>Automazione interfaccia utente di testo

Questo argomento descrive le unità di testo supportate dal pattern di controllo Microsoft Automazione interfaccia utente [TextRange.](uiauto-implementingtextandtextrange.md) Automazione interfaccia utente provider e client usano unità di testo per specificare la quantità in base alla quale spostare o modificare le dimensioni di un intervallo di testo.

-   [Elementi API unità di testo](#text-unit-api-elements)
-   [Descrizioni delle unità di testo](#text-unit-descriptions)
    -   [Carattere](#character)
    -   [Formato](#format)
    -   [Word](#word)
    -   [Linea](#line)
    -   [Paragraph](#paragraph)
    -   [Page](#page)
    -   [Documento](#document)
-   [Altri intervalli potenziali](#other-potential-ranges)
-   [Argomenti correlati](#related-topics)

## <a name="text-unit-api-elements"></a>Elementi DELL'API unità di testo

L Automazione interfaccia utente API include i metodi seguenti che richiedono la specifica di un'unità di testo:

-   [**ITextRangeProvider::Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)
-   [**ITextRangeProvider::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit)
-   [**ITextRangeProvider::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)
-   [**IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)
-   [**IUIAutomationTextRange::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit)
-   [**IUIAutomationTextRange::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)

[**L'enumerazione TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) definisce le unità di testo supportate Automazione interfaccia utente di testo. Per specificare l'unità di testo, viene specificato un membro dell'enumerazione [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) in una chiamata a un metodo [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) o [**IUIAutomationTextRange.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) Le unità di testo, dal più piccolo al più grande, sono le seguenti:

-   [**Carattere \_ TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Formato \_ TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Parola \_ TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Linea \_ TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Paragrafo \_ TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Pagina \_ TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Documento \_ TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)

Se un determinato controllo basato su testo non supporta l'unità di testo specificata, il provider deve rispondere sostituendo l'unità di testo più grande successiva supportata dal controllo . Ad esempio, se [**textUnit \_ Paragraph viene**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) specificato ma non supportato, il metodo può sostituire [**TextUnit \_ Page**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) o [**TextUnit \_ Document**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit).

Le caratteristiche linguistiche del testo di origine possono rendere difficile per un provider determinare i limiti del testo in base all'unità di testo specificata. Per informazioni su come determinare i limiti del testo, un provider può usare funzioni API Uniscribe, ad esempio [**ScriptBreak**](/windows/desktop/api/usp10/nf-usp10-scriptbreak). Per altre informazioni, vedere [Uniscribe](/windows/desktop/Intl/uniscribe) nel sito Web MSDN.

## <a name="endpoint-inclusivity"></a>Inclusività dell'endpoint

Un endpoint unità di testo può fungere sia da endpoint [start](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) che da endpoint [end](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) per intervalli di testo adiacenti dello stesso tipo. Se la fine di un'unità di testo è anche [](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) l'inizio di un'altra unità di testo, l'intervallo contenente l'endpoint finale non condivide alcun attributo o oggetto dell'intervallo adiacente contenente l'endpoint [](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) Start.

Ad esempio, un flusso di testo, "Hello **world",** contiene due unità di parola con attributi di spessore del carattere diversi (normale e grassetto). In questo caso, [l'endpoint](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) finale dell'unità di parola "Hello" e l'endpoint [di](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) inizio della parola unità "**world**" sono gli stessi, con il risultato seguente:

- L'intervallo di "Hello" non condivide l'attributo in grassetto dell'unità di parola "world" e non restituisce il valore dell'attributo misto per l'attributo di testo dello spessore del carattere.
- L'intervallo di "**world**" ha un singolo spessore del carattere (grassetto) e non condivide lo spessore del carattere dell'unità di parola precedente "Hello".

Ecco un altro esempio in cui un flusso di testo contiene due unità di parole, una delle quali è un collegamento: `[Foo]() Bar` . In questo caso, l'endpoint [finale](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) della parola unit e l'endpoint Start della parola unità "Bar" sono gli stessi, con il risultato `[Foo]()` seguente: [](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)

- Il collegamento appartiene all'intervallo di testo contenente "Foo".
- Il collegamento è un elemento figlio dell'intervallo di testo "Foo" ed è racchiuso da [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).
- L'intervallo di testo "Bar" non ha elementi figlio ed è racchiuso da [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).

**Note aggiuntive:**

> Un intervallo degenerato (vuoto) in corrispondenza di un limite di unità di testo con un intervallo di testo dello stesso tipo presuppone le proprietà dell'unità di testo immediatamente adiacente.
>
> Chiamando [IUIAutomationTextRange::ExpandToEnclosingUnit](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit
) su un intervallo degenerato in corrispondenza di un limite di unità di testo con un intervallo di testo dello stesso tipo, l'intervallo degenerato viene espanso nell'unità di testo seguente.

## <a name="text-unit-descriptions"></a>Descrizioni delle unità di testo

Questa sezione descrive ognuna delle unità di testo supportate da Automazione interfaccia utente.

### <a name="character"></a>Carattere

[**TextUnit \_ Character**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) è un'unità linguistica di testo che rappresenta un singolo carattere. La definizione linguistica di un carattere varia in base alla lingua. Per l'inglese degli Stati Uniti, un carattere è in genere punteggiato da uno spazio o da un altro carattere, ad esempio un segno di punteggiatura, un numero o una lettera.

I caratteri di controllo, ad esempio i ritorni a capo e il segno unicode da sinistra a destra (LTM), non devono essere considerati come caratteri, ma possono essere inclusi in un intervallo di testo normalizzato in base all'unità di testo del carattere.

I segni di punteggiatura e i caratteri di interruzione di parola, ad esempio gli spazi, devono essere considerati caratteri.

### <a name="format"></a>Formato

[**TextUnit \_ Format**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) viene usato per posizionare il limite di un intervallo di testo in base agli attributi di formattazione del testo. Ad esempio, se un intervallo di testo è attualmente posizionato su un singolo carattere di una parola, specificando **TextUnit \_ Format** in una chiamata a [**IUIAutomationTextRange::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) si espande l'intervallo di testo in modo da includere tutto il testo che condivide tutti gli stessi attributi del singolo carattere. L'intervallo di testo risultante potrebbe includere o meno l'intera parola. Inoltre, l'uso dell'unità di testo formato non espanderà un intervallo di testo oltre il limite di un oggetto incorporato, ad esempio un'immagine o un collegamento ipertestuale.

A differenza delle altre unità di testo, che includono le unità di testo più piccole di se stesse, [**il formato TextUnit \_ può**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) essere più piccolo o maggiore delle altre unità. Ad esempio, se un intero documento condivide gli stessi attributi di testo e non contiene oggetti incorporati, l'espansione di un intervallo di testo in **formato TextUnit \_** creerebbe un nuovo intervallo che comprende l'intero documento, mentre l'espansione dell'intervallo di testo in base a [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) creerebbe un intervallo più piccolo.

### <a name="word"></a>Word

[**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) è un'unità linguistica di testo che rappresenta una singola parola intera. La definizione linguistica di una parola varia in base alla lingua. Per l'inglese degli Stati Uniti, le parole sono in genere con spazi o caratteri di punteggiatura.

Quando [**si usa TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) per impostare il limite di un intervallo di testo, l'intervallo di testo risultante deve includere tutti i caratteri di interruzione di parola presenti alla fine della parola, ma prima dell'inizio della parola successiva.

### <a name="line"></a>A linee

[**TextUnit \_ Line**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) è un'unità di testo che rappresenta una singola riga di testo presentata nel riquadro di visualizzazione del controllo. Quando si usa **TextUnit \_ Line** per impostare il limite di un intervallo di testo, un provider deve impostare il limite immediatamente dopo il punto in cui un carattere di controllo interrompe la riga o dove il riquadro di visualizzazione del controllo esegue il wrapping del testo su una nuova riga. Il limite deve essere impostato in cui inizia una nuova riga.

### <a name="paragraph"></a>Paragraph

[**TextUnit \_ Il**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) paragrafo è un'unità linguistica di testo che rappresenta un paragrafo completo. Un paragrafo deve iniziare subito prima del primo carattere di un paragrafo e in genere deve terminare subito dopo l'ultimo carattere. Tutte le righe vuote che segue un paragrafo devono essere unite nel paragrafo, a meno che un elemento nell'origine del testo non indichi il contrario. In genere, il limite finale di un paragrafo contrassegna anche il limite finale di [**un'unità di testo TextUnit \_ Line.**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)

### <a name="page"></a>Pagina

[**TextUnit \_ Page**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) rappresenta una pagina di testo completa di un documento. I limiti di una pagina devono essere impostati nei punti immediati in cui inizia e termina una pagina.

### <a name="document"></a>Documento

[**TextUnit \_ Document**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) rappresenta l'intero contenuto di un documento supportato dal pattern [di controllo Text.](uiauto-implementingtextandtextrange.md) Non deve esistere testo all'esterno di un intervallo di testo che contiene un documento. Tutti gli oggetti inseriti in un documento, ad esempio le note di annotazione che attraversano un limite di pagina, devono essere considerati come oggetti incorporati del documento e non come parte del contenuto di testo del documento.

## <a name="other-potential-ranges"></a>Altri intervalli potenziali

La specifica corrente del pattern di controllo [TextRange](uiauto-implementingtextandtextrange.md) non consente l'aggiunta di nuovi valori di unità di testo all'enumerazione [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) né la ridefinizione dei valori di unità di testo esistenti. Per esporre altri intervalli potenziali, ad esempio intestazioni e annotazioni, un provider deve esporre questi intervalli come oggetti incorporati con un intervallo di testo associato. In questo modo, è anche possibile aggiungere il supporto per i pattern di controllo appropriati. Questa soluzione è più flessibile ed estendibile rispetto alla definizione di nuove unità di testo.

## <a name="related-topics"></a>Argomenti correlati

### <a name="reference"></a>Riferimento

[TextPatternRangeEndpoint](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)

[ITextRangeProvider::GetChildren](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-getchildren)





### <a name="conceptual"></a>Informazioni concettuali

[Automazione interfaccia utente supporto per il contenuto testuale](uiauto-ui-automation-textpattern-overview.md)

[Uso di controlli basati su testo](uiauto-workingwithtextbasedcontrols.md)