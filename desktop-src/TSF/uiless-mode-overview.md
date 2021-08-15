---
title: Cenni preliminari sulla modalità senza interfaccia utente
description: Cenni preliminari sulla modalità senza interfaccia utente
ms.assetid: cc0e4936-eab1-452d-9ba1-188401918e99
keywords:
- Framework servizi di testo (TSF),UILessMode
- TSF (Framework servizi di testo),UILessMode
- Applicazioni abilitate per TSF, UILessMode
- UILessMode
- Framework servizi di testo (TSF),list candidate UIElement
- TSF (Framework servizi di testo),list candidate UIElement
- Applicazioni abilitate per TSF, uiElement dell'elenco candidati
- UIElement dell'elenco di candidati
- Framework servizi di testo (TSF),UIElement TIP
- TSF (Framework servizi di testo),UIElement TIP
- Applicazioni abilitate per TSF, SUGGERIMENTO UIElement
- SUGGERIMENTO DI UIElement
- Framework servizi di testo (TSF), elementi predefiniti dell'interfaccia utente
- TSF (Framework servizi di testo),elementi predefiniti dell'interfaccia utente
- applicazioni abilitate per TSF, elementi predefiniti dell'interfaccia utente
- elementi predefiniti dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdac8e43cc8342c50a6d232b801af0c65315fd407b9f413f2b5fdcb7074282fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949864"
---
# <a name="uiless-mode-overview"></a>Cenni preliminari sulla modalità senza interfaccia utente

## <a name="how-to-create-uilessmode"></a>Come creare UILessMode

