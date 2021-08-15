---
title: Caching Automazione interfaccia utente proprietà e pattern di controllo
description: Quando si usa Microsoft Automazione interfaccia utente, i client spesso devono recuperare più proprietà per più elementi di automazione.
ms.assetid: 948b3bb9-75a9-4197-9680-e6fe7bb86feb
keywords:
- memorizzazione nella cache, Automazione interfaccia utente proprietà
- memorizzazione nella cache, proprietà
- memorizzazione nella cache, Automazione interfaccia utente di controllo
- memorizzazione nella cache, pattern di controllo
- Automazione interfaccia utente,memorizzazione nella cache delle proprietà
- Automazione interfaccia utente,memorizzazione nella cache delle proprietà
- client, memorizzazione nella cache Automazione interfaccia utente proprietà
- client, memorizzazione nella cache Automazione interfaccia utente di controllo
- Automazione interfaccia utente,memorizzazione nella cache dei pattern di controllo
- Automazione interfaccia utente,memorizzazione nella cache del pattern di controllo
- pattern di controllo, memorizzazione nella cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae14fb607dd66ab1a4ea99cd9836f2f74e5c863afef8465843d3ea174186ef29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324975"
---
# <a name="caching-ui-automation-properties-and-control-patterns"></a>Caching Automazione interfaccia utente proprietà e pattern di controllo

Quando si usa Microsoft Automazione interfaccia utente, i client spesso devono recuperare più proprietà per più elementi di automazione. Un client può recuperare singole proprietà un elemento alla volta usando i metodi di recupero delle proprietà, ad esempio [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) o [**CurrentAccessKey.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentaccesskey) Tuttavia, questo metodo è lento e inefficiente perché richiede una chiamata tra processi per ogni proprietà recuperata. Per migliorare le prestazioni, i client possono usare le funzionalità di memorizzazione nella cache (chiamate anche recupero bulk) di Automazione interfaccia utente. Caching consente a un client di recuperare tutte le proprietà desiderate per tutti gli elementi desiderati con una singola chiamata al metodo. Il client può quindi recuperare le singole proprietà dalla cache in base alle esigenze e può ottenere periodicamente un nuovo snapshot della cache, in genere in risposta a eventi che significano modifiche nell'interfaccia utente.

L'applicazione può richiedere la memorizzazione nella cache quando recupera un elemento Automazione interfaccia utente usando un metodo, ad esempio [**IUIAutomation::ElementFromPointBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache), [**IUIAutomationTreeWalker::GetFirstChildElementBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-getfirstchildelementbuildcache)o [**IUIAutomationElement::FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache).

Caching si verifica anche quando si specifica una richiesta di cache durante la sottoscrizione agli eventi. L Automazione interfaccia utente elemento passato al gestore eventi come origine di un evento contiene le proprietà memorizzate nella cache e i pattern di controllo specificati dalla richiesta della cache. Le modifiche apportate alla richiesta della cache dopo la sottoscrizione dell'evento non hanno alcun effetto.

In questo argomento sono contenute le sezioni seguenti.

