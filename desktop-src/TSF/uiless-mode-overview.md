---
title: Panoramica della modalità UILess
description: Panoramica della modalità UILess
ms.assetid: cc0e4936-eab1-452d-9ba1-188401918e99
keywords:
- Framework servizi di testo (TSF), UILessMode
- TSF (Framework dei servizi di testo), UILessMode
- Applicazioni abilitate per TSF, UILessMode
- UILessMode
- Framework servizi di testo (TSF), UIElement elenco candidati
- TSF (Framework dei servizi di testo), UIElement dell'elenco dei candidati
- Applicazioni abilitate per TSF, UIElement elenco candidati
- UIElement elenco candidati
- Framework servizi di testo (TSF), suggerimento UIElement
- TSF (Text Services Framework), suggerimento UIElement
- Applicazioni abilitate per TSF, suggerimento UIElement
- Suggerimento UIElement
- Framework di servizi di testo (TSF), elementi dell'interfaccia utente predefiniti
- TSF (Text Services Framework), elementi dell'interfaccia utente predefiniti
- Applicazioni abilitate per TSF, elementi dell'interfaccia utente predefiniti
- elementi dell'interfaccia utente predefiniti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7354a88fb28fd0d6bf5f4180ac23359a2117fe7
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104561846"
---
# <a name="uiless-mode-overview"></a>Panoramica della modalità UILess

## <a name="how-to-create-uilessmode"></a>Come creare UILessMode

**Creazione di un thread senza interfaccia utente:** L'applicazione può rendere un'interfaccia utente meno thread di [**ITfThreadMgrEx:: ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgrex-activateex) con ITF \_ AE \_ UIELEMENTENABLEDONLY. Quando ThreadMgr viene attivato con questo flag, solo i suggerimenti che possono controllare l'elemento dell'interfaccia utente vengono attivati sul thread. L'applicazione deve implementare l'interfaccia [**ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) e consigliare l'interfaccia in gestione thread. [**ITfUIElementSink:: BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-beginuielement) viene chiamato quando Tip Mostra la relativa interfaccia utente. L'applicazione può restituire **true** in pbShow param per consentire a tip di visualizzare l'interfaccia utente originale del suggerimento quando l'applicazione non vuole creare un oggetto. Se l'applicazione non consente l'interfaccia utente di TIP, può restituire **false** in pbShow (vedere i diagrammi seguenti). L'applicazione può creare l'interfaccia utente autonomamente ottenendo alcune informazioni dal parametro di *pelement* . Potrebbe trattarsi dell'elenco dei candidati, dell'elemento della barra della lingua o dell'interfaccia utente personalizzata del suggerimento. L'applicazione può essere in grado di comprendere il tipo di interfaccia utente dell'interfaccia [**ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) di QIing. Quando l'interfaccia utente viene modificata, viene chiamato [**ITfUIElementSink:: UpdateUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-updateuielement) . L'applicazione può confrontare il GUID di pElement->GetGuid () per verificare se l'elemento è attualmente disegnato dall'applicazione.

**Creazione di un suggerimento meno compatibile con l'interfaccia utente:** Il suggerimento deve supportare la modalità meno interfaccia utente se vuole eseguire nell'applicazione che non vuole consentire l'interfaccia utente di TIP, ad esempio applicazioni di gioco o applicazioni a schermo intero. Per essere meno compatibile con l'interfaccia utente, TIP deve implementare l'interfaccia [**ITfTextInputProcessorEx**](/windows/desktop/api/Msctf/nn-msctf-itftextinputprocessorex) . Se questa interfaccia non viene implementata, TIP non verrà attivato nel thread della modalità less UI. Inoltre, TIP deve chiamare [**ITFUIElementMgr:: BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement) prima di visualizzare un'interfaccia utente visibile sullo schermo. Questo metodo effettua una chiamata a [**ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) per notificare l'applicazione. E l'applicazione deciderà se è possibile visualizzarla o meno. Quando TIP chiama BeginUIElement (), TIP deve avere l'interfaccia [**ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) per l'interfaccia utente corrispondente. L'applicazione condurrà a QI l'interfaccia per ottenere un'altra interfaccia specifica dell'interfaccia utente per recuperare altre informazioni per creare l'interfaccia utente. Il sistema predefinisce [**ITfCandidateListUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfcandidatelistuielement) e [**ITfReadingInformationUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfreadinginformationuielement) per tip. Quando il suggerimento desidera visualizzare l'elenco dei candidati nel thread della modalità UI less, TIP deve creare un'istanza dell'interfaccia **ITfCandidateListUIElement** e chiamare **ITFUIElementMgr:: BeginUIElement**. Quando viene chiamato [**ITfTextInputProcessorEx:: ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessorex-activateex) , tip è già noto che il thread è l'interfaccia utente, in modo da poter eliminare l'interfaccia utente personalizzata aggiuntiva. Tuttavia, ovviamente, può implementare una propria interfaccia che può essere QIed da e provare a effettuare una notifica. In questo modo, suggerimento e **ITfUIElement** di applicazione possono avere una negoziazione per l'interfaccia utente personalizzata del suggerimento.

