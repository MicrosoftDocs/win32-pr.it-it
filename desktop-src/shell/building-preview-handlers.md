---
description: In questo argomento vengono illustrate le interfacce e i metodi specifici necessari per creare un gestore di anteprime.
ms.assetid: 6c240a63-c184-4b65-9483-794f5de4d695
title: Compilazione di gestori di anteprime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a309873cf082071d5f426ce0ba6d039107c59665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342851"
---
# <a name="building-preview-handlers"></a>Compilazione di gestori di anteprime

In questo argomento vengono illustrate le interfacce e i metodi specifici necessari per creare un gestore di anteprime.

Un gestore di anteprime deve implementare le interfacce seguenti:

-   [IInitializeWithStream:: Initialize](#iinitializewithstreaminitialize) (scelta consigliata), [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)o [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [IObjectWithSite](#iobjectwithsite)
-   [IOleWindow](#iolewindow)
-   [IPreviewHandler](#ipreviewhandler)

Se il gestore di anteprime supporta le impostazioni visive fornite dall'host, ad esempio il colore di sfondo e il tipo di carattere, deve implementare anche l'interfaccia seguente:

-   [IPreviewHandlerVisuals](#ipreviewhandlervisuals)

In questo argomento si presuppone che il gestore di anteprime venga inizializzato con un flusso ed è registrato per una particolare estensione di file.

## <a name="iinitializewithstreaminitialize"></a>IInitializeWithStream:: Initialize

Archiviare i parametri [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) e Mode per poter leggere i dati dell'elemento quando si è pronti per l'anteprima dell'elemento. Non caricare i dati in [**Initialize**](/windows/desktop/api/Propsys/nf-propsys-iinitializewithstream-initialize). Caricare i dati in [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) appena prima di eseguire il rendering.

## <a name="iobjectwithsite"></a>IObjectWithSite

-   [IObjectWithSite:: SESITE](#iobjectwithsitesetsite)
-   [IObjectWithSite:: GetSite](#iobjectwithsitegetsite)

### <a name="iobjectwithsitesetsite"></a>IObjectWithSite:: SESITE

Archiviare il puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per l'accesso successivo.

Se attualmente si dispone di un riferimento a un oggetto [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) , rilasciarlo. Usare il puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) archiviato per chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul sito per un nuovo riferimento **IPreviewHandlerFrame** .

Se si dispone attualmente di una tabella dei tasti di scelta rapida, eliminarla. Chiamare [**IPreviewHandlerFrame:: GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) per ottenere una nuova tabella dei tasti di scelta rapida. Archiviare questa tabella. Si noti che viene usato solo come un elenco di tasti di scelta rapida supportati dal frame. I comandi nelle voci dell'acceleratore vengono ignorati.

### <a name="iobjectwithsitegetsite"></a>IObjectWithSite:: GetSite

Restituisce il puntatore del sito, indipendentemente dal tipo.

## <a name="iolewindow"></a>IOleWindow

-   [IOleWindow:: ContextSensitiveHelp](#iolewindowcontextsensitivehelp)
-   [IOleWindow:: GetWindow](#iolewindowgetwindow)

### <a name="iolewindowcontextsensitivehelp"></a>IOleWindow:: ContextSensitiveHelp

Restituisce E \_ NOTIMPL per questo metodo.

### <a name="iolewindowgetwindow"></a>IOleWindow:: GetWindow

Se la finestra del gestore di anteprime esiste attualmente, restituire il **HWND** di tale finestra e s \_ OK. Se la finestra non esiste, restituire E ha \_ esito negativo.

## <a name="ipreviewhandler"></a>IPreviewHandler

-   [IPreviewHandler:: finestra](#ipreviewhandlersetwindow)
-   [IPreviewHandler:: serect](#ipreviewhandlersetrect)
-   [IPreviewHandler::D oPreview](#ipreviewhandlerdopreview)
-   [IPreviewHandler:: SetFocus](#ipreviewhandlersetfocus)
-   [IPreviewHandler:: QueryFocus](#ipreviewhandlerqueryfocus)
-   [IPreviewHandler:: TranslateAccelerator](#ipreviewhandlertranslateaccelerator)
-   [IPreviewHandler:: Unload](#ipreviewhandlerunload)

### <a name="ipreviewhandlersetwindow"></a>IPreviewHandler:: finestra

Impostare il parametro *HWND* di questo metodo sull'elemento padre dell'oggetto **HWND** del gestore di anteprime. Questo metodo può essere chiamato più volte. Ridimensionare l'anteprima in modo che venga eseguito il rendering solo nell'area descritta dal parametro *PRC* .

Se è in corso il rendering del Visualizzatore anteprima, usare il metodo [**IPreviewHandler:: sefinestra**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) per modificare l'elemento padre del Visualizzatore anteprima. Modificare anche l'area in cui viene eseguito il rendering del Visualizzatore anteprima.

### <a name="ipreviewhandlersetrect"></a>IPreviewHandler:: serect

Ridimensionare l'anteprima in modo che esegua il rendering solo nell'area descritta dalla *Repubblica popolare* di questo metodo.

Se è in corso il rendering del Visualizzatore anteprima, modificare l'area in cui viene eseguito il rendering del Visualizzatore anteprime.

### <a name="ipreviewhandlerdopreview"></a>IPreviewHandler::D oPreview

Questo è il punto in cui vengono eseguite le operazioni effettive. Poiché un'anteprima è dinamica, il contenuto di anteprima deve essere caricato solo quando necessario. Non caricare contenuto nell'inizializzazione.

Se la finestra del gestore di anteprime non esiste, crearla. Le finestre del gestore di anteprime devono essere elementi figlio della finestra fornita da [**IPreviewHandler:: sewindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow). Devono essere le dimensioni fornite da **IPreviewHandler:: sewindow** e [**IPreviewHandler:: serect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect) (a seconda di quale è stato chiamato più di recente).

Quando si dispone di una finestra, caricare i dati dall'oggetto [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) con cui è stato inizializzato il gestore di anteprime ed eseguire il rendering dei dati nella finestra del gestore di anteprime.

### <a name="ipreviewhandlersetfocus"></a>IPreviewHandler:: SetFocus

Questo metodo viene chiamato quando lo stato attivo entra nel riquadro di lettura tramite un'azione di tabulazione. Poiché può essere immesso come una scheda di avanzamento o una scheda inversa, utilizzare lo stato corrente del tasto MAIUSC per decidere se il primo o l'ultimo punto di tabulazione nel riquadro di lettura deve ricevere lo stato attivo.

### <a name="ipreviewhandlerqueryfocus"></a>IPreviewHandler:: QueryFocus

Questo metodo deve chiamare la funzione [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) e restituire il risultato di tale chiamata nel parametro *phwnd* .

### <a name="ipreviewhandlertranslateaccelerator"></a>IPreviewHandler:: TranslateAccelerator

Questo metodo viene chiamato dal message pump del processo del gestore di anteprime (indipendentemente dal fatto che sia prevhost.exe o un server locale personalizzato) in risposta alle sequenze di tasti dell'utente. I gestori di anteprime devono gestire queste sequenze di tasti o inviarle all'host in base all'algoritmo descritto di seguito.

Tuttavia, poiché le anteprime sono di sola lettura, l'input da tastiera deve essere minimo e le ottimizzazioni, ad esempio, non sono necessarie in molti casi.

Se il tasto di scelta rapida passato a questo metodo tramite message pump è un tasto di scelta rapida accettato dal gestore di anteprime, elaborarlo e restituire S \_ OK. Se il gestore non accetta tale acceleratore, il messaggio Accelerator può essere restituito fino al frame da gestire.

Sono disponibili due opzioni per l'invio di tasti di scelta rapida al frame:

Il modello più semplice consiste nell'inviare tutte le sequenze di tasti all'host usando [**IPreviewHandlerFrame:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator). Questa operazione viene eseguita nell'esempio di gestore di anteprime fornito con Windows Software Development Kit (SDK). Tutti i gestori di anteprime con integrità basso devono utilizzare questo modello. Se il tasto di scelta rapida non è gestito dal gestore di anteprime, chiamare **IPreviewHandlerFrame:: TranslateAccelerator** e restituire il risultato.

L'altro modello consiste nell'usare una tabella dei tasti di scelta rapida come ottimizzazione per evitare di inviare troppe sequenze di tasti tra i limiti dei processi:

1.  Quando [**IObjectWithSite:: SESITE**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) viene chiamato sul gestore di anteprime, acquisire la tabella dei tasti di scelta rapida tramite [**IPreviewHandlerFrame:: GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext). Assicurarsi di liberare l'handle alla tabella dei tasti di scelta rapida quando il Visualizzatore anteprima viene eliminato definitivamente.
2.  Se il tasto di scelta rapida è gestito dal gestore di anteprime, gestirlo e restituire S \_ OK.
3.  Se il tasto di scelta rapida non è gestito dal gestore di anteprime, confrontarlo con l' [**acceleratore**](/windows/win32/api/ole2/nf-ole2-isaccelerator) nella tabella dei tasti di scelta rapida acquisita.
4.  Se il tasto di scelta rapida corrisponde a una voce nella tabella dell'acceleratore, chiamare [**IPreviewHandlerFrame:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator) e restituire il risultato.
5.  Se il tasto di scelta rapida non corrisponde ad alcuna voce nella tabella dei tasti di scelta rapida, restituisce \_ false.

### <a name="ipreviewhandlerunload"></a>IPreviewHandler:: Unload

Quando viene chiamato questo metodo, Interrompi qualsiasi rendering, rilascia le risorse allocate leggendo i dati dal flusso e rilascia il [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) .

Quando viene chiamato questo metodo, il gestore deve essere reinizializzato prima di qualsiasi tentativo di chiamare [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) di nuovo.

## <a name="ipreviewhandlervisuals"></a>IPreviewHandlerVisuals

-   [IPreviewHandlerVisuals::SetBackgroundColor](#ipreviewhandlervisualssetbackgroundcolor)
-   [IPreviewHandlerVisuals:: sefont](#ipreviewhandlervisualssetfont)
-   [IPreviewHandlerVisuals:: SetTextColor](#ipreviewhandlervisualssettextcolor)

Questi metodi devono essere implementati quando il gestore di anteprime viene indirizzato per rispondere agli schemi di colori e tipi di carattere dell'host. L'host esegue una query sul gestore per [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals). Se risulta supportato, l'host fornisce il colore, il tipo di carattere e il colore del testo.

### <a name="ipreviewhandlervisualssetbackgroundcolor"></a>IPreviewHandlerVisuals::SetBackgroundColor

Archiviare questo colore e usarlo durante il rendering quando si desidera fornire un colore di sfondo. Ad esempio, per riempire la finestra quando il gestore viene sottoposto a rendering in un'area più piccola dell'area fornita da [**IPreviewHandler:: sewindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) e [**IPreviewHandler:: serect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect). Si noti, tuttavia, che non è consigliabile creare un oggetto all'esterno dell'area fornita da tali metodi.

Se questo metodo viene chiamato mentre è già in corso il rendering dell'anteprima, il rendering deve essere riavviato utilizzando questo colore di sfondo.

### <a name="ipreviewhandlervisualssetfont"></a>IPreviewHandlerVisuals:: sefont

Archiviare le informazioni sul tipo di carattere e usarle durante il rendering quando si desidera visualizzare il testo coerente con le impostazioni correnti di Windows Vista.

### <a name="ipreviewhandlervisualssettextcolor"></a>IPreviewHandlerVisuals:: SetTextColor

Archiviare le informazioni sul colore del testo e utilizzarle durante il rendering quando si desidera visualizzare il testo coerente con le impostazioni correnti di Windows Vista.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestori di anteprime e host di anteprima della shell](preview-handlers.md)
</dt> <dt>

[Come registrare un gestore di anteprime](how-to-register-a-preview-handler.md)
</dt> <dt>

[Linee guida per il gestore di anteprime](preview-handler-guidelines.md)
</dt> </dl>

 

 
