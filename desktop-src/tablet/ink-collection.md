---
description: La raccolta di input penna inizia con il digitalizzatore.
ms.assetid: 95e49f5b-d6f0-4a5a-868b-aa0caf87c39c
title: Raccolta input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45988ea93aac5016391e22c352b9d0123a5e122f4a79c55e41e06834ed040e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452067"
---
# <a name="ink-collection"></a>Raccolta input penna

La raccolta di input penna inizia con il digitalizzatore. Un utente posiziona una penna sul digitalizzatore e inizia a scrivere. È possibile usare le funzionalità di raccolta input penna dell'API per gestire la raccolta di dati dell'input penna che "scorre" dalla penna. È possibile accedere alle informazioni sull'hardware disponibile nel Tablet PC tramite la raccolta [**Tablets**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-item) e [**l'oggetto Tablet.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) Usare quindi [**l'oggetto InkCollector**](inkcollector-class.md) per ottenere i dati provenienti dal digitalizzatore.

## <a name="tablets-and-the-tablet-object"></a>Tablet e oggetto Tablet

Un [**tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) rappresenta un dispositivo digitalizzatore di Tablet PC. Un Tablet PC può avere più di un digitalizzatore. Usando **l'oggetto Tablet,** è possibile eseguire una query per trovare i dispositivi digitalizzatori disponibili collegati al Tablet PC e le rispettive funzionalità hardware. Ad esempio, è possibile determinare se il **tablet** in uso è integrato con lo schermo o è un dispositivo esterno separato.

## <a name="inkcollector-object"></a>Oggetto InkCollector

[**L'oggetto InkCollector**](inkcollector-class.md) acquisisce l'input penna dai [**dispositivi Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) disponibili. **L'oggetto InkCollector** raccoglie solo input penna e movimenti immessi in una finestra specifica. Un sink di evento molto efficiente esegue il rendering di questo input in tempo reale. **L'oggetto InkCollector** acquisisce l'input e lo indirizza a un [**oggetto Ink.**](inkdisp-class.md)

> [!Note]  
> La disposizione simultanea dell'input penna con più penna può funzionare o meno, a seconda delle funzionalità hardware del dispositivo digitalizzatore.

 

### <a name="how-the-ink-collector-works"></a>Funzionamento dell'agente di raccolta input penna

[**L'oggetto InkCollector**](inkcollector-class.md) si collega a una finestra dell'applicazione nota. Consente quindi agli utenti di usare qualsiasi dispositivo Tablet PC disponibile (incluso il mouse) per posizionare l'input penna in tempo reale in tale finestra. I tratti input penna raccolti vengono archiviati in un oggetto [**Ink**](inkdisp-class.md) associato. Questi tratti possono quindi essere manipolati o inviati a un sistema di riconoscimento per il riconoscimento. **L'oggetto InkCollector** notifica inoltre all'applicazione quando un cursore entra nell'intervallo di uno dei dispositivi Tablet PC in uso.

Perché [**l'oggetto InkCollector**](inkcollector-class.md) possa impostare in modo accurato il cursore del mouse all'interno di una finestra abilitata per l'input penna, tale finestra deve essere in grado di ricevere il **messaggio WM \_ SETCURSOR.** Questa operazione ha esito positivo per tutte le finestre normali, ma, per un controllo all'interno di una finestra di dialogo, l'elemento padre della finestra di dialogo del controllo filtra questo messaggio. Per fare in modo che il controllo riceva il messaggio, impostare lo **stile SS \_ NOTIFY.**

## <a name="inkoverlay-object"></a>Oggetto InkOverlay

[**L'oggetto InkCollector,**](inkcollector-class.md) illustrato in precedenza, è utile per le applicazioni per fornire il proprio modello per la selezione, la cancellazione e altre interazioni dell'utente. [**L'oggetto InkOverlay**](inkoverlay-class.md) è un superset dell'oggetto **InkCollector** che fornisce il supporto per la modifica. Ciò è utile per le applicazioni per integrare il disegno e la modifica dell'input penna nel proprio canvas del documento usando un set di modelli di selezione dell'input penna standard forniti dall'oggetto .

Sia l'oggetto [**InkCollector**](inkcollector-class.md) che l'oggetto [**InkOverlay**](inkoverlay-class.md) (nonché il controllo [InkPicture)](inkpicture-control.md) usano costrutti comuni, ad esempio l'oggetto [**Ink**](inkdisp-class.md) e la raccolta [**DrawingAttributes,**](inkdrawingattributes-class.md) in modo che il modo di base per modificare il colore dell'input penna sia lo stesso ovunque. In questo modo è possibile riutilizzare il codice e avere accesso a livello di codice comune, che può essere particolarmente importante se si offre supporto per gli script nell'applicazione.

[**InkOverlay**](inkoverlay-class.md) è un oggetto COM utile per gli scenari di annotazione in cui gli utenti non sono interessati a eseguire il riconoscimento sull'input penna, ma sono invece interessati alle dimensioni, alla forma, al colore e alla posizione dell'input penna. È particolarmente adatto per prendere appunti e scarabocchi di base. L'interfaccia utente predefinita è un rettangolo trasparente con input penna opaco.

[**InkOverlay**](inkoverlay-class.md) estende la [**classe InkCollector**](inkcollector-class.md) in tre modi:

-   Genera eventi per le modifiche agli attributi begin-stroke, end-stroke e ink.
-   Consente agli utenti di selezionare, cancellare e ridimensionare l'input penna.
-   Supporta i comandi Taglia, Copia e Incolla.

Uno scenario tipico in cui [**InkOverlay**](inkoverlay-class.md) è utile è quello di contrassegnare una diapositiva o un'immagine di presentazione. **L'oggetto InkOverlay** consente una facile implementazione delle funzionalità di input penna e layout necessarie per questo scenario.

Per usare [**InkOverlay,**](inkoverlay-class.md)è necessario:

1.  Creare [**un'istanza di un oggetto InkOverlay.**](inkoverlay-class.md)
2.  Associare hWnd (handle, nel codice gestito) di una finestra alla proprietà [**hWnd**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_hwnd) dell'oggetto [**InkOverlay**](inkoverlay-class.md) [(proprietà Handle,](/previous-versions/ms582171(v=vs.100)) nel codice gestito).
3.  Impostare la proprietà Enabled [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_enabled) dell'oggetto [**InkOverlay**](inkoverlay-class.md) su **TRUE.**

[**L'oggetto InkOverlay**](inkoverlay-class.md) include il supporto di stampa di base, ma è necessario implementare l'anteprima di stampa o altre funzionalità di stampa avanzate.

[**InkOverlay**](inkoverlay-class.md) rende persistente l'input penna in formato serializzato input penna (ISF).

> [!Note]  
> Se la proprietà [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) dell'oggetto [**InkOverlay**](inkoverlay-class.md) è impostata su **Delete** o **Select,** vengono attivati altri eventi, ad esempio [**InkAdded,**](inkdisp-inkadded.md) [**InkDeleted**](inkdisp-inkdeleted.md)e [**Stroke.**](inkoverlay-stroke.md) Questi eventi sono utili se si vogliono implementare modalità di eliminazione o selezione personalizzate.

 

### <a name="selecting-ink"></a>Selezione dell'input penna

[**L'oggetto InkOverlay**](inkoverlay-class.md) consente agli utenti di usare uno strumento lazo per selezionare gli oggetti input penna contenuti in un'area tracciata. Gli utenti possono anche selezionare l'input penna toccando qualsiasi [**oggetto Ink.**](inkdisp-class.md)

Usare la [**proprietà Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) per restituire una [**raccolta Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) che è possibile usare per modificare la selezione di un utente.

Quando si seleziona un oggetto [**Ink**](inkdisp-class.md) o un set di oggetti **Ink,** i quadratini di ridimensionamento vengono visualizzati ai quattro angoli del rettangolo di selezione dell'input penna e in tutti i punti intermedi tra gli angoli adiacenti. Se l'utente trascina un punto qualsiasi all'interno dell'area selezionata, l'input penna diventa mobile all'interno del controllo.

### <a name="default-behavior"></a>Comportamento predefinito

[**L'oggetto InkOverlay**](inkoverlay-class.md) è impostato per raccogliere l'input penna per impostazione predefinita. L'input penna è largo 53 unità di spazio input penna (dove 1 unità spazio input penna = 1 HIMETRIC). L'input penna è nero se l'utente non è in esecuzione in modalità a contrasto elevato. In caso contrario, l'input penna viene impostato sul **valore COLOR \_ WINDOWTEXT** (**WindowText** nel codice gestito). [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) è **FALSE.**

### <a name="cursor-and-button-objects"></a>Oggetti Cursor e Button

Un cursore corrisponde alla punta della penna usata nel Tablet PC. Ad esempio, una matita ha due estremità. In genere, un'estremità viene usata per la scrittura e l'altra per la cancellazione. Queste due estremità corrispondono a due cursori. La [**classe Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) non viene confusa con [**System.Windows. Forms.Cursor**](/dotnet/api/system.windows.forms.cursor?view=netcore-3.1).

Nel Tablet PC un cursore viene in genere definito per essere usato per la scrittura o la cancellazione. Un cursore può cambiare potenzialmente i ruoli se l'applicazione abilita questa funzionalità. Alcuni dispositivi Tablet PC consentono più penna. A ogni cursore è associato un ID cursore univoco nel sistema. Un cursore può avere zero o più pulsanti associati. Questi pulsanti vengono forniti all'applicazione come oggetti CursorButton. L'applicazione può fornire un [**oggetto DrawingAttributes**](inkdrawingattributes-class.md) specifico per qualsiasi cursore specificato.

### <a name="drawing-attributes-object"></a>Oggetto Attributi di disegno

Un [**oggetto DrawingAttributes**](inkdrawingattributes-class.md) descrive come disegnare qualsiasi set di input penna noto. Un **oggetto DrawingAttributes** include proprietà di base, ad esempio [**Color,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color) [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)e [**PenTip.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip) Può anche includere parametri avanzati, ad esempio trasparenza variabile e smussamento di Bezier, che possono offrire effetti interessanti o migliorare la leggibilità dell'input penna.

### <a name="peninputpanel-object"></a>Oggetto PenInputPanel

> [!Note]  
> La [**classe PenInputPanel**](peninputpanel-class.md) è stata deprecata. La **classe PenInputPanel** è stata sostituita dalla [**classe TextInputPanel.**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)

 

[**L'oggetto PenInputPanel**](peninputpanel-class.md) consente di aggiungere facilmente l'input penna sul posto alle applicazioni. **PenInputPanel è** disponibile come oggetto associabile che consente di aggiungere funzionalità del Pannello input penna di Tablet PC ai controlli esistenti. L'interfaccia utente è ampiamente richiesta dalla lingua di input corrente. È possibile scegliere il metodo di input predefinito per **PenInputPanel,** la grafia o la tastiera. L'utente finale può passare da un metodo di input all'altro usando i pulsanti nell'interfaccia utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe InkCollector (C++)**](inkcollector-class.md)
</dt> <dt>

[**Classe InkOverlay (C++)**](inkoverlay-class.md)
</dt> <dt>

[**Spazio dei nomi Microsoft.Ink**](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> </dl>

 

 
