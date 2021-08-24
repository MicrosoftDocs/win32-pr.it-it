---
title: Come creare procedure guidate
description: Una procedura guidata è un tipo di finestra delle proprietà che offre un modo semplice e potente per guidare gli utenti attraverso una procedura.
ms.assetid: f8def159-0a68-4d7f-9840-c7b6b906ed08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4254b448c719e3e1397fceadfcdc28475eaeae588f6f1eb0f0168cea07327d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655836"
---
# <a name="how-to-create-wizards"></a>Come creare procedure guidate

Una procedura guidata è un tipo di finestra delle proprietà che offre un modo semplice e potente per guidare gli utenti attraverso una procedura.

Le procedure guidate sono una delle chiavi per semplificare l'esperienza utente. Consentono di eseguire un'operazione complessa, ad esempio la configurazione di un'applicazione, e di suddividerla in una serie di semplici passaggi. In ogni punto del processo è possibile fornire una spiegazione degli elementi necessari e visualizzare i controlli che consentono all'utente di effettuare selezioni e immettere testo.

Una procedura guidata è in realtà un tipo di finestra delle proprietà. Una finestra delle proprietà è essenzialmente un contenitore per una raccolta di *pagine*, in cui ogni pagina è una finestra di dialogo separata. Mentre le normali finestre delle proprietà consentono all'utente di accedere a qualsiasi pagina in qualsiasi momento, le procedure guidate presentano le pagine in sequenza. Invece delle schede, i pulsanti vengono usati per spostarsi avanti e indietro. L'ordine di visualizzazione delle pagine è controllato dall'applicazione e può essere modificato in base all'input dell'utente.

Sono disponibili due stili principali della procedura guidata: lo stile Wizard97 precedente e lo stile Aero introdotto in Windows Vista. Per illustrazioni, vedere [Informazioni sulle finestre delle proprietà.](property-sheets.md) (Un terzo stile, usando solo il PSH \_ WIZARD o PSH WIZARD LITE flag, presenta una semplice sequenza di finestre delle \_ proprietà senza intestazioni o \_ filigrane.

> [!Note]  
> Una "filigrana" nel contesto delle procedure guidate è una bitmap visualizzata nel margine sinistro di alcune pagine.

 

La discussione nella maggior parte di questo documento presuppone che si sta implementando una procedura guidata per un sistema con la [versione 5.80](common-control-versions.md) o successiva dei controlli comuni. Se si tenta di usare lo stile Wizard97 con le versioni precedenti dei controlli comuni, l'applicazione può essere compilata ma non verrà visualizzata correttamente. Per informazioni su come creare una procedura guidata compatibile con Wizard97 nei sistemi precedenti, vedere Procedure guidate compatibili con le versioni precedenti più avanti in questo argomento.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="wizard-implementation"></a>Implementazione della procedura guidata

L'implementazione di una procedura guidata è simile all'implementazione di una normale finestra delle proprietà. Al livello più semplice, è necessario impostare uno dei flag o combinazioni di flag seguenti nella struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) che definisce la finestra delle proprietà.



| Contrassegno                           | Stile                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROCEDURA GUIDATA \_ PSH                    | Procedura guidata semplice senza intestazioni o bitmap.                                                                                                           |
| PSH \_ WIZARD \_ LITE              | Simile alla procedura guidata PSH, con alcune piccole differenze nell'aspetto. Ad esempio, il divisore sopra i pulsanti è impostato \_ sull'intera larghezza della finestra. |
| PROCEDURA GUIDATA \_ PSH97                  | Procedura guidata97 con intestazioni (facoltative), bitmap di intestazione e filigrane.                                                                            |
| PROCEDURA GUIDATA \_ \| PSH PSH - PROCEDURA GUIDATA PER LA CREAZIONE \_ GUIDATA PSH | Procedura guidata DiMito. Le procedure guidate di Aero non usano filigrane o bitmap di intestazione. Richiedono il modello apartment a thread singolo (STA).                         |



 

La procedura di base per l'implementazione di una procedura guidata è la seguente:

1.  Creare un modello di finestra di dialogo per ogni pagina.
2.  Definire le pagine creando una [**struttura PROPSHEETPAGE**](pss-propsheetpage.md) per ogni pagina. Questa struttura definisce la pagina e contiene puntatori al modello di finestra di dialogo ed eventuali bitmap o altre risorse.
3.  Passare la [**struttura PROPSHEETPAGE**](pss-propsheetpage.md) creata nel passaggio precedente alla funzione [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) per creare l'handle HPROPSHEETPAGE della pagina.
4.  Definire la procedura guidata creando una [**struttura PROPSHEETHEADER**](pss-propsheetheader.md) per la procedura.
5.  Passare la [**struttura PROPSHEETHEADER**](pss-propsheetheader.md) alla [**funzione PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) per visualizzare la procedura guidata.
6.  Implementare le procedure delle finestre di dialogo per ogni pagina per gestire i messaggi di notifica dai controlli della pagina e dai pulsanti della procedura guidata ed elaborare altri messaggi Windows messaggistica.

### <a name="create-the-dialog-box-templates"></a>Creare i modelli di finestra di dialogo

Esistono due tipi di base di pagina della procedura guidata: esterna e interna. Le pagine esterne sono le pagine introduttive e di completamento. Tutte le altre sono pagine interne.

**Modelli di finestra di dialogo della pagina esterna**

Il layout di base delle pagine di introduzione e completamento è identico. La figura seguente mostra una pagina introduttiva wizard97 di esempio, con una filigrana segnaposto.

![Screenshot che mostra una pagina della procedura guidata con un elemento grafico a sinistra, il testo del titolo e del corpo a destra e i pulsanti Avanti e Annulla nella parte inferiore](images/wiz97exterior.png)

Per le pagine esterne wizard97, il modello di finestra di dialogo è 317x193 unità di dialogo. Riempie tutta la procedura guidata, ad eccezione della didascalia e della banda nella parte inferiore che contiene i pulsanti **Indietro** **,** Avanti e **Annulla** . Il lato sinistro del modello, riservato per una bitmap "watermark", non deve contenere controlli. La filigrana viene specificata nella struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) della procedura guidata e viene aggiunta automaticamente alla pagina. Quando si progetta il modello di risorsa, è necessario lasciare spazio.

Quando si crea la bitmap della filigrana, tenere presente che le dimensioni della finestra di dialogo possono aumentare se, ad esempio, l'utente sceglie un tipo di carattere di sistema di grandi dimensioni. Anche lingue diverse tendono ad avere metriche dei tipi di carattere diverse. Quando la pagina aumenta, l'area riservata per la filigrana diventa proporzionalmente più grande. Tuttavia, non è possibile modificare la bitmap della filigrana né la bitmap viene estesa per riempire l'area più grande. Al contrario, la bitmap viene lasciata nella dimensione originale nella parte superiore sinistra dell'area riservata. La parte dell'area riservata più grande non coperta dalla filigrana viene riempita automaticamente con il colore del pixel superiore sinistro della bitmap.

Se è necessario disporre di bitmap di filigrana di dimensioni diverse per metriche dei tipi di carattere diverse, due possibili soluzioni sono:

-   Ottenere le metriche dei tipi di carattere prima di creare la procedura guidata e specificare una bitmap della filigrana di dimensioni appropriate.
-   Non specificare una bitmap del limite quando si crea la procedura guidata. Wizard97 lascia vuota l'area del limite. Disegnare quindi una bitmap di dimensioni appropriate sull'area riservata per la filigrana.

È possibile posizionare i controlli nell'area a destra della filigrana come si farebbe per una normale finestra di dialogo. Il colore di sfondo di quest'area è determinato dal sistema e non richiede alcuna azione da parte dell'utente. In genere vengono inseriti due controlli statici in quest'area. La parte superiore contiene il titolo e usa un carattere grassetto di grandi dimensioni (12 punti Verdana Grassetto per Wizard97). L'altra, per il testo esplicativo, usa il tipo di carattere standard della finestra di dialogo.

La differenza principale tra le pagine di introduzione e di completamento è che i pulsanti della procedura guidata e il testo nei controlli statici. Le pagine introduttive hanno in **genere un pulsante** Avanti e un **pulsante** Indietro, con solo il **pulsante** Avanti abilitato. Nelle pagine di completamento **è abilitato il** pulsante Indietro e il **pulsante** Avanti viene sostituito da **un pulsante** Fine.

> [!Note]  
> Nelle procedure guidate di Aero il **pulsante** Indietro viene sostituito da un pulsante freccia nella barra del titolo.

 

