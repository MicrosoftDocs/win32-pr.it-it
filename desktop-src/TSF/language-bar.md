---
title: Barra della lingua (servizi di testo)
description: Barra della lingua
ms.assetid: 82b92567-fdc1-488c-b395-4cb95257955c
keywords:
- Framework servizi di testo (TSF), barra della lingua
- TSF (Framework dei servizi di testo), barra della lingua
- Servizi di testo, barra della lingua
- barra della lingua
- Framework servizi di testo (TSF), pulsanti
- TSF (Framework di servizi di testo), pulsanti
- Servizi di testo, pulsanti
- Framework servizi di testo (TSF), menu
- TSF (Framework di servizi di testo), menu
- Servizi di testo, menu
- stili pulsante
- pulsanti di menu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41d64a488406f6eefcff5fef6c11093af00bc5b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400171"
---
# <a name="language-bar-text-services"></a>Barra della lingua (servizi di testo)

## <a name="implementing-the-language-bar-object"></a>Implementazione dell'oggetto barra della lingua

Per supportare l'aggiunta di un elemento alla barra della lingua, un servizio di testo deve implementare un oggetto che supporta l'interfaccia [ITfSource](/windows/desktop/api/msctf/nn-msctf-itfsource) e uno degli elementi di controllo [ITfLangBarItem](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem) . Quando l'elemento viene installato, la barra della lingua installa un sink [ITfLangBarItemSink](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemsink) chiamando l'elemento [ITfSource:: adviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) con IID \_ ITfLangBarItemSink. L'elemento utilizza l'interfaccia **ITfLangBarItemSink** per notificare alla barra della lingua le modifiche, ad esempio quando l'elemento è nascosto, visualizzato, abilitato o disabilitato.

È possibile installare quattro tipi di elementi della barra della lingua e ognuna delle interfacce richieste viene creata da **ITfLangBarItem**. Di seguito sono riportati i possibili elementi di controllo **ITfLangBarItem** .



|               |                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pulsante        | Un pulsante della barra della lingua funziona come un pulsante di comando, un controllo o un menu sulla barra della lingua. L'oggetto deve supportare l'interfaccia ITfLangBarItemButton.                   |
| Palloncino       | Un fumetto della barra della lingua funge da notifica popup sulla barra della lingua. L'oggetto deve supportare l'interfaccia ITfLangBarItemBalloon.                                       |
| Bitmap        | Una bitmap della barra della lingua funziona come elemento statico sulla barra della lingua che visualizza una bitmap. L'oggetto deve supportare l'interfaccia ITfLangBarItemBitmap.                       |
| Pulsante bitmap | Un pulsante bitmap della barra del linguaggio funziona come un elemento Button sulla barra della lingua che visualizza testo e una bitmap. L'oggetto deve supportare l'interfaccia ITfLangBarItemBitmapButton. |



 

## <a name="button-styles"></a>Stili dei pulsanti

Un elemento Button può funzionare come uno dei seguenti. La funzione dell'elemento del pulsante è determinata dai flag impostati nel membro **dwStyle** della struttura [tf \_ LANGBARITEMINFO](/windows/desktop/api/ctfutb/ns-ctfutb-tf_langbariteminfo) nel metodo [ITfLangBarItem:: GetInfo](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo) .



|               |                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pulsante        | Il pulsante funziona come un pulsante di comando standard. Questo stile di pulsante è identificato dallo stile del pulsante BTN di TF \_ LBI \_ Style \_ \_ . ITfLangBarItemButton:: OnClick viene chiamato quando si fa clic sull'elemento. ITfLangBarItemButton:: InitMenu e ITfLangBarItemButton:: OnMenuSelect non vengono usati.                                                                                                   |
| Interruttore | Il pulsante funziona come un controllo interruttore in grado di gestire uno stato selezionato, in modo analogo a una casella di controllo. Questo stile di pulsante è identificato dallo \_ stile di \_ \_ \_ attivazione/disimpostazione BTN di LBI Style. ITfLangBarItemButton:: OnClick viene chiamato quando si fa clic sull'elemento. ITfLangBarItemButton:: InitMenu e ITfLangBarItemButton:: OnMenuSelect non vengono usati.                                                  |
| Menu          | Il pulsante funziona come menu a discesa. Questo stile di pulsante è identificato dallo \_ stile del \_ menu BTN di LBI di tipo TF \_ \_ . ITfLangBarItemButton:: InitMenu viene chiamato quando si fa clic sul pulsante. Quando l'utente seleziona un elemento nel menu, la barra della lingua chiama ITfLangBarItemButton:: OnMenuSelect con l'identificatore della voce di menu selezionata. ITfLangBarItemButton:: OnClick non utilizzato. |



 

## <a name="implementing-a-menu-button"></a>Implementazione di un pulsante di menu

Quando l'utente fa clic su un pulsante di menu, la barra della lingua chiama [ITfLangBarItemButton:: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu). L'elemento aggiunge elementi al menu usando l'interfaccia [ITfMenu](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) passata a InitMenu.

Per aggiungere un sottomenu al menu, chiamare [ITfMenu:: AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) con il \_ sottomenu TF LBMENUF \_ . Al termine, viene restituito un nuovo oggetto **ITfMenu** che rappresenta il sottomenu nel parametro *ppMenu* di AddMenuItem. Questo nuovo oggetto menu viene usato per aggiungere elementi al sottomenu.

Quando l'utente seleziona un elemento nel menu, la barra della lingua chiama [ITfLangBarItemButton:: OnMenuSelect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) con l'identificatore della voce di menu selezionata.

