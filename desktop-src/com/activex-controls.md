---
title: Controlli ActiveX
description: Controlli ActiveX
ms.assetid: e491b66c-d6ba-4476-8413-7a9e41c05e8d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b75aabfbf2b81b4a4d3a45a1868a6eebf6fd4e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399748"
---
# <a name="activex-controls"></a>Controlli ActiveX

La tecnologia dei controlli ActiveX si basa su una base costituita da COM, oggetti collegabili, documenti composti, pagine delle proprietà, automazione OLE, persistenza degli oggetti e oggetti di tipo carattere e immagine forniti dal sistema. Come riepilogato di seguito, ognuna di queste tecnologie di base svolge un ruolo nei controlli.

<dl> <dt>

<span id="COM"></span><span id="com"></span>COM
</dt> <dd>

Un controllo è essenzialmente un oggetto COM che espone l'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , tramite la quale i client possono ottenere i puntatori alle altre interfacce. I controlli possono supportare le licenze tramite [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) e la registrazione automatica. Per ulteriori informazioni su COM, sulle licenze e sulla registrazione automatica, vedere [la Component Object Model](the-component-object-model.md) .

</dd> <dt>

<span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Oggetti collegabili
</dt> <dd>

I controlli possono supportare le interfacce in uscita tramite oggetti collegabili, in modo che il controllo possa comunicare con il client. Un'interfaccia in uscita, ad esempio, può attivare un'azione nel client, può notificare al client una modifica nel controllo o richiedere l'autorizzazione al client prima che il controllo esegua un'azione. Per ulteriori informazioni sul funzionamento degli oggetti collegabili, vedere [eventi in com e oggetti collegabili](events-in-com-and-connectable-objects.md) .

</dd> <dt>

<span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Trasferimento dati uniforme
</dt> <dd>

I controlli possono supportare il trascinamento e l'eliminazione in un contenitore con supporto dal relativo contenitore. Per ulteriori informazioni sul trascinamento della selezione, vedere [**IOleInPlaceObjectWindowless:: GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) .

</dd> <dt>

<span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Documenti composti
</dt> <dd>

Un controllo può essere un oggetto attivo sul posto che può essere incorporato in un client contenitore. Un utente finale attiva il controllo per avviare un'azione nell'applicazione contenitore. Per ulteriori informazioni sull'attivazione sul posto e altre interfacce per documenti compositi, vedere [documenti composti](compound-documents.md) .

</dd> <dt>

<span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Pagine delle proprietà
</dt> <dd>

I controlli possono fornire pagine delle proprietà in modo che gli utenti finali possano visualizzare e modificare le proprietà del controllo. Per ulteriori informazioni sul funzionamento delle pagine delle proprietà, vedere pagine delle proprietà [e finestre](property-pages-and-property-sheets.md) delle proprietà.

</dd> <dt>

<span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>Automazione OLE
</dt> <dd>

I controlli possono garantire la programmabilità tramite l'automazione OLE, in modo che i client possano sfruttare le funzionalità del controllo tramite un linguaggio di programmazione fornito dal client. Per ulteriori informazioni sull'automazione OLE, vedere la sezione automazione OLE.

</dd> <dt>

<span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Archiviazione permanente
</dt> <dd>

Un controllo può implementare una o più interfacce di persistenza per supportare la persistenza dello stato. L'implementatore del controllo deve decidere quali tipi di persistenza sono più importanti e implementare le interfacce di persistenza appropriate. Il client decide quale interfaccia si preferisce usare. Per ulteriori informazioni su tutte le interfacce di persistenza, vedere [la Component Object Model](the-component-object-model.md) .

</dd> <dt>

<span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Oggetti Font e Picture
</dt> <dd>

I controlli possono usare questi oggetti forniti dal sistema per fornire una rappresentazione visiva autonoma all'interno del client. L'oggetto Font implementa diverse interfacce, tra cui [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) e [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp). Un oggetto Font può essere creato con [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect). L'oggetto immagine implementa inoltre diverse interfacce, tra cui [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) e [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp). Un oggetto immagine può essere creato usando [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) e può essere caricato da un flusso con [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).

</dd> </dl>

È importante comprendere che queste funzionalità possono essere utilizzate in qualsiasi oggetto OLE. Non è necessario implementare un controllo per poter utilizzare queste funzionalità. Inoltre, l'unica interfaccia necessaria su un controllo è IUnknown. Il controllo supporta facoltativamente altre interfacce basate sulla necessità di supportare le funzionalità correlate.

Oltre a queste funzionalità, le interfacce e le funzioni seguenti sono specifiche della tecnologia dei controlli: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)e [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor). Anche i controlli sono specifici di un set di standard per le proprietà e i metodi che possono essere supportati da un controllo o da un contenitore di controlli.

> [!Note]  
> La libreria di sistema OleAut32.dll contiene le implementazioni delle funzioni ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)e [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)). Inoltre, OleAut32.dll contiene le implementazioni degli oggetti di tipo carattere e immagine standard, nonché una libreria dei tipi per tutte le interfacce utilizzate con i controlli, nonché le strutture di dati e i tipi di dati aggiuntivi.

 

Per altre informazioni, vedere i seguenti argomenti:

-   [Architettura di controlli ActiveX](activex-controls-architecture.md)
-   [Interfacce di controlli ActiveX](activex-controls-interfaces.md)
-   [Proprietà e metodi](properties-and-methods.md)
-   [Eventi di controllo](control-events.md)
-   [Rappresentazione visiva](visual-representation.md)
-   [Gestione della tastiera per i controlli](keyboard-handling-for-controls.md)
-   [Persistenza](persistence.md)
-   [Registrazione e licenze](registration-and-licensing.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per il controllo ActiveX e il controllo del contenitore](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 