È possibile modificare il testo sul pulsante **Fine** inviando alla procedura guidata un [**messaggio \_ PSM SETFINISHTEXT.**](psm-setfinishtext.md) Per impostazione predefinita, il **pulsante Fine** non include un tasto di scelta rapida. Per definire un tasto di scelta rapida, includere una e commerciale nella stringa di testo passata a \_ PSM SETFINISHTEXT. Ad esempio, "&fine" definisce "F" come tasto di scelta rapida.

**Modelli di finestra di dialogo pagina interna**

Le pagine interne hanno un aspetto leggermente diverso rispetto alle pagine esterne. Nella figura seguente viene illustrata una pagina interna wizard97 di esempio, con una bitmap di intestazione segnaposto.

![Screenshot di una pagina della procedura guidata con il testo del titolo e del sottotitolo e un elemento grafico nella parte superiore, il testo al centro e i pulsanti nella parte inferiore](images/wiz97interior.png)

L'area di intestazione nella parte superiore della pagina viene gestita dalla finestra delle proprietà, quindi non è inclusa nel modello. Il contenuto dell'intestazione viene specificato nella struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) della pagina e nella struttura [**PROPSHEETHEADER della**](pss-propsheetheader.md) procedura guidata. Poiché la pagina interna deve rientrare tra l'intestazione e i pulsanti, il modello di finestra di dialogo Wizard97 è di 317 x 143 unità di dialogo, un po' più piccolo del modello per le pagine esterne.

Nella figura seguente viene illustrata una procedura guidata Diameti creata dallo stesso modello.

![Screenshot che differisce da quello precedente con un'area del titolo nella parte superiore e solo i pulsanti Avanti e Annulla nella parte inferiore](images/wizardaerointerior.png)

### <a name="define-the-wizard-pages"></a>Definire le pagine della procedura guidata

Dopo aver creato i modelli di finestra di dialogo e le risorse correlate, ad esempio bitmap e tabelle di stringhe, è possibile creare le pagine della finestra delle proprietà. La procedura è simile a quella per le finestre delle proprietà standard. Prima di tutto, compilare i membri appropriati di una [**struttura PROPSHEETPAGE.**](pss-propsheetpage.md) Alcuni membri sono specifici delle procedure guidate. Chiamare quindi la [**funzione CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) per creare l'handle HPROPSHEETPAGE della pagina.

I flag correlati alla procedura guidata seguenti possono essere impostati nel membro **dwFlags** della [**struttura PROPSHEETPAGE.**](pss-propsheetpage.md)



| Flag                   | Descrizione                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| PSP \_ HIDEHEADER        | Impostare questo flag per le pagine esterne in Wizard97. L'intestazione non viene visualizzata e può essere visualizzata una filigrana.                                |
| PSP \_ USEHEADERTITLE    | Impostare questo flag per le pagine interne in modo da inserire un titolo nell'area dell'intestazione in Wizard97 o nella parte superiore dell'area client in una procedura guidata Aero. |
| PSP \_ USEHEADERSUBTITLE | Impostare questo flag per le pagine interne per inserire un sottotitolo nell'area dell'intestazione in Wizard97.                                                  |



 

Se è stato impostato PSP USEHEADERTITLE o PSP USEHEADERSUBTITLE, assegnare il testo del titolo e del sottotitolo rispettivamente ai membri \_ \_ **pszHeaderTitle** e **pszHeaderSubtitle.** Quando si assegnano stringhe di testo ai membri delle strutture [**PROPSHEETPAGE**](pss-propsheetpage.md) e [**PROPSHEETHEADER,**](pss-propsheetheader.md) è possibile assegnare un puntatore di stringa o usare la macro **MAKEINTRESOURCE** per assegnare un valore da una risorsa stringa. La risorsa stringa viene caricata dal modulo specificato nel membro **hInstance** della struttura **PROPSHEETHEADER della** procedura guidata.

Quando si chiama [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) per creare una pagina, assegnare il risultato a un elemento di una matrice di handle HPROPSHEETPAGE. Questa matrice viene utilizzata durante la creazione della finestra delle proprietà. L'indice della matrice dell'handle di una pagina determina l'ordine predefinito in cui viene visualizzato. Dopo aver creato l'handle HPROPSHEETPAGE di una pagina, è possibile riutilizzare la stessa [**struttura PROPSHEETPAGE**](pss-propsheetpage.md) per creare la pagina successiva assegnando nuovi valori ai membri pertinenti.

Un modo alternativo per creare pagine consiste nell'usare strutture [**PROPSHEETPAGE**](pss-propsheetpage.md) separate per ogni pagina e creare una matrice di strutture. Questa matrice viene usata al posto di una matrice di handle HPROPSHEETPAGE durante la creazione della finestra delle proprietà. **L'uso di strutture PROPSHEETPAGE** separate elimina la necessità di chiamare [**CreatePropertySheetPage,**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) ma usa più memoria. In caso contrario, non esiste alcuna differenza significativa tra i due approcci.

Nell'esempio seguente viene definita una pagina interna di Wizard97 assegnando valori a una [**struttura PROPSHEETPAGE.**](pss-propsheetpage.md) In questo esempio il titolo, il sottotitolo e il modello di finestra di dialogo della pagina sono tutti identificati dagli ID risorsa. Viene quindi chiamata la funzione [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) per creare l'handle HPROPSHEETPAGE della pagina. Poiché sarà la seconda pagina visualizzata, l'handle viene assegnato alla matrice di handle, *ahpsp*, con indice 1.


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



### <a name="custom-page-data"></a>Dati di pagina personalizzati

Quando si crea una pagina, è possibile assegnarle dati personalizzati usando il membro **lParam** della struttura [**PROPSHEETPAGE,**](pss-propsheetpage.md) in genere assegnando un puntatore a una struttura definita dall'utente.

Quando la pagina viene selezionata per la prima volta, la relativa routine della finestra di dialogo riceve un [**messaggio WM \_ INITDIALOG.**](/windows/desktop/dlgbox/wm-initdialog) Il valore *lParam* del messaggio punta a una copia della struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) della pagina, da cui è possibile recuperare i dati personalizzati. È quindi possibile archiviare questi dati per l'uso nei messaggi successivi usando [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) con GWL \_ USERDATA come parametro di indice. Più pagine possono avere un puntatore agli stessi dati e qualsiasi modifica ai dati apportati da una pagina è disponibile per le altre pagine nelle procedure di dialogo.

