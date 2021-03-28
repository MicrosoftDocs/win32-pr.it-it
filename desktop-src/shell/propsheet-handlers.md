---
description: Quando un utente fa clic con il pulsante destro del mouse su un oggetto Shell, il menu di scelta rapida visualizzato include in genere un elemento proprietà.
title: Gestori della finestra delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 72233ab5-212d-498c-8df1-1a96c8eda892
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 40ccb8d1cee0fffb993aef417b979816597cf707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882794"
---
# <a name="property-sheet-handlers"></a>Gestori della finestra delle proprietà

Quando un utente fa clic con il pulsante destro del mouse su un oggetto Shell, il menu di scelta rapida visualizzato include in genere un elemento **Proprietà** . Selezionando tale elemento viene avviata una finestra delle proprietà che consente all'utente di visualizzare e, in alcuni casi, di modificare le proprietà dell'oggetto. È possibile personalizzare questa finestra delle proprietà implementando e registrando un *gestore della finestra delle proprietà*.

Le procedure generali per l'implementazione e la registrazione di un gestore di estensione della shell sono descritte in [creazione di gestori di estensioni della shell](handlers.md). Questo documento è incentrato sugli aspetti dell'implementazione specifici dei gestori della finestra delle proprietà.

-   [Funzionamento del gestore della finestra delle proprietà](#how-property-sheet-handlers-work)
-   [Registrazione e implementazione di un gestore della finestra delle proprietà per un'unità montata](#registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive)
-   [Argomenti correlati](#related-topics)

## <a name="how-property-sheet-handlers-work"></a>Funzionamento del gestore della finestra delle proprietà

Nella figura seguente viene illustrata la finestra delle proprietà proprietà per un file di testo di Windows XP.

![finestra delle proprietà](images/propsheethandler1.jpg)

Questa illustrazione mostra la finestra delle proprietà delle proprietà predefinite visualizzata per qualsiasi file. Per molte finestre delle proprietà di questo tipo, è possibile aggiungere una o più pagine alla finestra delle proprietà implementando e registrando un gestore della finestra delle proprietà.

I gestori della finestra delle proprietà sono più comunemente registrati per un [tipo di file](fa-file-types.md). Ogni gestore può aggiungere una pagina personalizzata alla finestra delle proprietà delle proprietà per la classe. Queste pagine consentono in genere agli utenti di accedere alle proprietà specifiche del tipo di file specifico. Un tipo di file costituito da documenti di testo può, ad esempio, visualizzare una pagina in cui sono elencati il titolo e l'autore e un abstract del documento. Un caso speciale di questo tipo di gestore della finestra delle proprietà viene utilizzato per aggiungere una pagina alla finestra delle proprietà delle proprietà di un'unità montata.

L'altro uso per i gestori della finestra delle proprietà è quello di sostituire le pagine nelle finestre delle proprietà visualizzate dalle applicazioni del pannello di controllo. Un produttore del mouse, ad esempio, può utilizzare un gestore della finestra delle proprietà per sostituire la pagina dei **pulsanti** della finestra delle proprietà **del** pannello di controllo con una pagina personalizzata per le caratteristiche del mouse.

Come tutti i gestori di estensioni della shell, i gestori della finestra delle proprietà sono oggetti COM (Component Object Model in-process) implementati come dll. Devono esportare due interfacce, oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext).

L'interfaccia [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) viene utilizzata dalla Shell per inizializzare il gestore. Quando la shell chiama [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), passa un oggetto dati con il nome dell'oggetto e il puntatore a un elenco di identificatori di elemento (PIDL) della cartella che contiene il file. Il parametro *hRegKey* non viene usato con i gestori della finestra delle proprietà. Il metodo **IShellExtInit:: Initialize** deve estrarre il nome del file dall'oggetto dati e archiviare il nome e il PIDL della cartella per un uso successivo. Per ulteriori informazioni, vedere la sezione relativa all' *implementazione di IShellExtInit* in creazione di gestori di [estensioni della shell](handlers.md).

Il resto dell'operazione viene eseguita tramite l'interfaccia [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) del gestore. Se la finestra delle proprietà è associata a un tipo di file, la shell chiama [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) per consentire al gestore di aggiungere una pagina alla finestra delle proprietà. Se la finestra delle proprietà è associata a un'applicazione del pannello di controllo, la shell chiama [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) per consentire al gestore di sostituire una pagina.

## <a name="registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive"></a>Registrazione e implementazione di un gestore della finestra delle proprietà per un'unità montata

Ogni unità montata ha una finestra delle proprietà che può essere visualizzata dall'utente. Nella figura seguente viene illustrata una finestra delle proprietà delle proprietà per un'unità CD-ROM.

![finestra delle proprietà delle proprietà del CD-ROM](images/propsheethandler2.jpg)

È disponibile un'ampia gamma di dispositivi che possono essere montati come unità. Poiché la finestra delle proprietà predefinita, progettata per le unità disco, potrebbe non essere sufficiente per alcuni dispositivi, è possibile implementare un gestore della finestra delle proprietà per aggiungere una pagina specifica del dispositivo montato. L'implementazione di base di questo tipo di gestore della finestra delle proprietà è identica a quella descritta in [come registrare e implementare un gestore della finestra delle proprietà per un tipo di file](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md), con due eccezioni.

-   L'oggetto dati passato al metodo [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) del gestore può contenere il percorso dell'unità nel formato [ \_ MOUNTEDVOLUME CFSTR](clipboard.md) anziché il formato [CF \_ HDROP](clipboard.md) . Il \_ formato CF HDROP viene usato quando il dispositivo viene montato su una lettera di unità. Il \_ formato CFSTR MOUNTEDVOLUME viene usato con i file system NTFS quando il dispositivo remoto viene montato in una cartella anziché in una lettera di unità.
-   Il GUID del gestore viene registrato sotto l' **unità \_ \_ radice delle classi HKEY** \\  \\ **ShellEx** \\ chiave **PropertySheetHandlers** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come registrare e implementare un gestore della finestra delle proprietà per un tipo di file](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)
</dt> <dt>

[Come registrare e implementare un gestore della finestra delle proprietà per un'applicazione del pannello di controllo](how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application.md)
</dt> </dl>

 

 
