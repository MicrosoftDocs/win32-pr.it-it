---
title: Come creare procedure guidate
description: Una procedura guidata è un tipo di finestra delle proprietà che fornisce un modo semplice e potente per guidare gli utenti attraverso una procedura.
ms.assetid: f8def159-0a68-4d7f-9840-c7b6b906ed08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fedd35bd0454e0d78ddbe74d832543e58d0a8fc7
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323846"
---
# <a name="how-to-create-wizards"></a>Come creare procedure guidate

Una procedura guidata è un tipo di finestra delle proprietà che fornisce un modo semplice e potente per guidare gli utenti attraverso una procedura.

Le procedure guidate sono una delle chiavi per semplificare l'esperienza utente. Consentono di eseguire un'operazione complessa, ad esempio la configurazione di un'applicazione, e di suddividerla in una serie di semplici passaggi. In ogni punto del processo è possibile fornire una spiegazione degli elementi necessari e visualizzare i controlli che consentono all'utente di effettuare le selezioni e immettere il testo.

Una procedura guidata è effettivamente un tipo di finestra delle proprietà. Una finestra delle proprietà è essenzialmente un contenitore per una raccolta di *pagine*, in cui ogni pagina è una finestra di dialogo separata. Mentre le finestre delle proprietà normali consentono all'utente di accedere a qualsiasi pagina in qualsiasi momento, le procedure guidate presentano le pagine in sequenza. Anziché le schede, i pulsanti vengono usati per spostarsi avanti e indietro. L'ordine in cui vengono visualizzate le pagine è controllato dall'applicazione e può essere modificato in base all'input dell'utente.

Sono disponibili due stili principali della procedura guidata: lo stile Wizard97 precedente e lo stile Aero introdotto in Windows Vista. Per le illustrazioni, vedere [informazioni sulle finestre delle proprietà](property-sheets.md). (Un terzo stile, usando solo PSH \_ La procedura guidata \_ o \_ il flag PSH Wizard Lite presenta una semplice sequenza di finestre delle proprietà senza intestazioni o filigrane.

> [!Note]  
> Una "filigrana" nel contesto delle procedure guidate è una bitmap visualizzata nel margine sinistro di alcune pagine.

 

Nella maggior parte di questo documento si presuppone che si stia implementando una procedura guidata per un sistema con la [versione 5,80](common-control-versions.md) o successive dei controlli comuni. Se si tenta di utilizzare lo stile Wizard97 con le versioni precedenti dei controlli comuni, è possibile che l'applicazione venga compilata, ma non viene visualizzata correttamente. Per informazioni su come creare una procedura guidata compatibile con Wizard97 nei sistemi precedenti, vedere la pagina relativa alle procedure guidate compatibili con le versioni precedenti più avanti in questo argomento.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="wizard-implementation"></a>Implementazione della procedura guidata

L'implementazione di una procedura guidata è simile all'implementazione di una normale finestra delle proprietà. Al livello più elementare, è importante impostare uno dei flag o combinazioni di flag seguenti nella struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) che definisce la finestra delle proprietà.



| Contrassegno                           | Stile                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_procedura guidata PSH                    | Procedura guidata semplice senza intestazioni o bitmap.                                                                                                           |
| \_procedura guidata PSH \_ Lite              | Analogamente alla \_ procedura guidata PSH, con alcune differenze minime nell'aspetto. ad esempio, il divisore sopra i pulsanti è impostato sulla larghezza intera della finestra. |
| \_WIZARD97 PSH                  | Procedura guidata Wizard97 con intestazioni (facoltative), bitmap di intestazione e filigrane.                                                                            |
| PSH \_ Wizard \| PSH \_ AEROWIZARD | Procedura guidata Aero. Le creazioni guidate Aero non utilizzano filigrane o bitmap di intestazione. Richiedono il modello di Apartment a thread singolo (STA).                         |



 

La procedura di base per l'implementazione di una procedura guidata è la seguente:

1.  Creare un modello di finestra di dialogo per ogni pagina.
2.  Definire le pagine creando una struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) per ogni pagina. Questa struttura definisce la pagina e contiene i puntatori al modello della finestra di dialogo ed eventuali bitmap o altre risorse.
3.  Passare la struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) creata nel passaggio precedente alla funzione [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) per creare l'handle HPROPSHEETPAGE della pagina.
4.  Definire la procedura guidata creando una struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) .
5.  Passare la struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) alla funzione [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) per visualizzare la procedura guidata.
6.  Implementare le procedure della finestra di dialogo per ogni pagina per gestire i messaggi di notifica dai controlli della pagina e i pulsanti della procedura guidata e per elaborare altri messaggi di Windows.

