---
description: Quando un utente fa clic con il pulsante destro del mouse su un oggetto Shell, il menu di scelta rapida visualizzato in genere include un elemento Proprietà.
title: Gestori della finestra delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 72233ab5-212d-498c-8df1-1a96c8eda892
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 27327db4718430ba646d9566227116e304d4d5f5770d0119987b32e0cd2adce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719543"
---
# <a name="property-sheet-handlers"></a>Gestori della finestra delle proprietà

Quando un utente fa clic con il pulsante destro del mouse su un oggetto Shell, il menu di scelta rapida visualizzato in genere include un **elemento** Proprietà. Selezionando tale elemento viene avviata una finestra delle proprietà che consente all'utente di visualizzare e, in alcuni casi, modificare le proprietà dell'oggetto. È possibile personalizzare questa finestra delle proprietà implementando e registrando un gestore *della finestra delle proprietà.*

Le procedure generali per l'implementazione e la registrazione di un gestore di estensioni shell sono descritte in [Creazione di gestori di estensioni della shell](handlers.md). Questo documento è in particolare sugli aspetti dell'implementazione specifici dei gestori della finestra delle proprietà.

-   [Funzionamento dei gestori della finestra delle proprietà](#how-property-sheet-handlers-work)
-   [Registrazione e implementazione di un gestore della finestra delle proprietà per un'unità montata](#registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive)
-   [Argomenti correlati](#related-topics)

## <a name="how-property-sheet-handlers-work"></a>Funzionamento dei gestori della finestra delle proprietà

La figura seguente mostra la finestra delle proprietà Proprietà per un Windows di testo XP.

![finestra delle proprietà](images/propsheethandler1.jpg)

Questa figura mostra la finestra delle proprietà Proprietà predefinita visualizzata per qualsiasi file. Per molte finestre delle proprietà di questo tipo, è possibile aggiungere una o più pagine alla finestra delle proprietà implementando e registrando un gestore della finestra delle proprietà.

I gestori della finestra delle proprietà sono in genere registrati per un [tipo di file](fa-file-types.md). Ogni gestore può aggiungere una pagina personalizzata alla finestra delle proprietà Proprietà per la classe . Queste pagine consentono in genere agli utenti di accedere a proprietà specifiche del tipo di file specifico. Un tipo di file costituito da documenti di testo può, ad esempio, visualizzare una pagina in cui sono elencati il titolo e l'autore e un astratto del documento. Un caso speciale di questo tipo di gestore della finestra delle proprietà viene usato per aggiungere una pagina alla finestra delle proprietà Proprietà per un'unità montata.

L'altro uso per i gestori delle finestre delle proprietà è sostituire le pagine nelle finestre delle proprietà visualizzate dalle Pannello di controllo applicazioni. Un produttore del mouse, ad esempio, può  usare un gestore della finestra delle proprietà per sostituire la pagina Pulsanti nella finestra delle proprietà Proprietà **mouse** di Pannello di controllo con una pagina personalizzata per le caratteristiche del mouse.

Come tutti i gestori dell'estensione Shell, i gestori della finestra delle proprietà sono oggetti com (COM) Component Object Model in-process implementati come DLL. Devono esportare due interfacce oltre a [**IUnknown:**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext).

[**L'interfaccia IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) viene usata dalla shell per inizializzare il gestore. Quando shell chiama [**IShellExtInit::Initialize,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)passa un oggetto dati con il nome dell'oggetto e il puntatore a un elenco di identificatori di elemento (PIDL) della cartella che contiene il file. Il *parametro hRegKey* non viene usato con i gestori della finestra delle proprietà. Il **metodo IShellExtInit::Initialize** deve estrarre il nome file dall'oggetto dati e archiviare il nome e il FILE PIDL della cartella per un uso successivo. Per altri dettagli, vedere la *sezione Implementazione di IShellExtInit* di [Creazione di gestori di estensioni della shell](handlers.md).

Il resto dell'operazione viene eseguita tramite [**l'interfaccia IShellPropSheetExt del**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) gestore. Se la finestra delle proprietà è associata a un tipo di file, Shell chiama [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) per consentire al gestore di aggiungere una pagina alla finestra delle proprietà. Se la finestra delle proprietà è associata a un'applicazione Pannello di controllo, Shell chiama [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) per consentire al gestore di sostituire una pagina.

## <a name="registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive"></a>Registrazione e implementazione di un gestore della finestra delle proprietà per un'unità montata

Ogni unità montata ha una finestra Proprietà che può essere visualizzata dall'utente. La figura seguente mostra una finestra delle proprietà Proprietà per un'unità CD-ROM.

![Finestra delle proprietà cd-rom](images/propsheethandler2.jpg)

È disponibile un'ampia gamma di dispositivi che possono essere montati come unità. Poiché la finestra delle proprietà predefinita, progettata per le unità disco, potrebbe non essere sufficiente per alcuni dispositivi, è possibile implementato un gestore della finestra delle proprietà per aggiungere una pagina specifica per il dispositivo montato. L'implementazione di base di questo tipo di gestore della finestra delle proprietà è identica a quella descritta in Come registrare e implementare un gestore della finestra delle proprietà per un tipo [di file](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md), con due eccezioni.

-   L'oggetto dati passato al metodo [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) del gestore può contenere il percorso dell'unità nel formato [CFSTR \_ MOUNTEDVOLUME](clipboard.md) anziché nel formato [CF \_ HDROP.](clipboard.md) Il formato \_ CF HDROP viene usato quando il dispositivo viene montato in una lettera di unità. Il formato CFSTR MOUNTEDVOLUME viene usato con i file system NTFS quando il dispositivo remoto viene montato in una cartella \_ anziché in una lettera di unità.
-   Il GUID del gestore viene registrato nella shell **HKEY \_ CLASSES \_ ROOT** \\  \\ **Driveex** \\ **PropertySheetHandlers.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come registrare e implementare un gestore della finestra delle proprietà per un tipo di file](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)
</dt> <dt>

[Come registrare e implementare un gestore della finestra delle proprietà per un'Pannello di controllo applicazione](how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application.md)
</dt> </dl>

 

 