-   [Richieste della cache](#cache-requests)
    -   [Specifica di pattern di controllo e proprietà da memorizzare nella cache](#specifying-property-and-control-patterns-to-cache)
    -   [Specifica dell'ambito e del filtro di una Caching richiesta](#specifying-the-scoping-and-filtering-of-a-caching-request)
    -   [Intensità dei riferimenti agli elementi](#strength-of-element-references)
-   [Recupero di elementi figlio e padre memorizzati nella cache](#retrieving-cached-children-and-parents)
-   [Recupero di un nuovo snapshot della cache](#retrieving-a-new-snapshot-of-the-cache)
-   [esempi](#examples)
-   [Argomenti correlati](#related-topics)

## <a name="cache-requests"></a>Richieste della cache

Caching comporta la determinazione delle proprietà da recuperare e gli elementi da cui recuperarli e quindi l'uso di queste informazioni per creare una richiesta di cache. Ogni volta che il client ottiene [**un'interfaccia IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per l'elemento dell'interfaccia Automazione interfaccia utente memorizza nella cache le informazioni specificate nella richiesta della cache.

Per creare una richiesta di cache, iniziare usando il metodo [**IUIAutomation::CreateCacheRequest**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createcacherequest) per recuperare un puntatore a interfaccia [**IUIAutomationCacheRequest.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) Configurare quindi la richiesta di cache usando i metodi di **IUIAutomationCacheRequest**.

### <a name="specifying-property-and-control-patterns-to-cache"></a>Specifica di pattern di controllo e proprietà da memorizzare nella cache

È possibile specificare le proprietà da memorizzare nella cache chiamando [**IUIAutomationCacheRequest::AddProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addproperty). È possibile specificare i pattern di controllo da memorizzare nella cache chiamando [**IUIAutomationCacheRequest::AddPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addpattern). Quando un pattern di controllo viene memorizzato nella cache, le relative proprietà non vengono memorizzate automaticamente nella cache. è necessario specificare le proprietà da memorizzare nella cache usando **AddProperty**.

È possibile recuperare una proprietà del pattern di controllo, ad esempio la proprietà Value del pattern di controllo [Value,](uiauto-implementingvalue.md) senza dover recuperare l'intero pattern di controllo nella cache. È necessario recuperare il pattern di controllo solo se è necessario usare un metodo del pattern di controllo.

### <a name="specifying-the-scoping-and-filtering-of-a-caching-request"></a>Specifica dell'ambito e del filtro di una Caching richiesta

È possibile specificare gli elementi di cui memorizzare nella cache le proprietà e i pattern di controllo impostando la proprietà [**IUIAutomationCacheRequest::TreeScope**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) prima di usare la richiesta. L'ambito è relativo agli elementi recuperati dal metodo a cui viene passata la richiesta della cache. Ad esempio, se si imposta solo [**TreeScope \_ Children**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)e quindi si recupera un elemento Automazione interfaccia utente, le proprietà e i pattern di controllo degli elementi figlio di tale elemento vengono memorizzati nella cache, ma le proprietà e i pattern di controllo dell'elemento stesso non vengono memorizzati nella cache. Per assicurarsi che la memorizzazione nella cache sia eseguita per l'elemento recuperato stesso, è necessario includere l'elemento **\_ TreeScope** nella **proprietà IUIAutomationCacheRequest::TreeScope.** Non è possibile impostare l'ambito su **TreeScope \_ Parent** o **TreeScope \_ Ancestors**. Un elemento padre, tuttavia, può essere memorizzato nella cache quando un elemento figlio viene memorizzato nella cache. Vedere Recupero di elementi figlio e padre memorizzati nella cache.

L'estensione della memorizzazione nella cache è interessata anche dalla [**proprietà IUIAutomationCacheRequest::TreeFilter.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treefilter) Per impostazione predefinita, la memorizzazione nella cache viene eseguita solo per gli elementi visualizzati nella visualizzazione controllo dell'Automazione interfaccia utente albero. È possibile, tuttavia, modificare questa proprietà per poter applicare la memorizzazione nella cache a tutti gli elementi o solo agli elementi presenti nella visualizzazione contenuto.

### <a name="strength-of-element-references"></a>Intensità dei riferimenti agli elementi

Quando si recupera un elemento di automazione, per impostazione predefinita è possibile accedere a tutte le proprietà e i pattern di controllo dell'elemento, incluse le proprietà e i pattern di controllo non memorizzati nella cache. È tuttavia possibile specificare che il riferimento all'elemento faccia riferimento solo ai dati memorizzati nella cache, impostando la proprietà [**IUIAutomationCacheRequest::AutomationElementMode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_automationelementmode) su **AutomationElementMode \_ None**. In questo caso, non è possibile accedere alle proprietà non memorizzate nella cache e ai pattern di controllo degli elementi recuperati. Ciò significa che non è possibile accedere alle proprietà correnti, ad esempio [**IUIAutomationElement::CurrentIsEnabled,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisenabled) o recuperare un pattern di controllo usando [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern). Nei pattern di controllo memorizzati nella cache non è possibile chiamare metodi che eseguono azioni sul controllo, ad esempio [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke).

Un esempio di un'applicazione che potrebbe non richiedere riferimenti completi agli oggetti è un'utilità per la lettura dello schermo, che potrebbe preletturare le proprietà del nome e del tipo di controllo degli elementi in una finestra senza che gli oggetti dell'elemento di automazione stessi.

## <a name="retrieving-cached-children-and-parents"></a>Recupero di elementi figlio e padre memorizzati nella cache

Quando si recupera un elemento di automazione e si richiede la memorizzazione nella cache per gli elementi figlio di tale elemento tramite la proprietà [**IUIAutomationCacheRequest::TreeScope**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) della richiesta, è possibile ottenere gli elementi figlio chiamando [**IUIAutomationElement::GetCachedChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedchildren) sull'elemento recuperato.

Se [**l'elemento TreeScope \_**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) è stato incluso nell'ambito della richiesta della cache, l'elemento radice della richiesta può essere recuperato chiamando [**IUIAutomationElement::GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent) su uno degli elementi figlio.

> [!Note]  
> Non è possibile memorizzare nella cache elementi padre o predecessori dell'elemento radice della richiesta.

 

## <a name="retrieving-a-new-snapshot-of-the-cache"></a>Recupero di un nuovo snapshot della cache

La cache è valida solo se nell'interfaccia utente non cambia nulla. L'applicazione è responsabile del recupero di un nuovo snapshot della cache, in genere, in risposta agli eventi.

Se si sottoscrive un evento con una richiesta di cache, si ottiene un nuovo snapshot [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) della cache come origine dell'evento ogni volta che viene chiamato il gestore eventi. È anche possibile recuperare un nuovo snapshot delle informazioni memorizzate nella cache per un elemento chiamando [**IUIAutomationElement::BuildUpdatedCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache). È possibile passare l'oggetto [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) originale per ottenere un nuovo snapshot di tutte le informazioni precedentemente memorizzate nella cache.

Il recupero di un nuovo snapshot della cache non modifica le proprietà dei riferimenti [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) esistenti.

## <a name="examples"></a>Esempio

Per esempi di codice che illustrano come usare le funzionalità di memorizzazione nella cache di Automazione interfaccia utente, vedere [Come usare Caching](uiauto-howto-use-caching.md).

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

 

 