### <a name="create-the-dialog-box-templates"></a>Creare i modelli della finestra di dialogo

Sono disponibili due tipi di base della pagina della procedura guidata: esterno e interno. Le pagine esterne sono le pagine introduttive (introduttive) e di completamento. Tutti gli altri sono pagine interne.

**Modelli di finestra di dialogo della pagina esterna**

Il layout di base delle pagine introduttive e di completamento è identico. Nella figura seguente è illustrata una pagina introduttiva di esempio Wizard97 con una filigrana segnaposto.

![screenshot che mostra una pagina della procedura guidata con un grafico a sinistra, un titolo e un testo del corpo a destra e pulsanti indietro, avanti e Annulla nella parte inferiore](images/wiz97exterior.png)

Per le pagine esterne di Wizard97, il modello della finestra di dialogo è unità di dialogo 317x193. Riempie tutta la procedura guidata, eccetto la didascalia e la banda nella parte inferiore che contiene i pulsanti **indietro**, **Avanti** e **Annulla** . Il lato sinistro del modello, riservato per una bitmap "watermark", non deve contenere alcun controllo. La filigrana viene specificata nella struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) della procedura guidata e viene aggiunta automaticamente alla pagina. Quando si progetta il modello di risorsa, è necessario consentirne lo spazio.

Quando si crea la bitmap della filigrana, tenere presente che la dimensione della finestra di dialogo può aumentare se, ad esempio, l'utente sceglie un tipo di carattere di sistema di grandi dimensioni. Lingue diverse tendono anche a avere metriche dei tipi di carattere differenti. Quando la pagina cresce, l'area riservata per la filigrana è proporzionalmente più grande. Tuttavia, non è possibile modificare la bitmap della filigrana né la bitmap estesa per riempire l'area più grande. La bitmap viene invece lasciata nelle dimensioni originali nella parte superiore sinistra dell'area riservata. La parte dell'area riservata più grande che non è coperta dalla filigrana viene riempita automaticamente con il colore del pixel in alto a sinistra della bitmap.

Se è necessario disporre di bitmap di filigrana di dimensioni diverse per le diverse metriche dei tipi di carattere, sono disponibili due soluzioni:

-   Ottenere la metrica del tipo di carattere prima di creare la procedura guidata e specificare una bitmap di filigrana opportunamente dimensionata.
-   Non specificare una bitmap della filigrana quando si crea la procedura guidata. Wizard97 lascerà vuota l'area della filigrana. Quindi, creare una bitmap di dimensioni appropriate nell'area riservata per la filigrana.

È possibile posizionare i controlli nell'area a destra della filigrana come per una normale finestra di dialogo. Il colore di sfondo di quest'area è determinato dal sistema e non richiede alcuna azione da parte dell'utente. In questa area vengono in genere inseriti due controlli statici. Il valore superiore include il titolo e usa un carattere grassetto di grandi dimensioni (Verdana in grassetto a 12 punti per Wizard97). L'altro, che è per il testo esplicativo, usa il tipo di carattere standard della finestra di dialogo.

La differenza principale tra le pagine introduttive e di completamento è costituita dai pulsanti della procedura guidata e dal testo nei controlli statici. Le pagine introduttive dispongono in genere di un pulsante **Avanti** e **indietro** , in cui è abilitato solo il pulsante **Avanti** . Nelle pagine di completamento è abilitato il pulsante **indietro** e il pulsante **Avanti** viene sostituito da un pulsante **fine** .

> [!Note]  
> Nelle procedure guidate Aero il pulsante **indietro** viene sostituito da un pulsante freccia sulla barra del titolo.

 

È possibile modificare il testo nel pulsante **fine** inviando la procedura guidata un messaggio [**PSM \_ SETFINISHTEXT**](psm-setfinishtext.md) . Per impostazione predefinita, il pulsante **fine** non include un tasto di scelta rapida. Per definire un tasto di scelta rapida, includere una e commerciale nella stringa di testo passata a PSM \_ SETFINISHTEXT. Ad esempio, "&Finish" definisce "F" come tasto di scelta rapida.

