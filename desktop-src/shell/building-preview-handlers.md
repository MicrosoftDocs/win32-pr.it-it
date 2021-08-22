---
description: Questo argomento illustra le interfacce e i metodi specifici necessari per creare un gestore di anteprima.
ms.assetid: 6c240a63-c184-4b65-9483-794f5de4d695
title: Compilazione di gestori di anteprima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a810f15fed66d69bce32387249a2e0d678a1eb6c0dd918ec5df2e1ddbeb5be8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032919"
---
# <a name="building-preview-handlers"></a>Compilazione di gestori di anteprima

Questo argomento illustra le interfacce e i metodi specifici necessari per creare un gestore di anteprima.

Un gestore di anteprima deve implementare le interfacce seguenti:

-   [IInitializeWithStream::Initialize](#iinitializewithstreaminitialize) (scelta fortemente preferita), [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)o [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [IObjectWithSite](#iobjectwithsite)
-   [IOleWindow](#iolewindow)
-   [IPreviewHandler](#ipreviewhandler)

Se il gestore dell'anteprima supporta le impostazioni visive fornite dall'host, ad esempio il colore di sfondo e il tipo di carattere, deve implementare anche l'interfaccia seguente:

-   [IPreviewHandlerVisuals](#ipreviewhandlervisuals)

In questo argomento si presuppone che il gestore di anteprima sia inizializzato con un flusso e sia registrato per una determinata estensione di file.

## <a name="iinitializewithstreaminitialize"></a>IInitializeWithStream::Initialize

Archiviare [**i parametri IStream**](/windows/win32/api/objidl/nn-objidl-istream) e mode in modo che sia possibile leggere i dati dell'elemento quando si è pronti per visualizzare l'anteprima dell'elemento. Non caricare i dati in [**Inizializzare**](/windows/desktop/api/Propsys/nf-propsys-iinitializewithstream-initialize). Caricare i dati in [**IPreviewHandler::D oPreview appena prima**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) del rendering.

## <a name="iobjectwithsite"></a>IObjectWithSite

-   [IObjectWithSite::SetSite](#iobjectwithsitesetsite)
-   [IObjectWithSite::GetSite](#iobjectwithsitegetsite)

### <a name="iobjectwithsitesetsite"></a>IObjectWithSite::SetSite

Archiviare il [**puntatore IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per un accesso successivo.

Se attualmente si ha un riferimento a un [**oggetto IPreviewHandlerFrame,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) rilasciarlo. Usare il [**puntatore IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) archiviato per chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) nel sito per un nuovo **riferimento IPreviewHandlerFrame.**

Se è attualmente disponibile una tabella dei tasti di scelta rapida, eliminarla. Chiamare [**IPreviewHandlerFrame::GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) per ottenere una nuova tabella dei tasti di scelta rapida. Archiviare questa tabella. Si noti che viene usato solo come elenco di tasti di scelta rapida supportati dal frame. I comandi nelle voci dei tasti di scelta rapida vengono ignorati.

### <a name="iobjectwithsitegetsite"></a>IObjectWithSite::GetSite

Restituisce il puntatore del sito, indipendentemente dal fatto che si tratta.

## <a name="iolewindow"></a>IOleWindow

-   [IOleWindow::ContextSensitiveHelp](#iolewindowcontextsensitivehelp)
-   [IOleWindow::GetWindow](#iolewindowgetwindow)

### <a name="iolewindowcontextsensitivehelp"></a>IOleWindow::ContextSensitiveHelp

Restituisce E \_ NOTIMPL per questo metodo.

### <a name="iolewindowgetwindow"></a>IOleWindow::GetWindow

Se la finestra del gestore di anteprima esiste attualmente, restituire **L'HWND** di tale finestra e S \_ OK. Se la finestra non esiste, restituire E \_ FAIL.

## <a name="ipreviewhandler"></a>IPreviewHandler

-   [IPreviewHandler::SetWindow](#ipreviewhandlersetwindow)
-   [IPreviewHandler::SetRect](#ipreviewhandlersetrect)
-   [IPreviewHandler::D oPreview](#ipreviewhandlerdopreview)
-   [IPreviewHandler::SetFocus](#ipreviewhandlersetfocus)
-   [IPreviewHandler::QueryFocus](#ipreviewhandlerqueryfocus)
-   [IPreviewHandler::TranslateAccelerator](#ipreviewhandlertranslateaccelerator)
-   [IPreviewHandler::Unload](#ipreviewhandlerunload)

### <a name="ipreviewhandlersetwindow"></a>IPreviewHandler::SetWindow

Impostare il *parametro hwnd* di questo metodo sull'elemento padre dell'oggetto **HWND** del gestore di anteprima. Questo metodo può essere chiamato più volte. Ridimensionare l'anteprima in modo che venga eseguito il rendering solo nell'area descritta dal *parametro prc.*

Se il visualizzatore anteprima è in fase di rendering, usare il metodo [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) per modificare l'elemento padre del visualizzatore anteprima. Modificare anche l'area in cui viene visualizzato il visualizzatore anteprima.

### <a name="ipreviewhandlersetrect"></a>IPreviewHandler::SetRect

Ridimensionare l'anteprima in modo che ne venga eseguito il rendering solo nell'area descritta da *prc di questo metodo.*

Se il visualizzatore anteprima è in fase di rendering, modificare l'area in cui viene eseguito il rendering del visualizzatore anteprima.

### <a name="ipreviewhandlerdopreview"></a>IPreviewHandler::D oPreview

Qui viene eseguito il lavoro reale. Poiché un'anteprima è dinamica, il contenuto dell'anteprima deve essere caricato solo quando è necessario. Non caricare contenuto nell'inizializzazione.

Se la finestra del gestore di anteprima non esiste, crearla. Le finestre del gestore di anteprima devono essere figli della finestra fornita da [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow). Devono essere le dimensioni fornite da **IPreviewHandler::SetWindow** e [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect) (a seconda della chiamata più recente).

Dopo aver creato una finestra, caricare i dati [**dall'interfaccia IStream**](/windows/win32/api/objidl/nn-objidl-istream) con cui è stato inizializzato il gestore di anteprima ed eseguire il rendering dei dati nella finestra del gestore di anteprima.

### <a name="ipreviewhandlersetfocus"></a>IPreviewHandler::SetFocus

Questo metodo viene chiamato quando lo stato attivo entra nel riquadro di lettura tramite un'azione di tabulazione. Poiché può essere immesso come scheda avanti o tabulazione inversa, usare lo stato corrente del tasto MAIUSC per decidere se la prima o l'ultima tabulazione nel riquadro di lettura deve ricevere lo stato attivo.

### <a name="ipreviewhandlerqueryfocus"></a>IPreviewHandler::QueryFocus

Questo metodo deve chiamare [**la funzione GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) e restituire il risultato della chiamata nel *parametro phwnd.*

### <a name="ipreviewhandlertranslateaccelerator"></a>IPreviewHandler::TranslateAccelerator

Questo metodo viene chiamato dal message pump del processo del gestore di anteprima (che prevhost.exe o un server locale personalizzato) in risposta alle sequenze di tasti dell'utente. I gestori di anteprima devono gestire queste sequenze di tasti o inoltrarle al relativo host in base all'algoritmo descritto di seguito.

Tuttavia, poiché le anteprime sono di sola lettura, l'input da tastiera deve essere minimo e in molti casi non sono necessarie ottimizzazioni come questa.

Se il tasto di scelta rapida passato a questo metodo tramite message pump è un acceleratore accettato dal gestore di anteprima, elaborarlo e restituire S \_ OK. Se il gestore non accetta tale tasto di scelta rapida, il messaggio del tasto di scelta rapida può essere inviato fino al frame da gestire.

Sono disponibili due opzioni per inoltrare di nuovo i tasti di scelta rapida al frame:

Il modello più semplice è inoltrare tutte le sequenze di tasti all'host [**usando IPreviewHandlerFrame::TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator). Questa operazione viene eseguita nell'esempio del gestore di anteprima fornito con Windows Software Development Kit (SDK). Tutti i gestori di anteprima con integrità bassa devono usare questo modello. Se l'acceleratore non viene gestito dal gestore di anteprima, chiamare **IPreviewHandlerFrame::TranslateAccelerator** e restituirne il risultato.

L'altro modello è usare una tabella dei tasti di scelta rapida come ottimizzazione per evitare di inviare troppe sequenze di tasti oltre i limiti del processo:

1.  Quando [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) viene chiamato nel gestore di anteprima, acquisire la tabella dei tasti di scelta [**rapida tramite IPreviewHandlerFrame::GetWindowContext.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) Assicurarsi di liberare l'handle per la tabella dei tasti di scelta rapida quando il visualizzatore anteprima viene eliminato.
2.  Se l'acceleratore viene gestito dal gestore di anteprima, gestirlo e restituire S \_ OK.
3.  Se l'acceleratore non viene gestito dal gestore di anteprima, confrontare il messaggio usando [**IsAccelerator**](/windows/win32/api/ole2/nf-ole2-isaccelerator) con la tabella dei tasti di scelta rapida acquisita.
4.  Se il tasto di scelta rapida corrisponde a una voce nella tabella dei tasti di scelta rapida, chiamare [**IPreviewHandlerFrame::TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator) e restituirne il risultato.
5.  Se il tasto di scelta rapida non corrisponde ad alcuna voce nella tabella dei tasti di scelta rapida, restituisce S \_ FALSE.

### <a name="ipreviewhandlerunload"></a>IPreviewHandler::Unload

Quando viene chiamato questo metodo, arrestare qualsiasi rendering, rilasciare tutte le risorse allocate leggendo i dati dal flusso e rilasciare [**l'IStream**](/windows/win32/api/objidl/nn-objidl-istream) stesso.

Una volta chiamato questo metodo, il gestore deve essere reinizializzato prima di qualsiasi tentativo di chiamare di nuovo [**IPreviewHandler::D oPreview.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview)

## <a name="ipreviewhandlervisuals"></a>IPreviewHandlerVisuals

-   [IPreviewHandlerVisuals::SetBackgroundColor](#ipreviewhandlervisualssetbackgroundcolor)
-   [IPreviewHandlerVisuals::SetFont](#ipreviewhandlervisualssetfont)
-   [IPreviewHandlerVisuals::SetTextColor](#ipreviewhandlervisualssettextcolor)

Questi metodi devono essere implementati quando si indica al gestore di anteprima di rispondere alle combinazioni di colori e caratteri dell'host. L'host esegue una query sul gestore [**per IPreviewHandlerVisuals.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals) Se viene trovato il supporto, l'host fornisce colore, tipo di carattere e colore del testo.

### <a name="ipreviewhandlervisualssetbackgroundcolor"></a>IPreviewHandlerVisuals::SetBackgroundColor

Archiviare questo colore e usarlo durante il rendering quando si vuole fornire un colore di sfondo. Ad esempio, per riempire la finestra quando il gestore esegue il rendering in un'area più piccola dell'area fornita da [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) e [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect). Si noti, tuttavia, che non è consigliabile disegnare all'esterno dell'area fornita da tali metodi.

Se questo metodo viene chiamato mentre è già in corso il rendering dell'anteprima, il rendering deve essere riavviato usando questo colore di sfondo.

### <a name="ipreviewhandlervisualssetfont"></a>IPreviewHandlerVisuals::SetFont

Archiviare queste informazioni sul tipo di carattere e usarle durante il rendering quando si vuole visualizzare testo coerente con le impostazioni correnti Windows Vista.

### <a name="ipreviewhandlervisualssettextcolor"></a>IPreviewHandlerVisuals::SetTextColor

Archiviare queste informazioni sul colore del testo e usarle durante il rendering quando si vuole visualizzare testo coerente con le impostazioni correnti Windows Vista.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestori di anteprima e host di anteprima della shell](preview-handlers.md)
</dt> <dt>

[Come registrare un gestore di anteprima](how-to-register-a-preview-handler.md)
</dt> <dt>

[Linee guida per i gestori di anteprima](preview-handler-guidelines.md)
</dt> </dl>

 

 