### <a name="define-the-wizard-property-sheet"></a>Definire la finestra delle proprietà della procedura guidata

Come per le normali finestre delle proprietà, la finestra delle proprietà della procedura guidata viene definita compilando i membri di una [**struttura PROPSHEETHEADER.**](pss-propsheetheader.md) Questa struttura consente di specificare le pagine che costituiscono la procedura guidata e l'ordine predefinito in cui vengono visualizzate, insieme a diversi parametri correlati. Avviare quindi la procedura guidata chiamando la [**funzione PropertySheet.**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)

Nello stile Wizard97 il membro **pszCaption** della [**struttura PROPSHEETHEADER**](pss-propsheetheader.md) viene ignorato. La procedura guidata visualizza invece la didascalia specificata nel modello di finestra di dialogo della pagina corrente. Se il modello non dispone di una didascalia, viene visualizzata la didascalia della pagina precedente. Pertanto, per visualizzare la stessa didascalia in tutte le pagine, specificare la didascalia nel modello per la pagina introduttiva.

Nello stile della procedura guidata Aero, la didascalia della finestra di dialogo viene presa da **pszCaption**.

Se è stata creata una matrice di handle HPROPSHEETPAGE per le pagine, assegnare la matrice al **membro phpage.** Se invece è stata creata una matrice di strutture [**PROPSHEETPAGE,**](pss-propsheetpage.md) assegnare la matrice al membro **ppsp** e impostare il flag PSH PROPSHEETPAGE nel membro \_ **dwFlags.**

Nell'esempio seguente vengono assegnati valori a *psh*, una [**struttura PROPSHEETHEADER**](pss-propsheetheader.md) e viene chiamata la [**funzione PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) per avviare la procedura guidata. La procedura guidata in stile Wizard97 include elementi grafici con filigrana e intestazione, specificati dagli ID risorsa. La *matrice ahpsp* contiene tutti gli handle HPROPSHEETPAGE e definisce l'ordine predefinito in cui vengono visualizzati.


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



### <a name="the-dialog-box-procedure"></a>Procedura della finestra di dialogo