**Modelli di finestra di dialogo della pagina interna**

Le pagine interne hanno un aspetto leggermente diverso rispetto alle pagine esterne. Nella figura seguente è illustrata una pagina interna di esempio di Wizard97 con una bitmap dell'intestazione segnaposto.

![Screenshot di una pagina della procedura guidata con testo titolo e sottotitolo e un elemento grafico nella parte superiore, testo al centro e pulsanti in basso](images/wiz97interior.png)

L'area di intestazione nella parte superiore della pagina viene gestita dalla finestra delle proprietà, quindi non è inclusa nel modello. Il contenuto dell'intestazione viene specificato nella struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) della pagina e nella struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) della procedura guidata. Poiché la pagina interna deve rientrare tra l'intestazione e i pulsanti, il modello della finestra di dialogo Wizard97 è unità di dialogo 317x143, leggermente più piccolo del modello per le pagine esterne.

Nella figura seguente è illustrata una procedura guidata Aero creata con lo stesso modello.

![Screenshot diverso da quello precedente con un'area del titolo nella parte superiore e solo i pulsanti avanti e Annulla nella parte inferiore](images/wizardaerointerior.png)

### <a name="define-the-wizard-pages"></a>Definire le pagine della procedura guidata

Dopo aver creato i modelli della finestra di dialogo e le risorse correlate, ad esempio le bitmap e le tabelle di stringhe, è possibile creare le pagine della finestra delle proprietà. La procedura è simile a quella per le finestre delle proprietà standard. Per prima cosa, compilare i membri appropriati di una struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) . Alcuni membri sono specifici delle procedure guidate. Chiamare quindi la funzione [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) per creare l'handle HPROPSHEETPAGE della pagina.

I flag seguenti relativi alla procedura guidata possono essere impostati nel membro **dwFlags** della struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) .



| Flag                   | Descrizione                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| \_HIDEHEADER PSP        | Impostare questo flag per le pagine esterne in Wizard97. L'intestazione non viene visualizzata e può essere visualizzata una filigrana.                                |
| \_USEHEADERTITLE PSP    | Impostare questo flag per le pagine interne per inserire un titolo nell'area di intestazione in Wizard97 o nella parte superiore dell'area client in una procedura guidata Aero. |
| \_USEHEADERSUBTITLE PSP | Impostare questo flag per le pagine interne per inserire un sottotitolo nell'area di intestazione di Wizard97.                                                  |



 

Se è stato impostato PSP \_ USEHEADERTITLE o PSP \_ USEHEADERSUBTITLE, assegnare il testo titolo e sottotitolo ai membri **pszHeaderTitle** e **pszHeaderSubtitle** , rispettivamente. Quando si assegnano stringhe di testo ai membri delle strutture [**PROPSHEETPAGE**](pss-propsheetpage.md) e [**PROPSHEETHEADER**](pss-propsheetheader.md) , è possibile assegnare un puntatore di stringa o usare la macro **MAKEINTRESOURCE** per assegnare un valore da una risorsa di tipo stringa. La risorsa di stringa viene caricata dal modulo specificato nel membro **HINSTANCE** della struttura **PROPSHEETHEADER** della procedura guidata.

Quando si chiama [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) per creare una pagina, assegnare il risultato a un elemento di una matrice di handle HPROPSHEETPAGE. Questa matrice viene utilizzata durante la creazione della finestra delle proprietà. L'indice della matrice di un handle di pagina determina l'ordine predefinito in cui viene visualizzato. Dopo aver creato un handle HPROPSHEETPAGE della pagina, è possibile riutilizzare la stessa struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) per creare la pagina successiva assegnando nuovi valori ai membri pertinenti.

Un modo alternativo per creare pagine consiste nell'usare strutture [**PROPSHEETPAGE**](pss-propsheetpage.md) separate per ogni pagina e creare una matrice di strutture. Questa matrice viene usata al posto di una matrice di handle HPROPSHEETPAGE durante la creazione della finestra delle proprietà. L'uso di strutture **PROPSHEETPAGE** separate Elimina la necessità di chiamare [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) ma usa una maggiore quantità di memoria. In caso contrario, non esiste alcuna differenza significativa tra i due approcci.