## <a name="uielement-supporting-tip"></a>Suggerimento di supporto UIElement

Il suggerimento che supporta UIElement deve essere categorizzato in base al GUID \_ TFCAT \_ TIPCAP \_ UIELEMENTENABLED. Il suggerimento in GUID \_ TFCAT \_ TIPCAP \_ UIELEMENTENABLED deve usare [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) per visualizzare qualsiasi interfaccia utente, in modo che l'applicazione possa controllare la visibilità dell'interfaccia utente.

**Mostra/Nascondi stato di UIElement:** Mostra/Nascondi lo stato indicato dal metodo [**ITfUIElement:: Show**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-show) o [**ITfUIElement::**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-isshown) IsVisible è lo stato visibile effettivo. Non è correlato alla disponibilità di UIElement. UIElement deve essere sempre disponibile quando lo stato di visualizzazione è esistente. Lo stato di visualizzazione è controllabile dall'applicazione. L'applicazione può passare improvvisamente alla modalità UILess e iniziare a disegnare un'interfaccia utente autonomamente, chiamando **ITfUIElement:: Show** con **false** per nascondere tutta l'interfaccia utente del suggerimento. Quindi, suggerimento può assumere una di alcune opzioni. 1) suggerimento può spostare l'elemento UIElement nello stato Hide e avviare la generazione di UpdateUIElement. 2) il suggerimento può completare UIElement poiché l'elemento dell'interfaccia utente non supporta lo stato Hide e Tip chiama EndUIElement () per terminarlo.

## <a name="predefined-ui-elements"></a>Elementi dell'interfaccia utente predefiniti

**Elenco candidati:** L'elenco dei candidati è uno degli elementi principali dell'interfaccia utente per l'input EA. Questo elemento dell'interfaccia utente fornisce l'elenco dei candidati e il numero corrispondente di stringhe candidate per il disegno.

**Finestra informazioni di lettura** La finestra informazioni di lettura è comune per gli input da tastiera cinesi. Contiene la fase che non può essere inserita nel documento come stringa di composizione. Un processore di input cinese apre una piccola finestra di informazioni di lettura che mostra le informazioni di lettura, fonetica o di tipizzazione.

## <a name="the-flow-chart-of-uilessmode"></a>Il diagramma di flusso di UILessMode

![Diagramma che mostra il diagramma di flusso di U I LessMode.](images/tsf-uilessmode-ovw1.gif)

Quando il suggerimento riceve **true** in \* pbShown by [**ITfUIElementMgr:: BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement), il suggerimento non deve chiamare UpdateUIElement per l'oggetto UIElement. È tuttavia necessario che TIP chiami EndUIElement () in modo che [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) e l'applicazione possano tenere traccia dello stato di UIElement. TIP deve chiamare UpdateUIElement () dopo che BeginUIElement () restituisce **false** in \* pbShow. L'applicazione che vuole creare l'interfaccia utente non controlla il contenuto in BeginUIElement (), restituisce semplicemente lo stato di visualizzazione in BeginUIElement () e inizia a controllare il contenuto in UpdateUIElement (). Ad esempio, il flag di aggiornamento dell'UIElement dell'elenco dei candidati presenta tutti i bit al primo UpdateUIElement (). Ciò significa che non è necessario che il contenuto di UIElement sia pronto in BeginUIElement ().

![Diagramma che mostra la chiamata a T I P chiamate a' ITUIElementMgr:: BeginUIElement ()' è BeginUIElement dell'applicazione UIElementSink '.](images/tsf-uilessmode-ovw2.gif)![Il diagramma che mostra l'applicazione restituisce FALSE in * pbShow.](images/tsf-uilessmode-ovw3.gif)![diagramma di flusso uilessmode](images/tsf-uilessmode-ovw4.gif)

## <a name="the-candidate-list-uielement"></a>UIElement dell'elenco dei candidati

**Informazioni su pageIndex:** Nell'applicazione che disegna l'elenco dei candidati verrà calcolato il numero di stringhe per ogni pagina quando viene modificato il contenuto dell'elenco ( \_ è stata impostata la stringa TF CLUIE \_ ). Non è opportuno modificare l'indice della pagina mentre l'elenco dei candidati è disponibile per la modalità UILess. Ciò significa che l'elenco dei candidati del suggerimento deve comportarsi nel paging anziché scorrere quando la selezione viene spostata nella pagina successiva. Se lo scorrimento si verifica in corrispondenza dello spostamento della selezione, l'indice di pagina viene modificato e l'applicazione deve ricalcolare l'indice della pagina. Il risultato potrebbe non essere previsto da TIP.

**Nessuna selezione:** [**ITfCandidateListUIElement:: GetSelection**](/windows/desktop/api/Msctf/nf-msctf-itfcandidatelistuielement-getselection) restituisce \_ false se l'elenco dei candidati non ha una selezione. Il valore restituito del primo parametro non è valido.

 

 




