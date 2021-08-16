---
title: Come eseguire una query su un elemento virtualizzato nella visualizzazione Elementi
description: Questo argomento descrive come usare Microsoft Automazione interfaccia utente recuperare informazioni sull'interfaccia utente sugli elementi virtualizzati nella visualizzazione Windows 7 elementi.
ms.assetid: a0bff8a1-47b1-4750-8086-e2e65a79099e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9196d62e7aa93b21aed15b76b8ced6a9520b27fb5bcee74a0e0d4ddc510c86f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759247"
---
# <a name="how-to-query-a-virtualized-item-in-items-view"></a>Come eseguire una query su un elemento virtualizzato nella visualizzazione Elementi

Questo argomento descrive come usare Microsoft Automazione interfaccia utente recuperare informazioni sull'interfaccia utente sugli elementi virtualizzati nella visualizzazione Windows 7 elementi. In questo argomento sono incluse le sezioni seguenti.

> [!Note]  
> Questo argomento si applica solo Windows 7. Tenere presente che le funzionalità di accessibilità descritte in questo argomento possono cambiare nelle versioni future di Windows.

 

-   [Overview](#overview)
-   [Struttura ad albero della visualizzazione Elementi](#items-view-tree-structure)
-   [Virtualizzazione](#virtualization)
-   [Recupero di un conteggio di tutti gli elementi](#obtaining-a-count-of-all-items)
-   [Recupero di un indice degli elementi rispetto a tutti gli elementi](#obtaining-an-item-index-with-respect-to-all-items)
-   [Recupero di un riferimento a un elemento vitualizzato](#obtaining-a-reference-to-a-vitualized-item)
-   [Scorrimento di un elemento virtualizzato sullo schermo](#scrolling-a-virtualized-item-on-screen)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Visualizzazione elementi è un componente dell'interfaccia utente che consente agli utenti di visualizzare e interagire con file e altri elementi. In Windows 7 la visualizzazione elementi sostituisce il controllo visualizzazione elenco per la presentazione di elementi nella visualizzazione predefinita di Windows Explorer. La visualizzazione Elementi viene usata anche nella finestra di dialogo Elementi comuni, menu Start risultati della ricerca e in altri Windows 7 elementi dell'interfaccia utente che usano il controllo Browser explorer. Rispetto al controllo visualizzazione elenco, la visualizzazione Elementi offre agli utenti i vantaggi seguenti:

-   La visualizzazione Elementi può presentare gli elementi in modi più utili, desiderabili e pertinenti, consentendo agli utenti di trovare e organizzare gli elementi in modo più semplice, rapido e divertente.
-   La visualizzazione Elementi consente di visualizzare grandi set di elementi da origini dati con caratteristiche di prestazioni diverse, consentendo agli utenti di esplorare ed eseguire ricerche nell'intera raccolta di elementi in più origini.

L'immagine seguente mostra la visualizzazione Elementi in Windows Explorer.

![Screenshot che mostra Esplora risorse con il componente di visualizzazione elementi](images/itemsview.gif)

Dal punto di vista dello sviluppatore, la struttura generale e le funzionalità della visualizzazione Elementi sono simili a quelle del controllo visualizzazione elenco. La differenza principale è che la visualizzazione elementi supporta la virtualizzazione, mentre il controllo visualizzazione elenco non lo supporta. Inoltre, la visualizzazione elementi usa due nuove interfacce Automazione interfaccia utente per garantire che il contenuto virtualizzato fornito dalla visualizzazione elementi sia accessibile. Queste interfacce sono descritte nelle sezioni seguenti di questo argomento.

Per informazioni generali sulla virtualizzazione in Automazione interfaccia utente, vedere [Utilizzo di elementi virtualizzati.](uiauto-workingwithvirtualizeditems.md)

## <a name="items-view-tree-structure"></a>Struttura ad albero della visualizzazione Elementi

Nell'Automazione interfaccia utente seguente, l'elemento Automazione interfaccia utente di primo livello della visualizzazione Elementi ha il nome "ItemsView" e il tipo di controllo "list". Nell'immagine precedente, il controllo ItemsView Automazione interfaccia utente elemento è delineato in rosso. Esistono Automazione interfaccia utente elementi sotto il livello superiore di ItemsView, ma in questo documento viene fatto riferimento solo ad altri due elementi Automazione interfaccia utente: elementi di gruppo ed elementi elenco.

Gli elementi del gruppo sono gli Automazione interfaccia utente che contengono tutti gli elementi dell'elenco del gruppo. Il tipo di controllo è "Group" e i relativi nomi variano a seconda del nome del gruppo. Nell'immagine precedente il primo elemento del gruppo contiene sia l'intestazione "A-H (1)" che l'elemento elenco "Cartella" e il nome è "A-H".

Gli elementi dell'elenco sono gli Automazione interfaccia utente che rappresentano gli elementi foglia nella visualizzazione. Il tipo di controllo è "ListItem" e i relativi nomi variano a seconda del nome dell'elemento. Nell'immagine precedente gli elementi dell'elenco sono elementi foglia, ad esempio "Cartella", "Musica" e "Immagine". Questi tre Automazione interfaccia utente elementi sono indicati dai termini elemento ItemsView, elemento Group e elemento ListItem nella parte restante di questo documento.

## <a name="virtualization"></a>Virtualizzazione

La visualizzazione Elementi usa la virtualizzazione, ovvero gli elementi esterni all'area visibile della visualizzazione non vengono recuperati dal sistema e la rappresentazione dell'interfaccia utente non viene creata. Questi elementi sono denominati *elementi virtualizzati.* Poiché non vengono creati, gli elementi virtualizzati non hanno elementi Automazione interfaccia utente e pertanto non vengono visualizzati nell'albero Automazione interfaccia utente quando un client Automazione interfaccia utente enumera l'albero. Inoltre, Automazione interfaccia utente pattern di controllo funzionano solo su elementi visibili. Ad esempio, il pattern di controllo [Selection](uiauto-implementingselection.md) restituisce solo gli elementi selezionati visibili quando un client chiama il [**metodo IUIAutomationSelectionPattern::GetCurrentSelection.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-getcurrentselection)

La visualizzazione Elementi supporta la possibilità di recuperare le informazioni seguenti sugli elementi virtualizzati:

-   Conteggio del numero totale di elementi, inclusi gli elementi virtualizzati
-   Automazione interfaccia utente elementi per gli elementi virtualizzati
-   Automazione interfaccia utente elementi per gli elementi virtualizzati selezionati

## <a name="obtaining-a-count-of-all-items"></a>Recupero di un conteggio di tutti gli elementi

Un client può usare l'elemento ItemsView per ottenere un conteggio di tutti gli elementi, nonché un conteggio degli elementi selezionati. L'elemento ItemsView offre due modi per ottenere questi conteggi. Il primo è ottenere la proprietà ItemStatus dell'elemento ItemsView, il secondo è ottenere proprietà personalizzate dall'elemento ItemsView.

La proprietà ItemStatus è una stringa che specifica un conteggio del numero totale di elementi e un conteggio degli elementi selezionati, separati da una virgola. Ad esempio: "3 elementi, 1 elemento selezionato". Questa stringa è localizzata e può essere comunicata direttamente all'utente.

Le proprietà personalizzate dell'elemento ItemsView includono una proprietà per il conteggio degli elementi e un'altra per il conteggio delle selezioni. includono:

-   GUID della proprietà ItemCount \_ \_ (ABBF5C45-5CCC-47b7-BB4E-87CB87BBD162): numero di tutti gli elementi univoci nella vista. Se raggruppati in base a una proprietà multivalore (MVP) in modo che un singolo elemento possa essere visualizzato più volte, ogni elemento viene conteggiato una sola volta.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Nome a livello di codice: "ItemCount")

-   GUID della proprietà SelectedItemCount \_ \_ (92A053DA-2969-4021-BF27-514CFC2E4A69): numero di tutti gli elementi univoci selezionati nella vista. Se raggruppati in base a una proprietà multivalore (MVP) in modo che un singolo elemento possa essere visualizzato più volte, ogni elemento viene conteggiato una sola volta.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Nome a livello di codice: "SelectedItemCount")

Queste proprietà personalizzate sono definite in Shlguid.h, incluso in Windows Software Development Kit (SDK) e queste proprietà vengono registrate tramite il metodo [**IUIAutomationRegistrar::RegisterProperty.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) Automazione interfaccia utente client usano **RegisterProperty** per recuperare gli identificatori di proprietà (PROPERTYID) per le proprietà personalizzate.

## <a name="obtaining-an-item-index-with-respect-to-all-items"></a>Recupero di un indice degli elementi rispetto a tutti gli elementi

Un client può ottenere l'indice di un elemento ottenendo la proprietà ItemStatus di un elemento ListItem o una proprietà personalizzata di un elemento ListItem.

La proprietà ItemStatus è una stringa che contiene l'indice di un elemento rispetto al numero totale di elementi. Ad esempio: "elemento 1 di 3". Questa stringa è localizzata e può essere comunicata direttamente all'utente.

La proprietà personalizzata seguente ottiene l'indice di un elemento ListItem:

-   GUID della proprietà ItemIndex \_ \_ (92A053DA-2969-4021-BF27-514CFC2E4A69): indice assoluto in base 1 di un elemento. Se raggruppati in base a una proprietà multivalore (MVP) in modo che un singolo elemento possa essere visualizzato due volte, ogni aspetto dell'elemento ottiene un indice separato.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Nome a livello di codice: "ItemIndex")

Questa proprietà personalizzata è definita in Shlguid.h, incluso in Windows SDK, ed è registrata tramite il metodo [**IUIAutomationRegistrar::RegisterProperty.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) Automazione interfaccia utente client usano **RegisterProperty** per recuperare un identificatore di proprietà (PROPERTYID) per la proprietà personalizzata.

## <a name="obtaining-a-reference-to-a-vitualized-item"></a>Recupero di un riferimento a un elemento vitualizzato

Un elemento ItemsView implementa il pattern di controllo [ItemContainer](uiauto-implementingitemcontainer.md) (interfaccia [**IItemContainerProvider),**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) che consente a un client di ottenere un elemento Automazione interfaccia utente per un elemento virtualizzato (un elemento esterno all'area visibile). ItemsView consente al client di trovare un elemento ListItem eseguendo una ricerca nelle proprietà Name e Selection. Il tentativo di cercare qualsiasi altra proprietà avrà esito negativo.

Un elemento virtuale implementa solo il pattern [di controllo VirtualizedItem](uiauto-implementingvirtualizeditem.md) ([**interfaccia IVirtualizedItemProvider).**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) Poiché l'elemento rappresentato da un elemento Automazione interfaccia utente virtuale non esiste ancora, il tentativo di ottenere qualsiasi altro pattern di controllo o proprietà dell'elemento avrà esito negativo.

Entrambi gli elementi ListItem e Group sono virtualizzati, ma solo gli elementi ListItem possono essere restituiti dal pattern [di controllo ItemContainer.](uiauto-implementingitemcontainer.md) Poiché la chiamata al metodo [**IUIAutomationItemContainerPattern::FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) viene eseguita nel thread dell'interfaccia utente e blocca, la visualizzazione non risponde fino al completamento di **FindItemByProperty** e qualsiasi altra chiamata al metodo nel provider deve attendere il completamento di **FindItemByProperty.** In alcuni casi, **FindItemByProperty** deve elaborare l'intero set di dati prima della restituzione, operazione che può essere a elevato utilizzo di risorse. Se si **specifica NULL** come elemento iniziale, **FindItemByProperty** inizia la ricerca con il primo elemento nella visualizzazione.

ItemsView supporta le proprietà seguenti per [**FindItemByProperty:**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty)

-   Name (UIA NamePropertyId): cerca il primo elemento il cui \_ nome corrisponde completamente alla stringa specificata. Alla ricerca non viene applicata la distinzione tra maiuscole e minuscole. I caratteri jolly o la corrispondenza parziale non sono supportati. Se viene specificato un nome **NULL,** viene restituito l'elemento successivo dopo l'elemento iniziale. La specifica **di nomi NULL** consente a Automazione interfaccia utente client di enumerare tutti gli elementi nella vista. Tuttavia, l'enumerazione di tutti gli elementi è sconsigliata perché causa la realizzare tutti gli elementi nella visualizzazione.
-   SelectionItem \_ IsSelected (UIA \_ SelectionItemIsSelectedPropertyId): cerca il primo elemento la cui proprietà SelectionItem \_ IsSelected corrisponde al valore specificato. Specificare **TRUE** per trovare il primo elemento selezionato oppure **FALSE** per trovare il primo elemento non selezionato. Prestare attenzione quando si enumerano tutti gli elementi selezionati perché il numero di elementi selezionati può essere molto elevato, soprattutto se l'utente ha selezionato tutti gli elementi.

## <a name="scrolling-a-virtualized-item-on-screen"></a>Scorrimento di un elemento virtualizzato sullo schermo

Dopo aver ottenuto un riferimento a un elemento Automazione interfaccia utente per un elemento virtualizzato (fuori schermo), il client può scorrere l'elemento nella visualizzazione usando il metodo [**IUIAutomationVirtualizeItemPattern::Realize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) del pattern di [controllo VirtualizedItem.](uiauto-implementingvirtualizeditem.md) Dopo che l'elemento è stato realizzato, è visibile e tutte le proprietà e i pattern di controllo normalmente associati a un elemento ListItem sono disponibili per il client.

Solo gli elementi ListItem ottenuti dal [**metodo IUIAutomationItemContainerPattern::FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) espongono il pattern di [controllo VirtualizedItem.](uiauto-implementingvirtualizeditem.md) Quando si scorre un elemento sullo schermo fuori schermo, l'elemento diventa non valido e il client deve chiamare **FindItemByProperty** per ottenere il riferimento all'esterno dello schermo.

È anche possibile spostare elementi all'interno e all'uscita dalla visualizzazione usando il pattern [di controllo Scroll](uiauto-implementingscroll.md) (o le barre di scorrimento). Gli elementi e i gruppi vengono realizzati mentre scorrono nella visualizzazione e vengono virtualizzati mentre scorrono fuori dalla visualizzazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di elementi virtualizzati](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




