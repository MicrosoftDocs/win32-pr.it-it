---
description: La raccolta di input penna inizia con il digitalizzatore.
ms.assetid: 95e49f5b-d6f0-4a5a-868b-aa0caf87c39c
title: Raccolta di input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fcd5bf0d73f48e63366843c85c9d6dd7cd388f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525308"
---
# <a name="ink-collection"></a>Raccolta di input penna

La raccolta di input penna inizia con il digitalizzatore. Un utente inserisce una penna sul digitalizzatore e inizia a scrivere. È possibile usare le funzionalità della raccolta di input penna dell'API per gestire la raccolta di dati di input penna che passano dalla penna. È possibile accedere alle informazioni sull'hardware disponibile su Tablet PC tramite la raccolta [**Tablets**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-item) e l'oggetto [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) . Si usa quindi l'oggetto [**InkCollector**](inkcollector-class.md) per ottenere i dati provenienti dal digitalizzatore.

## <a name="tablets-and-the-tablet-object"></a>Tablet e oggetto Tablet

Un [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) rappresenta un dispositivo di digitalizzazione del Tablet PC. Un Tablet PC può avere più di un digitalizzatore. Utilizzando l'oggetto **Tablet** , è possibile eseguire una query per i dispositivi digitalizzazione disponibili collegati a Tablet PC e le rispettive funzionalità hardware. Ad esempio, è possibile determinare se il **Tablet** in uso è integrato con la visualizzazione o è un dispositivo esterno separato.

## <a name="inkcollector-object"></a>Oggetto InkCollector

L'oggetto [**InkCollector**](inkcollector-class.md) acquisisce input penna da dispositivi [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) disponibili. L'oggetto **InkCollector** raccoglie solo input penna e movimenti che vengono inseriti in una finestra specifica. Un sink di evento molto efficiente esegue il rendering di questo input in tempo reale. L'oggetto **InkCollector** acquisisce l'input e lo indirizza in un oggetto [**Ink**](inkdisp-class.md) .

> [!Note]  
> La disinstallazione simultanea dell'input penna con più penne può funzionare o meno, a seconda delle funzionalità hardware del dispositivo di digitalizzazione.

 

### <a name="how-the-ink-collector-works"></a>Funzionamento dell'agente di raccolta input penna

L'oggetto [**InkCollector**](inkcollector-class.md) si connette a una finestra di applicazione nota. Consente quindi agli utenti di utilizzare qualsiasi dispositivo Tablet PC disponibile (incluso il mouse) per collocare l'input penna in tempo reale in tale finestra. I tratti di input penna raccolti vengono archiviati in un oggetto [**Ink**](inkdisp-class.md) associato. Questi tratti possono quindi essere modificati o inviati a un riconoscimento per il riconoscimento. L'oggetto **InkCollector** invia una notifica all'applicazione anche quando un cursore entra in un intervallo di tutti i dispositivi Tablet PC in uso.

Affinché l'oggetto [**InkCollector**](inkcollector-class.md) imposti accuratamente il cursore del mouse all'interno di una finestra abilitata per l'input penna, tale finestra deve essere in grado di ricevere il messaggio del **\_ cursore WM** . Questa operazione ha esito positivo per tutte le finestre normali, ma, per un controllo all'interno di una finestra di dialogo, la finestra di dialogo padre del controllo Filtra questo messaggio. Per il controllo che riceve il messaggio, impostare lo stile di **\_ notifica SS** .

## <a name="inkoverlay-object"></a>InkOverlay (oggetto)

L'oggetto [**InkCollector**](inkcollector-class.md) , descritto in precedenza, è utile per le applicazioni in modo da fornire il proprio modello per la selezione, la cancellazione e l'interazione dell'utente. L'oggetto [**InkOverlay**](inkoverlay-class.md) è un superset dell'oggetto **InkCollector** che fornisce supporto per la modifica. Questa operazione è utile per le applicazioni che integrano il disegno e la modifica di input penna nella relativa area di disegno del documento utilizzando un set di modelli di selezione di input penna standard forniti dall'oggetto.

Sia l'oggetto [**InkCollector**](inkcollector-class.md) che l'oggetto [**InkOverlay**](inkoverlay-class.md) (nonché il controllo [InkPicture](inkpicture-control.md) ) utilizzano costrutti comuni, ad esempio l'oggetto [**Ink**](inkdisp-class.md) e la raccolta [**DrawingAttributes**](inkdrawingattributes-class.md) , in modo che il modo più semplice per modificare il colore dell'input penna sia lo stesso ovunque. Questo consente di riutilizzare il codice e di avere un accesso a livello di programmazione comune, che può essere particolarmente importante se si offre supporto per gli script nell'applicazione.

[**InkOverlay**](inkoverlay-class.md) è un oggetto com utile per gli scenari di annotazione in cui gli utenti non sono interessati a eseguire il riconoscimento sull'input penna ma sono interessati alla dimensione, alla forma, al colore e alla posizione dell'input penna. È particolarmente adatto per prendere appunti e scarabocchi di base. L'interfaccia utente predefinita è un rettangolo trasparente con input penna opaco.

[**InkOverlay**](inkoverlay-class.md) estende la classe [**InkCollector**](inkcollector-class.md) in tre modi:

-   Genera eventi per le modifiche dell'attributo begin-Stroke, end-Stroke e Ink.
-   Consente agli utenti di selezionare, cancellare e ridimensionare l'input penna.
-   Supporta i comandi taglia, copia e incolla.

Uno scenario tipico in cui l'oggetto [**InkOverlay**](inkoverlay-class.md) è utile consiste nel contrassegnare una diapositiva o un'immagine di presentazione. L'oggetto **InkOverlay** consente un'implementazione semplificata delle funzionalità di input penna e layout richieste da questo scenario.