Nell'esempio seguente viene definita una pagina Wizard97 interna assegnando valori a una struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) . In questo esempio il titolo, il sottotitolo e il modello della finestra di dialogo della pagina sono tutti identificati dai relativi ID di risorsa. Viene quindi chiamata la funzione [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) per creare l'handle HPROPSHEETPAGE della pagina. Poiché verrà visualizzata la seconda pagina, l'handle viene assegnato alla matrice di Handles, *ahpsp*, con indice 1.


```C++
// g_hInstance is the global HINSTANCE of the application.
// IntPage1DlgProc is the dialog procedure for this page.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETPAGE psp = { sizeof(psp) };

psp.hInstance         = g_hInstance;
psp.dwFlags           = PSP_USEHEADERTITLE | PSP_USEHEADERSUBTITLE;
psp.lParam            = (LPARAM) &wizdata;
psp.pszHeaderTitle    = MAKEINTRESOURCE(IDS_TITLE1);
psp.pszHeaderSubTitle = MAKEINTRESOURCE(IDS_SUBTITLE1);
psp.pszTemplate       = MAKEINTRESOURCE(IDD_INTERIOR1);
psp.pfnDlgProc        = IntPage1DlgProc;

ahpsp[1] = CreatePropertySheetPage(&psp);
```



### <a name="custom-page-data"></a>Dati della pagina personalizzati

Quando si crea una pagina, è possibile assegnarvi dati personalizzati usando il membro **lParam** della struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) , in genere assegnando un puntatore a una struttura definita dall'utente.

Quando la pagina viene selezionata per la prima volta, la relativa routine della finestra di dialogo riceve un messaggio [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . Il valore *lParam* del messaggio punta a una copia della struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) della pagina, da cui è possibile recuperare i dati personalizzati. È quindi possibile archiviare questi dati per l'uso nei messaggi successivi usando [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) con GWL \_ UserData come parametro di indice. Più pagine possono avere un puntatore per gli stessi dati e qualsiasi modifica apportata ai dati da una pagina è disponibile per le altre pagine nelle relative procedure di dialogo.

### <a name="define-the-wizard-property-sheet"></a>Definire la finestra delle proprietà della procedura guidata

Come per le finestre delle proprietà ordinarie, si definisce la finestra delle proprietà della procedura guidata compilando i membri di una struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) . Questa struttura consente di specificare le pagine che costituiscono la procedura guidata e l'ordine predefinito in cui vengono visualizzate, insieme a diversi parametri correlati. Viene quindi avviata la procedura guidata chiamando la funzione [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) .

Nello stile Wizard97, il membro **pszCaption** della struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) viene ignorato. Al contrario, nella procedura guidata viene visualizzata la didascalia specificata nel modello della finestra di dialogo della pagina corrente. Se il modello non dispone di una didascalia, viene visualizzata la didascalia della pagina precedente. Quindi, per visualizzare la stessa didascalia in tutte le pagine, specificare la didascalia nel modello per la pagina introduttiva.

Nello stile della procedura guidata Aero la didascalia della finestra di dialogo viene ricavata da **pszCaption**.

Se è stata creata una matrice di handle HPROPSHEETPAGE per le pagine, assegnare la matrice al membro **phpage** . Se invece è stata creata una matrice di strutture [**PROPSHEETPAGE**](pss-propsheetpage.md) , assegnare la matrice al membro **ppSP** e impostare il flag PSH \_ PROPSHEETPAGE nel membro **dwFlags** .

Nell'esempio seguente vengono assegnati valori a *PSH*, una struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) e viene chiamata la funzione [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) per avviare la procedura guidata. La procedura guidata di tipo Wizard97 ha sia la filigrana che la grafica dell'intestazione, specificata dai rispettivi ID di risorsa. La matrice *ahpsp* contiene tutti gli handle HPROPSHEETPAGE e definisce l'ordine predefinito in cui vengono visualizzati.


```C++
// g_hInstance is the global HINSTANCE of the application.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETHEADER psh = { sizeof(psh) };

psh.hInstance      = g_hInstance;
psh.hwndParent     = NULL;
psh.phpage         = ahpsp;
psh.dwFlags        = PSH_WIZARD97 | PSH_WATERMARK | PSH_HEADER;
psh.pszbmWatermark = MAKEINTRESOURCE(IDB_WATERMARK);
psh.pszbmHeader    = MAKEINTRESOURCE(IDB_BANNER);
psh.nStartPage     = 0;
psh.nPages         = 4;

PropertySheet(&psh);
```



### <a name="the-dialog-box-procedure"></a>Routine della finestra di dialogo

