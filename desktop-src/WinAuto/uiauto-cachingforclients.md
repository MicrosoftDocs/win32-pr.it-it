---
title: Memorizzare nella cache le proprietà e i pattern di controllo di automazione interfaccia utente
description: Quando si usa l'automazione interfaccia utente Microsoft, i client spesso devono recuperare più proprietà per più elementi di automazione.
ms.assetid: 948b3bb9-75a9-4197-9680-e6fe7bb86feb
keywords:
- Caching, proprietà di automazione interfaccia utente
- memorizzazione nella cache, proprietà
- memorizzazione nella cache, pattern di controllo di automazione interfaccia utente
- memorizzazione nella cache, pattern di controllo
- Automazione interfaccia utente, proprietà di Caching
- Automazione interfaccia utente, memorizzazione nella cache delle proprietà
- client, memorizzazione nella cache delle proprietà di automazione interfaccia utente
- client, memorizzazione nella cache dei pattern di controllo di automazione interfaccia utente
- Automazione interfaccia utente, pattern di controllo di memorizzazione nella cache
- Automazione interfaccia utente, Caching pattern di controllo
- pattern di controllo, Caching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f75a7dc9491565fdfdc0ecc73808c2fb6a9d82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395611"
---
# <a name="caching-ui-automation-properties-and-control-patterns"></a>Memorizzare nella cache le proprietà e i pattern di controllo di automazione interfaccia utente

Quando si usa l'automazione interfaccia utente Microsoft, i client spesso devono recuperare più proprietà per più elementi di automazione. Un client può recuperare le singole proprietà un elemento alla volta usando i metodi di recupero delle proprietà, ad esempio [**IUIAutomationElement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) o [**CurrentAccessKey**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentaccesskey). Tuttavia, questo metodo è lento e inefficiente perché richiede una chiamata tra processi per ogni proprietà recuperata. Per migliorare le prestazioni, i client possono usare le funzionalità di memorizzazione nella cache (chiamate anche recupero bulk) dell'automazione interfaccia utente. La memorizzazione nella cache consente a un client di recuperare tutte le proprietà desiderate per tutti gli elementi desiderati con una singola chiamata al metodo. Il client può quindi recuperare le singole proprietà dalla cache in base alle esigenze e può ottenere periodicamente un nuovo snapshot della cache, in genere in risposta a eventi che indicano modifiche nell'interfaccia utente.

L'applicazione può richiedere la memorizzazione nella cache quando recupera un elemento di automazione interfaccia utente usando un metodo, ad esempio [**IUIAutomation:: ElementFromPointBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache), [**IUIAutomationTreeWalker:: GetFirstChildElementBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-getfirstchildelementbuildcache)o [**IUIAutomationElement:: FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache).

La memorizzazione nella cache viene eseguita anche quando si specifica una richiesta di cache durante la sottoscrizione degli eventi. L'elemento di automazione interfaccia utente passato al gestore eventi come origine di un evento contiene le proprietà e i pattern di controllo memorizzati nella cache specificati dalla richiesta della cache. Eventuali modifiche apportate alla richiesta della cache dopo la sottoscrizione dell'evento non hanno alcun effetto.

In questo argomento sono contenute le sezioni seguenti.