Per utilizzare [**InkOverlay**](inkoverlay-class.md), è necessario:

1.  Creare un'istanza di un oggetto [**InkOverlay**](inkoverlay-class.md) .
2.  Alleghi hWnd (handle, in codice gestito) di una finestra alla proprietà [**HWND**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_hwnd) dell'oggetto [**InkOverlay**](inkoverlay-class.md) (proprietà [handle](/previous-versions/ms582171(v=vs.100)) , nel codice gestito).
3.  Impostare la proprietà [**Enabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_enabled) dell'oggetto [**InkOverlay**](inkoverlay-class.md) su **true**.

L'oggetto [**InkOverlay**](inkoverlay-class.md) include il supporto di stampa di base, ma è necessario implementare l'anteprima di stampa o altre funzionalità di stampa avanzate.

[**InkOverlay**](inkoverlay-class.md) rende permanente l'input penna nel formato ISF (Ink Serialized Format).

> [!Note]  
> Se il [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) dell'oggetto [**InkOverlay**](inkoverlay-class.md) è impostato su **Delete** o **Select**, vengono attivati altri eventi, ad esempio [**InkAdded**](inkdisp-inkadded.md), [**InkDeleted**](inkdisp-inkdeleted.md)e [**Stroke**](inkoverlay-stroke.md). Questi eventi sono utili se si desidera implementare modalità di eliminazione o selezione personalizzate.

 

### <a name="selecting-ink"></a>Selezione dell'input penna

L'oggetto [**InkOverlay**](inkoverlay-class.md) consente agli utenti di utilizzare uno strumento lazo per selezionare gli oggetti input penna contenuti in un'area tracciata. Gli utenti possono anche selezionare l'input penna toccando qualsiasi oggetto [**input penna**](inkdisp-class.md) .

Usare la proprietà [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) per restituire una raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) che è possibile usare per modificare la selezione di un utente.

Quando si seleziona un oggetto [**Ink**](inkdisp-class.md) o un set di oggetti **Ink** , i quadratini di ridimensionamento vengono visualizzati nei quattro angoli del rettangolo di selezione dell'input penna e in tutte le ai punti medi tra gli angoli adiacenti. Se l'utente trascina in un punto qualsiasi all'interno dell'area selezionata, l'input penna diventa mobile all'interno del controllo.

### <a name="default-behavior"></a>Comportamento predefinito

Per impostazione predefinita, l'oggetto [**InkOverlay**](inkoverlay-class.md) è impostato per la raccolta di input penna. L'input penna è 53 unità di spazio input penna (dove 1 unità di spazio inchiostro = 1 HIMETRIC). L'input penna è nero se l'utente non è in esecuzione in modalità a contrasto elevato. In caso contrario, l'input penna è impostato sul valore **\_ WINDOWTEXT del colore** (**WINDOWTEXT** nel codice gestito). [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) è **false**.

### <a name="cursor-and-button-objects"></a>Oggetti Cursor e Button

Un cursore corrisponde alla punta della penna utilizzata nel Tablet PC. Ad esempio, una matita ha due estremità. In genere, viene usata un'estremità per la scrittura e l'altra per la cancellazione. Queste due estremità corrispondono a due cursori. La classe [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) non può essere confusa con [**System. Windows. Forms. Cursor**](/dotnet/api/system.windows.forms.cursor?view=netcore-3.1).

Nel Tablet PC un cursore viene in genere definito per essere usato per la scrittura o la cancellazione. È possibile che un cursore modifichi i ruoli se questa funzionalità è abilitata dall'applicazione. Alcuni dispositivi Tablet PC consentono più penne. A ogni cursore è associato un ID del cursore univoco nel sistema. Un cursore può avere zero o più pulsanti associati. Questi pulsanti vengono forniti all'applicazione come oggetti CursorButton. L'applicazione può fornire un oggetto [**DrawingAttributes**](inkdrawingattributes-class.md) specifico per qualsiasi cursore specificato.

### <a name="drawing-attributes-object"></a>Drawing (oggetto attributi)

Un oggetto [**DrawingAttributes**](inkdrawingattributes-class.md) descrive il modo in cui deve essere disegnato qualsiasi set di input penna noto. Un oggetto **DrawingAttributes** include proprietà di base, ad esempio [**colore**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color), [**larghezza**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)e [**PenTip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip). Può includere anche parametri avanzati, come la trasparenza variabile e la smussatura di Bezier, che possono fornire effetti interessanti o migliorare la leggibilità dell'input penna.

### <a name="peninputpanel-object"></a>PenInputPanel (oggetto)

> [!Note]  
> La classe [**PenInputPanel**](peninputpanel-class.md) è stata deprecata. La classe **PenInputPanel** è stata sostituita dalla classe [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) .

 

L'oggetto [**PenInputPanel**](peninputpanel-class.md) consente di aggiungere facilmente input penna sul posto alle applicazioni. **PenInputPanel** è disponibile come oggetto collegato che consente di aggiungere la funzionalità del pannello di input di Tablet PC ai controlli esistenti. L'interfaccia utente è in gran parte obbligatoria dalla lingua di input corrente. È possibile scegliere il metodo di input predefinito per l'oggetto **PenInputPanel**, ovvero la grafia o la tastiera. L'utente finale può passare da un metodo di input all'altra usando i pulsanti dell'interfaccia utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe InkCollector (C++)**](inkcollector-class.md)
</dt> <dt>

[**Classe InkOverlay (C++)**](inkoverlay-class.md)
</dt> <dt>

[**Spazio dei nomi Microsoft. Ink**](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> </dl>

 

 