Per ogni pagina della procedura guidata è necessaria una routine della finestra di dialogo per elaborare i messaggi di Windows, in particolare le notifiche dei controlli e della procedura guidata. I tre messaggi che quasi tutte le procedure guidate devono essere in grado di gestire sono [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog), [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy)e [**WM \_ Notify**](wm-notify.md).

Il messaggio di [**\_ notifica WM**](wm-notify.md) viene ricevuto prima che la pagina venga visualizzata e quando si fa clic su uno dei pulsanti della procedura guidata. Il parametro *lParam* del messaggio è un puntatore a una struttura di intestazione [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) . L'ID della notifica è contenuto nel membro del **codice** della struttura. Di seguito sono riportate le quattro notifiche che devono essere gestite dalla maggior parte delle procedure guidate.



| Codice                                | Descrizione                                 |
|-------------------------------------|---------------------------------------------|
| [seactive PSN \_](psn-setactive.md) | Inviato prima della visualizzazione della pagina.          |
| [\_WIZBACK PSN](psn-wizback.md)     | Inviato quando si fa clic sul pulsante **indietro** .   |
| [\_WIZNEXT PSN](psn-wiznext.md)     | Inviato quando si fa clic sul pulsante **Avanti** .   |
| [\_WIZFINISH PSN](psn-wizfinish.md) | Inviato quando si fa clic sul pulsante **fine** . |



 

### <a name="handle-wm_initdialog-and-wm_destroy"></a>Gestisci WM \_ INITDIALOG e WM \_ Destroy