Ogni pagina della procedura guidata richiede una procedura della finestra di dialogo per elaborare Windows messaggi, in particolare le notifiche dai relativi controlli e dalla procedura guidata. I tre messaggi che quasi tutte le procedure guidate devono essere in grado di gestire sono [**WM \_ INITDIALOG,**](/windows/desktop/dlgbox/wm-initdialog) [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)e [**WM \_ NOTIFY.**](wm-notify.md)

Il [**messaggio WM \_ NOTIFY**](wm-notify.md) viene ricevuto prima della visualizzazione della pagina e quando viene fatto clic su uno dei pulsanti della procedura guidata. Il *parametro lParam* del messaggio è un puntatore a una [**struttura di intestazione NMHDR.**](/windows/desktop/api/richedit/ns-richedit-nmhdr) L'ID della notifica è contenuto nel membro di **codice della** struttura. Le quattro notifiche che la maggior parte delle procedure guidate devono gestire sono le seguenti.



| Codice                                | Descrizione                                 |
|-------------------------------------|---------------------------------------------|
| [PSN \_ SETACTIVE](psn-setactive.md) | Inviato prima della visualizzazione della pagina.          |
| [PSN \_ WIZBACK](psn-wizback.md)     | Inviato quando si **fa clic sul** pulsante Indietro.   |
| [PSN \_ WIZNEXT](psn-wiznext.md)     | Inviato quando si **fa clic sul** pulsante Avanti.   |
| [PSN \_ WIZFINISH](psn-wizfinish.md) | Inviato quando si **fa clic sul** pulsante Fine. |



 

### <a name="handle-wm_initdialog-and-wm_destroy"></a>Gestire WM \_ INITDIALOG e WM \_ DESTROY

Quando una pagina sta per essere visualizzata per la prima volta, la relativa routine della finestra di dialogo riceve un [**messaggio WM \_ INITDIALOG.**](/windows/desktop/dlgbox/wm-initdialog) La gestione di questo messaggio consente alla procedura guidata di eseguire tutte le attività di inizializzazione necessarie, ad esempio l'archiviazione di dati personalizzati o l'impostazione dei tipi di carattere.

Quando la finestra delle proprietà viene distrutta, viene visualizzato un [**messaggio WM \_ DESTROY.**](/windows/desktop/winmsg/wm-destroy) La procedura guidata viene automaticamente distrutta dal sistema, ma la gestione di questo messaggio consente di eseguire la pulizia necessaria.

### <a name="handle-psn_setactive"></a>Gestire PSN \_ SETACTIVE

Il [codice di notifica \_ PSN SETACTIVE](psn-setactive.md) viene inviato ogni volta che una pagina sta per essere resa visibile. La prima volta che viene visitata una pagina, PSN \_ SETACTIVE segue il [**messaggio WM \_ INITDIALOG.**](/windows/desktop/dlgbox/wm-initdialog) Se la pagina viene successivamente rivisitata, riceve solo una notifica \_ PSN SETACTIVE. Questa notifica viene in genere gestita per inizializzare i dati per la pagina e abilitare i pulsanti appropriati.

Per impostazione predefinita, nella procedura guidata vengono visualizzati **i pulsanti** **Indietro**, Avanti **e** Annulla , con tutti i pulsanti abilitati. Per disabilitare un pulsante o visualizzare **Fine** anziché **Avanti,** è necessario inviare un [**messaggio \_ SETWIZBUTTONS PSM.**](psm-setwizbuttons.md) Dopo l'invio, lo stato dei pulsanti viene mantenuto fino a quando non viene modificato da un altro messaggio **\_ SETWIZBUTTONS PSM,** anche se è selezionata una nuova pagina. In genere, tutti [i gestori \_ SETACTIVE PSN](psn-setactive.md) inviano questo messaggio per assicurarsi che ogni pagina abbia lo stato corretto del pulsante.

È possibile modificare lo stato del pulsante con questo messaggio in qualsiasi momento. Ad esempio, è possibile che il **pulsante** Avanti venga inizialmente disabilitato. Dopo che un utente ha immesso tutte le informazioni necessarie, è possibile  inviare un altro messaggio [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md) per abilitare il pulsante Avanti e consentire all'utente di passare alla pagina successiva.

