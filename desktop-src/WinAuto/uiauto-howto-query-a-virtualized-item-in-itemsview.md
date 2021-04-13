---
title: Come eseguire una query su un elemento virtualizzato nella visualizzazione elementi
description: Questo argomento descrive come usare l'automazione interfaccia utente Microsoft per recuperare informazioni sull'interfaccia utente sugli elementi virtualizzati nella visualizzazione elementi di Windows 7.
ms.assetid: a0bff8a1-47b1-4750-8086-e2e65a79099e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a098635d6e1045c6ff4573de088d8455685014d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396663"
---
# <a name="how-to-query-a-virtualized-item-in-items-view"></a>Come eseguire una query su un elemento virtualizzato nella visualizzazione elementi

Questo argomento descrive come usare l'automazione interfaccia utente Microsoft per recuperare informazioni sull'interfaccia utente sugli elementi virtualizzati nella visualizzazione elementi di Windows 7. In questo argomento sono incluse le sezioni seguenti.

> [!Note]  
> Questo argomento si applica solo a Windows 7. Tenere presente che le funzionalità di accessibilità descritte in questo argomento possono cambiare nelle versioni future di Windows.

 

-   [Overview](#overview)
-   [Struttura ad albero di visualizzazione elementi](#items-view-tree-structure)
-   [Virtualizzazione](#virtualization)
-   [Recupero di un conteggio di tutti gli elementi](#obtaining-a-count-of-all-items)
-   [Recupero di un indice di elemento rispetto a tutti gli elementi](#obtaining-an-item-index-with-respect-to-all-items)
-   [Recupero di un riferimento a un elemento Vitualized](#obtaining-a-reference-to-a-vitualized-item)
-   [Scorrimento di un elemento virtualizzato sullo schermo](#scrolling-a-virtualized-item-on-screen)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Visualizzazione elementi è un componente dell'interfaccia utente che consente agli utenti di visualizzare e interagire con i file e altri elementi. In Windows 7, visualizzazione elementi sostituisce il controllo visualizzazione elenco per la presentazione degli elementi nella visualizzazione predefinita di Esplora risorse. La visualizzazione elementi viene usata anche nella finestra di dialogo elemento comune, nei risultati di ricerca del menu Start e in altri elementi dell'interfaccia utente di Windows 7 che usano il controllo browser di Explorer. Rispetto al controllo visualizzazione elenco, visualizzazione elementi offre i vantaggi seguenti agli utenti:

-   La visualizzazione elementi può presentare elementi in modo più utile, auspicabile e pertinente, consentendo agli utenti di trovare e organizzare gli elementi in modo più semplice, rapido e piacevole.
-   La visualizzazione elementi può visualizzare grandi set di elementi da origini dati con caratteristiche di prestazioni diverse, consentendo agli utenti di esplorare e cercare l'intera raccolta di elementi in più origini.

Nell'immagine seguente viene illustrata la visualizzazione elementi in Esplora risorse.

![screenshot che Mostra Esplora risorse con componente visualizzazione elementi](images/itemsview.gif)

Dal punto di vista di uno sviluppatore, la struttura generale e le funzionalità della visualizzazione elementi sono simili a quelle del controllo visualizzazione elenco. La differenza principale è che la visualizzazione elementi supporta la virtualizzazione, mentre il controllo visualizzazione elenco non lo è. Inoltre, la visualizzazione elementi usa due nuove interfacce di automazione interfaccia utente per garantire che il contenuto virtualizzato fornito dalla visualizzazione elementi sia accessibile. Queste interfacce sono descritte nelle sezioni seguenti di questo argomento.

Per informazioni generali sulla virtualizzazione nell'automazione interfaccia utente, vedere [utilizzo di elementi virtualizzati](uiauto-workingwithvirtualizeditems.md).

## <a name="items-view-tree-structure"></a>Struttura ad albero di visualizzazione elementi

Nell'albero di automazione interfaccia utente, l'elemento di automazione interfaccia utente di livello superiore della visualizzazione elementi ha il nome "ItemsView" e il tipo di controllo "list". Nell'immagine precedente, l'elemento di automazione interfaccia utente di ItemsView è descritto in rosso. Diversi elementi di automazione interfaccia utente sono al di sotto del livello principale di ItemsView, ma in questo documento sono presenti solo due elementi di automazione interfaccia utente: elementi del gruppo ed elementi elenco.

Gli elementi del gruppo sono gli elementi di automazione interfaccia utente che contengono tutti gli elementi dell'elenco di tale gruppo, il cui tipo di controllo è "gruppo" e i loro nomi variano a seconda del nome del gruppo. Nell'immagine precedente, il primo elemento del gruppo contiene sia l'intestazione "A-H (1)" che l'elemento dell'elenco "Folder" e il nome è "A-H".

Gli elementi dell'elenco sono gli elementi di automazione interfaccia utente che rappresentano gli elementi foglia nella vista: il tipo di controllo è "ListItem" e i relativi nomi variano a seconda del nome dell'elemento. Nell'immagine precedente, gli elementi dell'elenco sono gli elementi foglia, ad esempio "Folder", "Music" e "Picture". Questi tre elementi di automazione interfaccia utente sono indicati dall'elemento ItemsView, elemento Group e ListItem nella parte restante di questo documento.

## <a name="virtualization"></a>Virtualizzazione

La visualizzazione elementi usa la virtualizzazione, che significa che gli elementi al di fuori dell'area visibile della vista non vengono recuperati dal sistema e la rappresentazione dell'interfaccia utente non viene creata. Questi elementi sono detti *elementi virtualizzati*. Poiché non vengono creati, gli elementi virtualizzati non hanno elementi di automazione interfaccia utente e pertanto non vengono visualizzati nell'albero di automazione interfaccia utente quando un client di automazione interfaccia utente enumera l'albero. Inoltre, i pattern di controllo di automazione interfaccia utente funzionano solo su elementi visibili. Ad esempio, il pattern di controllo [Selection](uiauto-implementingselection.md) restituisce solo gli elementi selezionati visibili quando un client chiama il metodo [**IUIAutomationSelectionPattern:: GetCurrentSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-getcurrentselection) .

Visualizzazione elementi supporta la possibilità di recuperare le seguenti informazioni sugli elementi virtualizzati:

-   Conteggio del numero totale di elementi, inclusi gli elementi virtualizzati
-   Elementi di automazione interfaccia utente per elementi virtualizzati
-   Elementi di automazione interfaccia utente per gli elementi virtualizzati selezionati

## <a name="obtaining-a-count-of-all-items"></a>Recupero di un conteggio di tutti gli elementi

Un client può usare l'elemento ItemsView per ottenere un conteggio di tutti gli elementi, nonché un conteggio degli elementi selezionati. L'elemento ItemsView fornisce due modi per ottenere questi conteggi. Il primo consiste nell'ottenere la proprietà ItemStatus dell'elemento ItemsView e la seconda ottenendo proprietà personalizzate dall'elemento ItemsView.

La proprietà ItemStatus è una stringa che specifica un conteggio del numero totale di elementi e un conteggio degli elementi selezionati, separati da una virgola. Ad esempio: "3 elementi, 1 elemento selezionato". Questa stringa è localizzata e può essere comunicata direttamente all'utente.

Le proprietà personalizzate dell'elemento ItemsView includono una proprietà per il numero di elementi e un'altra per il numero di selezioni. e comprendono:

-   ItemCount \_ Property \_ GUID (ABBF5C45-5CCC-47B7-BB4E-87CB87BBD162): numero di tutti gli elementi univoci nella visualizzazione. Se raggruppati in base a una proprietà multivalore (MVP), in modo che un singolo elemento possa essere visualizzato più volte, ogni elemento viene conteggiato una sola volta.

    (UIAutomationType: [**UIAutomationType \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), nome a livello di codice: "ItemCount")

-   \_ \_ GUID della proprietà SELECTEDITEMCOUNT (92A053DA-2969-4021-BF27-514CFC2E4A69): numero di tutti gli elementi univoci selezionati nella vista. Se raggruppati in base a una proprietà multivalore (MVP), in modo che un singolo elemento possa essere visualizzato più volte, ogni elemento viene conteggiato una sola volta.

    (UIAutomationType: [**UIAutomationType \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), nome a livello di codice: "SelectedItemCount")

Queste proprietà personalizzate sono definite in Shlguid. h, incluso in Windows Software Development Kit (SDK), e queste proprietà vengono registrate tramite il metodo [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) . I client di automazione interfaccia utente usano **RegisterProperty** per recuperare gli identificatori di proprietà (PROPERTYIDs) per le proprietà personalizzate.

## <a name="obtaining-an-item-index-with-respect-to-all-items"></a>Recupero di un indice di elemento rispetto a tutti gli elementi

Un client può ottenere l'indice di un elemento ottenendo la proprietà ItemStatus di un elemento ListItem oppure ottenendo una proprietà personalizzata di un elemento ListItem.

La proprietà ItemStatus è una stringa che contiene l'indice di un elemento rispetto al numero totale di elementi. Ad esempio: "elemento 1 di 3". Questa stringa è localizzata e può essere comunicata direttamente all'utente.

La proprietà personalizzata seguente ottiene l'indice dell'elemento di un elemento ListItem:

-   \_ \_ GUID della proprietà ITEMINDEX (92A053DA-2969-4021-BF27-514CFC2E4A69): indice assoluto in base 1 di un elemento. Se raggruppati in base a una proprietà multivalore (MVP), in modo che un singolo elemento possa essere visualizzato due volte, ogni aspetto dell'elemento ottiene un indice separato.

    (UIAutomationType: [**UIAutomationType \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), nome a livello di codice: "ItemIndex")

Questa proprietà personalizzata è definita in Shlguid. h, inclusa nella Windows SDK, ed è registrata tramite il metodo [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) . I client di automazione interfaccia utente usano **RegisterProperty** per recuperare un identificatore di proprietà (PROPERTYIDs) per la proprietà personalizzata.

## <a name="obtaining-a-reference-to-a-vitualized-item"></a>Recupero di un riferimento a un elemento Vitualized

Un elemento ItemsView implementa il pattern di controllo [ItemContainer](uiauto-implementingitemcontainer.md) (interfaccia [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) ), che consente a un client di ottenere un elemento di automazione interfaccia utente per un elemento virtualizzato (un elemento che si trova al di fuori dell'area visibile). ItemsView consente al client di trovare un elemento ListItem eseguendo una ricerca sulle proprietà Name e Selection. il tentativo di eseguire la ricerca in qualsiasi altra proprietà avrà esito negativo.

Un elemento virtuale implementa solo il pattern di controllo [VirtualizedItem](uiauto-implementingvirtualizeditem.md) (interfaccia [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) ). Poiché l'elemento rappresentato da un elemento di automazione interfaccia utente virtualizzato non esiste ancora, il tentativo di ottenere qualsiasi altro pattern di controllo o proprietà dell'elemento avrà esito negativo.

Gli elementi ListItem e Group sono virtualizzati, ma solo gli elementi ListItem possono essere restituiti dal pattern di controllo [ItemContainer](uiauto-implementingitemcontainer.md) . Poiché la chiamata al metodo [**IUIAutomationItemContainerPattern:: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) viene eseguita sul thread dell'interfaccia utente e sta bloccando, la visualizzazione non risponde fino a quando **FindItemByProperty** non restituisce il risultato e qualsiasi altra chiamata al metodo nel provider deve attendere fino al termine di **FindItemByProperty** . In alcuni casi, **FindItemByProperty** deve elaborare l'intero set di dati prima di restituire, operazione che può richiedere un utilizzo intensivo delle risorse. Se si specifica **null** come elemento iniziale, **FindItemByProperty** inizia la ricerca con il primo elemento nella visualizzazione.

ItemsView supporta le proprietà seguenti per [**FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty):

-   Nome (UIA \_ NamePropertyId): Cerca il primo elemento il cui nome corrisponde completamente alla stringa specificata. Alla ricerca non viene applicata la distinzione tra maiuscole e minuscole. I caratteri jolly o le corrispondenze parziali non sono supportati. Se viene specificato un nome **null** , viene restituito l'elemento successivo dopo l'elemento iniziale. La specifica di nomi **null** consente a un client di automazione interfaccia utente di enumerare tutti gli elementi nella visualizzazione. Tuttavia, l'enumerazione di tutti gli elementi è sconsigliata perché causa la realizzazione di tutti gli elementi della vista.
-   SelectionItem \_ IsSelected ( \_ SelectionItemIsSelectedPropertyId UIA): Cerca il primo elemento la cui \_ Proprietà SelectionItem IsSelected corrisponde al valore specificato. Specificare **true** per trovare il primo elemento selezionato oppure **false** per trovare il primo elemento non selezionato. Prestare attenzione durante l'enumerazione di tutti gli elementi selezionati perché il numero di elementi selezionati può essere molto elevato, soprattutto se l'utente ha selezionato tutti gli elementi.

## <a name="scrolling-a-virtualized-item-on-screen"></a>Scorrimento di un elemento virtualizzato sullo schermo

Dopo aver ottenuto un riferimento a un elemento di automazione interfaccia utente per un elemento virtualizzato (fuori schermo), il client può scorrere l'elemento nella visualizzazione usando il metodo [**IUIAutomationVirtualizeItemPattern:: réalisateur**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) del pattern di controllo [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . Una volta realizzato, l'elemento è visibile e tutte le proprietà e i pattern di controllo normalmente associati a un elemento ListItem sono disponibili per il client.

Solo gli elementi ListItem ottenuti dal metodo [**IUIAutomationItemContainerPattern:: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) espongono il pattern di controllo [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . Quando un elemento sullo schermo viene spostato fuori schermo, l'elemento diventa non valido e il client deve chiamare **FindItemByProperty** per ottenere il riferimento fuori schermo.

È anche possibile spostare elementi all'interno e all'esterno della visualizzazione usando il pattern di controllo [Scroll](uiauto-implementingscroll.md) (oppure usando le barre di scorrimento). Gli elementi e i gruppi vengono realizzati mentre scorrono nella visualizzazione e vengono virtualizzati quando scorrono fuori dalla visualizzazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo degli elementi virtualizzati](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