## <a name="adding-items-to-the-language-bar"></a>Aggiunta di elementi alla barra della lingua

Un servizio di testo deve aggiungere i relativi elementi alla barra della lingua quando viene chiamato il metodo [ITfTextInputProcessor:: Activate](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate) e rimuoverli quando viene chiamato il relativo [ITfTextInputProcessor::D ttiva](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-deactivate) .

Per aggiungere un elemento alla barra della lingua, il servizio di testo ottiene un'interfaccia [ITfLangBarItemMgr](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr) chiamando ITfThreadMgr:: QUERYINTERFACE con IID \_ ITfLangBarItemMgr. Il servizio di testo chiama quindi [ITfLangBarItemMgr:: AddItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem) con il puntatore all'oggetto elemento della barra della lingua.

Il servizio di testo deve rimuovere l'elemento quando è disattivato. Il servizio di testo utilizza la stessa interfaccia **ITfLangBarItemMgr** utilizzata per aggiungere gli elementi o ottenere un'altra istanza dell'interfaccia. Il servizio di testo chiama quindi [ITfLangBarItemMgr:: RemoveItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-removeitem) con il puntatore di interfaccia dell'elemento da rimuovere.

## <a name="extending-system-language-bar-items"></a>Estensione degli elementi della barra della lingua di sistema

TSF offre la possibilità di aggiungere voci di menu ai menu della barra delle lingue esistente. Questo consente a un servizio di testo di aggiungere elementi al menu di un altro servizio di testo senza dover aggiungere un pulsante separato alla barra degli strumenti. Consente inoltre di organizzare le voci di menu in gruppi logici. Ad esempio, un servizio di testo che fornisce funzionalità aggiuntive al servizio testo vocale standard può aggiungere elementi al menu del servizio testo vocale anziché aggiungere il proprio pulsante di menu di primo livello.

Un servizio di testo fornisce un'estensione del menu della barra delle lingue implementando un oggetto che supporta l'interfaccia [ITfSystemLangBarItemSink](/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritemsink) . Questa interfaccia funziona esattamente come l'interfaccia [ITfLangBarItemButton](/windows/desktop/api/Ctfutb/nn-ctfutb-itflangbaritembutton) per un pulsante di menu. Quando viene visualizzato il menu, il servizio di testo esteso chiama [ITfSystemLangBarItemSink:: InitMenu](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu). L'estensione aggiunge elementi al menu usando l'interfaccia [ITfMenu](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) passata a **InitMenu**. Quando l'utente seleziona un elemento aggiunto dall'estensione, il servizio di testo esteso chiama [ITfSystemLangBarItemSink:: OnMenuSelect](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-onmenuselect) con l'identificatore della voce di menu selezionata.

Per installare un'estensione del menu della barra delle lingue, il servizio di testo completa i passaggi seguenti.

1.  Ottenere l'interfaccia **ITfLangBarItem** per l'elemento da estendere chiamando [ITfLangBarItemMgr:: GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem) con il **GUID** per l'elemento da estendere.
2.  Ottenere l'interfaccia **ITfSource** per l'elemento da estendere chiamando ITfLangBarItem:: QUERYINTERFACE con IID \_ ITfSource.
3.  Chiamare [ITfSource:: adviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) con IID \_ ITfSystemLangBarItemSink e il puntatore all'oggetto **ITfSystemLangBarItemSink** . Se ITfSource:: AdviseSink ha esito negativo, il servizio di testo non supporta le estensioni di menu.

[ITfSource:: UnadviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink)**ITfSource:: adviseSink**

## <a name="supporting-language-bar-menu-extensions"></a>Supporto delle estensioni del menu della barra Lingue

Un servizio di testo può consentire ad altri servizi di testo di aggiungere elementi ai menu della barra della lingua, come illustrato in precedenza. Il servizio di testo che deve pubblicare il GUID in modo che l'elemento possa essere ottenuto chiamando [ITfLangBarItemMgr:: GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem).

Per supportare le estensioni di menu, il servizio di testo deve supportare l'interfaccia [ITfSource](/windows/desktop/api/msctf/nn-msctf-itfsource) . La procedura seguente consente di abilitare il supporto per una o più estensioni di menu.

1.  Quando viene chiamato [ITfSource:: adviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) con IID \_ ITfSystemLangBarItemSink, il servizio di testo deve archiviare l'interfaccia **ITfSystemLangBarItemSink** e restituire un valore del cookie che identificherà l'estensione.
2.  Quando viene chiamato [ITfLangBarItemButton:: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) , il servizio di testo chiama il metodo [ITfSystemLangBarItemSink:: InitMenu](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu) dell'estensione. Il servizio di testo deve implementare un modo per identificare le voci di menu aggiunte dall'estensione anziché gli elementi aggiunti dal servizio di testo stesso.
3.  Quando [ITfLangBarItemButton:: OnMenuSelect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) viene chiamato con un identificatore di voce di menu che appartiene a un'estensione, il servizio di testo chiama il metodo **ITfSystemLangBarItemSink:: OnMenuSelect** delle estensioni.
4.  Quando [ITfSource:: UnadviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink) viene chiamato con il cookie appropriato, il servizio di testo rimuove l'estensione di menu.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come configurare il Framework dei servizi di testo](how-to-set-up-tsf.md)
</dt> <dt>

[Barra della lingua (applicazioni)](language-bar-app.md)
</dt> </dl>

 

 