**Creazione di thread senza interfaccia utente:** L'applicazione può rendere un'interfaccia utente meno thread di [**ITfThreadMgrEx::ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgrex-activateex) con ITF \_ AE \_ UIELEMENTENABLEDONLY. Quando ThreadMgr viene attivato con questo flag, nel thread vengono attivati solo i TIP che possono controllare il relativo elemento dell'interfaccia utente. L'applicazione deve implementare [**l'interfaccia ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) e consigliare l'interfaccia nella gestione thread. [**ITfUIElementSink::BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-beginuielement) viene chiamato quando TIP mostra l'interfaccia utente. L'applicazione può restituire **TRUE** nel parametro pbShow per consentire a TIP di visualizzare l'interfaccia utente originale di TIP quando l'applicazione non vuole disegnare. Se l'applicazione non consente l'interfaccia utente di TIP, può restituire **FALSE** in pbShow (vedere i diagrammi seguenti). L'applicazione può disegnare l'interfaccia utente da sola ottenendo alcune informazioni dal *parametro pElement.* Può trattarsi dell'elenco dei candidati, dell'elemento della barra della lingua o dell'interfaccia utente personalizzata di TIP. L'applicazione può conoscere il tipo di interfaccia utente tramite QIing [**interfaccia ITfUIElement.**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) Quando l'interfaccia utente viene modificata, viene chiamato [**ITfUIElementSink::UpdateUIElement.**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-updateuielement) L'applicazione può confrontare il GUID di pElement->GetGUID() per determinare se l'elemento è attualmente disegnato dall'applicazione.

**Suggerimento senza interfaccia utente:** TIP deve supportare la modalità ui less se vuole essere eseguita nell'applicazione che non vuole consentire l'interfaccia utente di TIP, ad esempio l'applicazione di gioco o le applicazioni a schermo intero. Per essere meno compatibile con l'interfaccia utente, TIP deve implementare [**l'interfaccia ITfTextInputProcessorEx.**](/windows/desktop/api/Msctf/nn-msctf-itftextinputprocessorex) Se questa interfaccia non viene implementata, TIP non verrà attivato nel thread ui less mode. Tip deve anche chiamare [**ITFUIElementMgr::BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement) prima di visualizzare un'interfaccia utente visibile sullo schermo. Questo metodo effettua una chiamata a [**ITfUIElementSink per**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) inviare una notifica all'applicazione. E l'applicazione deciderà se può essere visualizzata o meno. Quando TIP chiama BeginUIElement(), TIP deve avere [**l'interfaccia ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) per l'interfaccia utente corrispondente. L'applicazione domanderà l'interfaccia per ottenere un'altra interfaccia specifica dell'interfaccia utente per recuperare altre informazioni per disegnare l'interfaccia utente. System prefissi [**ITfCandidateListUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfcandidatelistuielement) e [**ITfReadingInformationUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfreadinginformationuielement) per TIP. Quando TIP vuole visualizzare l'elenco dei candidati nel thread ui less mode, TIP deve creare un'istanza **dell'interfaccia ITfCandidateListUIElement** e chiamare **ITFUIElementMgr::BeginUIElement**. Quando [**viene chiamato ITfTextInputProcessorEx::ActivateEx,**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessorex-activateex) TIP sa già che il thread è meno interfaccia utente, quindi può eliminare l'interfaccia utente personalizzata aggiuntiva. Tuttavia, naturalmente, può implementare la propria interfaccia da cui è possibile eseguire l'QI e provare a inviare una notifica. Pertanto TIP e l'interfaccia **ITfUIElement** dell'applicazione possono avere una negoziazione per l'interfaccia utente personalizzata TIP.

## <a name="uielement-supporting-tip"></a>SUGGERIMENTO di supporto per UIElement

Il suggerimento che supporta UIElement deve essere categorizzato in base al GUID \_ TFCAT \_ TIPCAP \_ UIELEMENTENABLED. TIP in GUID \_ TFCAT TIPCAP UIELEMENTENABLED deve usare \_ \_ [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) per visualizzare qualsiasi interfaccia utente in modo che l'applicazione possa controllare la visibilità dell'interfaccia utente.

**Mostra/Nascondi lo stato di UIElement:** Lo stato Show/Hide indicato dal metodo [**ITfUIElement::Show**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-show) o [**ITfUIElement::IsShown**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-isshown) è lo stato visibile effettivo. Non è correlato alla disponibilità di UIElement. UIElement deve essere sempre disponibile quando lo stato di visualizzazione esiste. Lo stato di visualizzazione è controllabile dall'applicazione. L'applicazione può passare improvvisamente alla modalità senza interfaccia utente e iniziare a disegnare un'interfaccia utente da sola, chiamando **ITfUIElement::Show** con **FALSE** per nascondere tutta l'interfaccia utente di TIP. Tip può quindi scegliere tra alcune opzioni. 1) TIP può spostare UIElement sullo stato Nascondi e avviare la generazione di UpdateUIElement. 2) TIP può terminare UIElement perché l'elemento dell'interfaccia utente non supporta lo stato Hide e Tip chiama EndUIElement() per completarlo.

## <a name="predefined-ui-elements"></a>Elementi predefiniti dell'interfaccia utente

**Elenco di candidati:** L'elenco dei candidati è uno degli elementi principali dell'interfaccia utente per l'input EA. Questo elemento dell'interfaccia utente fornisce l'elenco di candidati e il numero corrispondente delle stringhe candidate per il disegno.

**Finestra di lettura delle informazioni** La finestra delle informazioni di lettura è comune per l'input da tastiera cinese. Contiene la fase che non può essere inserita nel documento come stringa di composizione. Alcuni processori di input in cinese apre una piccola finestra di informazioni di lettura che mostra le informazioni di lettura, fonetica o digitazione.

## <a name="the-flow-chart-of-uilessmode"></a>Diagramma di flusso di UILessMode

![Diagramma che mostra il diagramma di flusso U I LessMode.](images/tsf-uilessmode-ovw1.gif)

Dopo che TIP ha ricevuto **TRUE** in \* pbShown da [**ITfUIElementMgr::BeginUIElement,**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement)tip non deve chiamare UpdateUIElement per UIElement. TIP deve tuttavia chiamare EndUIElement() in modo che [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) e l'applicazione possano tenere traccia dello stato di UIElement. TIP deve chiamare UpdateUIElement() dopo che BeginUIElement() restituisce **FALSE** in \* pbShow. L'applicazione che vuole disegnare l'interfaccia utente non controlla il contenuto in BeginUIElement(), restituisce semplicemente lo stato di visualizzazione in BeginUIElement() e inizia a controllare il contenuto in UpdateUIElement(). Ad esempio, il flag di aggiornamento dell'elenco di candidati UIElement include tutti i bit al primo UpdateUIElement(). Ciò significa che il contenuto di UIElement non deve essere pronto in BeginUIElement().

![Diagramma che mostra quando il provider di funzionalità chiama 'ITUIElementMgr::BeginUIElement()' e 'BeginUIElement di UIElementSink' dell'applicazione.](images/tsf-uilessmode-ovw2.gif)![Diagramma che mostra che l'applicazione restituisce FALSE in *pbShow.](images/tsf-uilessmode-ovw3.gif)![Diagramma di flusso uilessmode](images/tsf-uilessmode-ovw4.gif)

## <a name="the-candidate-list-uielement"></a>UiElement dell'elenco di candidati

**Informazioni su PageIndex:** L'applicazione che disegna l'elenco di candidati calcolerà il numero di stringhe per pagina quando il contenuto dell'elenco viene modificato (è impostato TF \_ CLUIE \_ STRING). Non è bene modificare l'indice della pagina mentre l'elenco dei candidati è disponibile per la modalità senza interfaccia utente. Ciò significa che l'elenco di candidati di TIP deve comportarsi come il paging anziché scorrere quando la selezione viene spostata nella pagina successiva. Se lo scorrimento avviene in corrispondenza dello spostamento della selezione, l'indice della pagina viene modificato e l'applicazione deve ricalcolare l'indice della pagina. Il risultato potrebbe non essere previsto da TIP.

**Nessuna selezione:** [**ITfCandidateListUIElement::GetSelection**](/windows/desktop/api/Msctf/nf-msctf-itfcandidatelistuielement-getselection) restituisce S \_ FALSE, se l'elenco di candidati non ha una selezione. Il valore restituito del primo parametro non è valido.

 

 