Quando una pagina sta per essere visualizzata per la prima volta, la relativa routine della finestra di dialogo riceve un messaggio [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . Gestione di questo messaggio consente alla procedura guidata di eseguire le attività di inizializzazione necessarie, ad esempio l'archiviazione di dati personalizzati o l'impostazione di tipi di carattere.

Quando la finestra delle proprietà viene distrutta, viene visualizzato un messaggio [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) . La procedura guidata viene automaticamente eliminata dal sistema, ma la gestione di questo messaggio consente di eseguire tutte le operazioni di pulizia necessarie.

### <a name="handle-psn_setactive"></a>Gestire PSN in modo \_ SEattivo

Il codice di notifica [ \_ seattivo PSN](psn-setactive.md) viene inviato ogni volta che una pagina sta per essere resa visibile. La prima volta che viene visitata una pagina, PSN \_ seactive segue il messaggio [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . Se la pagina viene successivamente rivisitata, riceve solo una \_ notifica SEATTIVA PSN. Questa notifica viene in genere gestita per inizializzare i dati della pagina e abilitare i pulsanti appropriati.

Per impostazione predefinita, la procedura guidata Visualizza i pulsanti **indietro**, **Avanti** e **Annulla** con tutti i pulsanti abilitati. Per disabilitare un pulsante o la visualizzazione **fine** anziché **successiva**, è necessario inviare un messaggio [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md) . Una volta inviato questo messaggio, lo stato dei pulsanti viene mantenuto finché non viene modificato da un altro messaggio **PSM \_ SETWIZBUTTONS** , anche se è stata selezionata una nuova pagina. In genere, tutti i gestori di [PSN \_ seactive](psn-setactive.md) inviano questo messaggio per assicurarsi che ogni pagina abbia lo stato del pulsante corretto.

È possibile modificare lo stato del pulsante con questo messaggio in qualsiasi momento. Ad esempio, potrebbe essere necessario disabilitare inizialmente il pulsante **Avanti** . Dopo che un utente ha immesso tutte le informazioni necessarie, è possibile inviare un altro messaggio di [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md) per abilitare il pulsante **Avanti** e consentire all'utente di passare alla pagina successiva.

Il frammento di codice seguente usa la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) per abilitare i pulsanti **indietro** e **Avanti** in una pagina interna prima che venga visualizzata.


```C++
case WM_NOTIFY :
    {
        LPNMHDR pnmh = (LPNMHDR)lParam;
        
        switch(pnmh->code)
        {
        
        ...
        
        case PSN_SETACTIVE :
        
            ...
            
            // This is an interior page.
            PropSheet_SetWizButtons(hwnd, PSWIZB_NEXT | PSWIZB_BACK);
            
            ...
        }
    ...
    
    }
```



### <a name="handle-psn_wiznext-psnwizback-and-psn_wizfinish"></a>Gestire PSN \_ WIZNEXT, PSNWIZBACK e PSN \_ WIZFINISH

Quando si fa clic su un pulsante **Avanti** o **indietro** , si riceve un codice di notifica [PSN \_ WIZNEXT](psn-wiznext.md) o [PSN \_ WIZBACK](psn-wizback.md) . Per impostazione predefinita, la procedura guidata passa automaticamente alla pagina precedente o successiva nell'ordine definito al momento della creazione della finestra delle proprietà. Un motivo comune per gestire queste notifiche è impedire all'utente di cambiare le pagine o di eseguire l'override dell'ordine predefinito della pagina.

Per impedire all'utente di passare da una pagina all'altra, gestire la notifica dei pulsanti, chiamare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il \_ valore di MSGRESULT DWL impostato su-1 e restituire **true**. Ad esempio:


```C++
case PSN_WIZNEXT :

        ...
        
        // Do not go to the next page yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, -1);
        
        return TRUE;
        
        ...
```



Per eseguire l'override dell'ordine standard e passare a una pagina specifica, chiamare [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il \_ valore DWL MSGRESULT impostato sull'ID di risorsa della finestra di dialogo della pagina e restituire **true**. Ad esempio:


```C++
case PSN_WIZNEXT :

        ...
        
        // Go straight to the completion page.
        SetWindowLong(hwnd, DWL_MSGRESULT, IDD_FINISH);
        
        return TRUE;
        
        ...
```



Quando si fa clic sul pulsante **fine** o **Annulla** , viene visualizzato rispettivamente un codice di notifica di [ \_ reimpostazione](psn-reset.md) PSN [ \_ WIZFINISH](psn-wizfinish.md) o PSN. Quando si fa clic su uno di questi pulsanti, la procedura guidata viene automaticamente eliminata dal sistema. Tuttavia, è possibile gestire queste notifiche se è necessario eseguire attività di pulizia prima che la procedura guidata venga distrutta. Per evitare che la procedura guidata venga distrutta quando si riceve una \_ notifica di WIZFINISH PSN, chiamare [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il \_ valore DWL MSGRESULT impostato su **true** e restituire **true**. Ad esempio:


```C++
case PSN_WIZFINISH :

        ...
        
        // Not finished yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, TRUE);
        
        return TRUE;
        
        ...
```



### <a name="backward-compatible-wizards"></a>Procedure guidate compatibili con le versioni precedenti

Nella sezione precedente si presuppone che si stia implementando una procedura guidata per un sistema con la [versione 5](common-control-versions.md) o successiva dei controlli comuni.

Se si sta scrivendo una procedura guidata per i sistemi con versioni precedenti dei controlli comuni, molte delle funzionalità descritte nella sezione precedente non saranno disponibili. Molti dei membri delle strutture [**PROPSHEETHEADER**](pss-propsheetheader.md) e [**PROPSHEETPAGE**](pss-propsheetpage.md) usati dallo stile Wizard97 sono supportati solo dai controlli comuni versione 5 e successive. Tuttavia, è comunque possibile implementare una procedura guidata *compatibile con le versioni precedenti* con un aspetto simile a quello dello stile Wizard97. A tale scopo, è necessario implementare in modo esplicito quanto segue:

-   Aggiungere l'immagine della filigrana al modello della finestra di dialogo per le pagine introduttive e di completamento.
-   Rendere le stesse dimensioni di tutti i modelli. Non esiste un'area di intestazione definita dal sistema separata per le pagine interne.
-   Creare l'area di intestazione della pagina interna in modo esplicito sui modelli.
-   Non usare una rappresentazione grafica dell'intestazione perché potrebbe essere in conflitto con il titolo o il sottotitolo se la procedura guidata cambia dimensione.

Per ulteriori informazioni sulle procedure guidate compatibili con le versioni precedenti, vedere la [procedura guidata compatibile con](/previous-versions//ms737910(v=vs.85))le versioni precedenti 97.

## <a name="remarks"></a>Commenti

Per una descrizione completa dei problemi di progettazione per Wizard97, vedere la [specifica Wizard97](/previous-versions//ms738248(v=vs.85)), in altre parti del Windows SDK. Questo documento contiene linee guida per elementi quali le dimensioni delle finestre di dialogo, le dimensioni e i colori bitmap e il posizionamento dei controlli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo delle finestre delle proprietà](using-property-sheets.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 