Il frammento di codice seguente usa la macro  [**\_ PropSheet SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) per abilitare i pulsanti Indietro e Avanti in una pagina interna prima che venga visualizzata. 


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

Quando si **fa clic** su **un pulsante** Avanti o Indietro, si riceve un codice di notifica [ \_ PSN WIZNEXT](psn-wiznext.md) o [PSN \_ WIZBACK.](psn-wizback.md) Per impostazione predefinita, la procedura guidata passa automaticamente alla pagina successiva o precedente nell'ordine definito al momento della creazione della finestra delle proprietà. Un motivo comune per gestire queste notifiche è impedire all'utente di cambiare pagina o di eseguire l'override dell'ordine di pagina predefinito.

Per impedire all'utente di cambiare pagina, gestire la notifica del pulsante, chiamare la [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il valore MSGRESULT DWL impostato \_ su -1 e restituire **TRUE.** Esempio:


```C++
case PSN_WIZNEXT :

        ...
        
        // Do not go to the next page yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, -1);
        
        return TRUE;
        
        ...
```



Per eseguire l'override dell'ordine standard e passare a una pagina specifica, chiamare [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il valore MSGRESULT DWL impostato sull'ID risorsa della finestra di dialogo della pagina \_ e restituire **TRUE**. Esempio:


```C++
case PSN_WIZNEXT :

        ...
        
        // Go straight to the completion page.
        SetWindowLong(hwnd, DWL_MSGRESULT, IDD_FINISH);
        
        return TRUE;
        
        ...
```



Quando si **fa clic** **sul** pulsante Fine o Annulla, si riceve rispettivamente un codice di notifica [PSN \_ WIZFINISH](psn-wizfinish.md) o [PSN \_ RESET.](psn-reset.md) Quando si fa clic su uno di questi pulsanti, la procedura guidata viene automaticamente distrutta dal sistema. Tuttavia, è possibile gestire queste notifiche se è necessario eseguire attività di pulizia prima che la procedura guidata venga distrutta. Per evitare che la procedura guidata venga distrutta quando si riceve una notifica \_ PSN WIZFINISH, chiamare [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il valore \_ DWL MSGRESULT impostato su **TRUE** e restituire **TRUE**. Esempio:


```C++
case PSN_WIZFINISH :

        ...
        
        // Not finished yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, TRUE);
        
        return TRUE;
        
        ...
```



### <a name="backward-compatible-wizards"></a>Procedure guidate compatibili con le versioni precedenti

Nella sezione precedente si presuppone che si sta implementando una procedura guidata per un sistema con [la versione 5](common-control-versions.md) o successiva dei controlli comuni.

Se si scrive una procedura guidata per sistemi con versioni precedenti dei controlli comuni, molte delle funzionalità descritte nella sezione precedente non saranno disponibili. Alcuni membri delle strutture [**PROPSHEETHEADER**](pss-propsheetheader.md) e [**PROPSHEETPAGE**](pss-propsheetpage.md) usati dallo stile Wizard97 sono supportati solo dai controlli comuni versione 5 e successive. Tuttavia, è comunque possibile implementare una procedura *guidata* compatibile con le versioni precedenti con un aspetto simile a quello dello stile Wizard97. A tale scopo, è necessario implementare in modo esplicito quanto segue:

-   Aggiungere l'immagine della filigrana al modello di finestra di dialogo per le pagine di introduzione e completamento.
-   Impostare le stesse dimensioni per tutti i modelli. Non esiste un'area di intestazione definita dal sistema separata per le pagine interne.
-   Creare l'area di intestazione della pagina interna in modo esplicito nei modelli.
-   Non usare un'immagine di intestazione perché potrebbe essere in conflitto con il titolo o il sottotitolo se le dimensioni della procedura guidata cambiano.

Per altre informazioni sulle procedure guidate compatibili con le versioni precedenti, vedere Procedura guidata compatibile con le versioni precedenti [97.](/previous-versions//ms737910(v=vs.85))

## <a name="remarks"></a>Commenti

Per una descrizione completa dei problemi di progettazione per Wizard97, vedere la [specifica Wizard97,](/previous-versions//ms738248(v=vs.85))altrove in Windows SDK. Questo documento contiene linee guida per elementi quali le dimensioni per le finestre di dialogo, le dimensioni e i colori delle bitmap e la posizione dei controlli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle finestre delle proprietà](using-property-sheets.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 