-   [Richieste cache](#cache-requests)
    -   [Impostazione della proprietà e pattern di controllo da memorizzare nella cache](#specifying-property-and-control-patterns-to-cache)
    -   [Specifica dell'ambito e del filtro di una richiesta di memorizzazione nella cache](#specifying-the-scoping-and-filtering-of-a-caching-request)
    -   [Livello di attendibilità dei riferimenti agli elementi](#strength-of-element-references)
-   [Recupero di elementi figlio e padre memorizzati nella cache](#retrieving-cached-children-and-parents)
-   [Recupero di un nuovo snapshot della cache](#retrieving-a-new-snapshot-of-the-cache)
-   [esempi](#examples)
-   [Argomenti correlati](#related-topics)

## <a name="cache-requests"></a>Richieste cache

La memorizzazione nella cache comporta la determinazione delle proprietà da recuperare e degli elementi da cui recuperarle e quindi l'utilizzo di queste informazioni per creare una richiesta della cache. Ogni volta che il client ottiene un'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per l'elemento dell'interfaccia utente, l'automazione interfaccia utente memorizza nella cache le informazioni specificate nella richiesta della cache.

Per creare una richiesta della cache, iniziare usando il metodo [**IUIAutomation:: CreateCacheRequest**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createcacherequest) per recuperare un puntatore a interfaccia [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) . Configurare quindi la richiesta della cache usando i metodi di **IUIAutomationCacheRequest**.

### <a name="specifying-property-and-control-patterns-to-cache"></a>Impostazione della proprietà e pattern di controllo da memorizzare nella cache

È possibile specificare le proprietà da memorizzare nella cache chiamando [**IUIAutomationCacheRequest:: AddProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addproperty). È possibile specificare i pattern di controllo da memorizzare nella cache chiamando [**IUIAutomationCacheRequest:: AddPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addpattern). Quando un pattern di controllo viene memorizzato nella cache, le proprietà non vengono automaticamente memorizzate nella cache. è necessario specificare le proprietà che si desidera memorizzare nella cache utilizzando **AddProperty**.

È possibile recuperare una proprietà del pattern di controllo (ad esempio, la proprietà Value del pattern di controllo [value](uiauto-implementingvalue.md) ), senza dover recuperare l'intero pattern di controllo nella cache. È necessario recuperare il pattern di controllo solo se è necessario usare un metodo del pattern di controllo.

### <a name="specifying-the-scoping-and-filtering-of-a-caching-request"></a>Specifica dell'ambito e del filtro di una richiesta di memorizzazione nella cache

È possibile specificare gli elementi di cui si desidera memorizzare nella cache le proprietà e i pattern di controllo impostando la proprietà [**IUIAutomationCacheRequest:: TreeScope**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) prima di utilizzare la richiesta. L'ambito è relativo agli elementi recuperati dal metodo a cui viene passata la richiesta della cache. Se ad esempio si impostano solo gli elementi [**\_ figlio TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)e quindi si recupera un elemento di automazione interfaccia utente, le proprietà e i pattern di controllo degli elementi figlio di tale elemento vengono memorizzati nella cache, ma le proprietà e i pattern di controllo dell'elemento stesso non vengono memorizzati nella cache. Per assicurarsi che la memorizzazione nella cache venga eseguita per l'elemento recuperato, è necessario includere l' **\_ elemento TreeScope** nella proprietà **IUIAutomationCacheRequest:: TreeScope** . Non è possibile impostare l'ambito su **TreeScope \_ padre** o **TreeScope \_ predecessori**. Un elemento padre, tuttavia, può essere memorizzato nella cache quando un elemento figlio viene memorizzato nella cache. Vedere Recupero di elementi figlio e padre memorizzati nella cache.

L'ambito della memorizzazione nella cache è influenzato anche dalla proprietà [**IUIAutomationCacheRequest:: TreeFilter**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treefilter) . Per impostazione predefinita, la memorizzazione nella cache viene eseguita solo per gli elementi visualizzati nella visualizzazione controlli dell'albero di automazione interfaccia utente. È possibile, tuttavia, modificare questa proprietà per poter applicare la memorizzazione nella cache a tutti gli elementi o solo agli elementi presenti nella visualizzazione contenuto.

### <a name="strength-of-element-references"></a>Livello di attendibilità dei riferimenti agli elementi

Quando si recupera un elemento di automazione, per impostazione predefinita si ha accesso a tutte le proprietà e pattern di controllo di tale elemento, incluse le proprietà e i pattern di controllo che non sono stati memorizzati nella cache. Tuttavia, è possibile specificare che il riferimento all'elemento si riferisce solo ai dati memorizzati nella cache, impostando la proprietà [**IUIAutomationCacheRequest:: AutomationElementMode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_automationelementmode) su **AutomationElementMode \_ None**. In questo caso, non è possibile accedere alle proprietà non memorizzate nella cache e ai pattern di controllo degli elementi recuperati. Ciò significa che non è possibile accedere ad alcuna proprietà corrente, ad esempio [**IUIAutomationElement:: CurrentIsEnabled**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisenabled) o recuperare un pattern di controllo usando [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern). Nei pattern di controllo memorizzati nella cache non è possibile chiamare metodi che eseguono azioni sul controllo, ad esempio [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke).

Un esempio di applicazione che potrebbe non avere bisogno di riferimenti completi agli oggetti è un'applicazione per la lettura dello schermo, che potrebbe prerecuperare le proprietà del tipo di controllo e del nome degli elementi in una finestra senza che siano necessari gli oggetti dell'elemento di automazione.

## <a name="retrieving-cached-children-and-parents"></a>Recupero di elementi figlio e padre memorizzati nella cache

Quando si recupera un elemento di automazione e si utilizza la memorizzazione nella cache delle richieste per gli elementi figlio di tale elemento tramite la proprietà [**IUIAutomationCacheRequest:: TreeScope**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) della richiesta, è possibile ottenere gli elementi figlio chiamando [**IUIAutomationElement:: GetCachedChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedchildren) sull'elemento recuperato.

Se [**l' \_ elemento TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) è stato incluso nell'ambito della richiesta della cache, l'elemento radice della richiesta può essere recuperato chiamando [**IUIAutomationElement:: GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent) su uno qualsiasi degli elementi figlio.

> [!Note]  
> Non è possibile memorizzare nella cache elementi padre o predecessori dell'elemento radice della richiesta.

 

## <a name="retrieving-a-new-snapshot-of-the-cache"></a>Recupero di un nuovo snapshot della cache

La cache è valida solo finché non vengono apportate modifiche all'interfaccia utente. L'applicazione è responsabile del recupero di un nuovo snapshot della cache, in genere in risposta agli eventi.

Se si sottoscrive un evento con una richiesta di cache, si ottiene un nuovo snapshot [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) della cache come origine dell'evento ogni volta che viene chiamato il gestore eventi. È anche possibile recuperare un nuovo snapshot delle informazioni memorizzate nella cache per un elemento chiamando [**IUIAutomationElement:: BuildUpdatedCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache). È possibile passare la [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) originale per ottenere un nuovo snapshot di tutte le informazioni precedentemente memorizzate nella cache.

Il recupero di un nuovo snapshot della cache non comporta la modifica delle proprietà di nessun riferimento [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) esistente.

## <a name="examples"></a>Esempio

Per esempi di codice che illustrano come usare le funzionalità di memorizzazione nella cache di automazione interfaccia utente, vedere [come usare la memorizzazione nella cache](uiauto-howto-use-caching.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Ottenere elementi di automazione interfaccia utente](uiauto-obtainingelements.md)
</dt> <dt>

[Cenni preliminari sulle proprietà di automazione interfaccia utente](uiauto-propertiesoverview.md)
</dt> </dl>

 

 




