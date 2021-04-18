---
title: Struttura PROPSHEETHEADER (Prsht. h)
description: Definisce il frame e le pagine di una finestra delle proprietà.
keywords:
- Controlli di Windows della struttura PROPSHEETHEADER
topic_type:
- apiref
api_name:
- PROPSHEETHEADER
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/23/2021
ms.openlocfilehash: 90a11ff727b491a1801f8071e28c39a3a6594408
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323847"
---
# <a name="propsheetheader--structure"></a>Struttura PROPSHEETHEADER

Definisce il frame e le pagine di una finestra delle proprietà.

## <a name="syntax"></a>Sintassi

```cpp
typedef struct {
    DWORD      dwSize;
    DWORD      dwFlags;
    HWND       hwndParent;
    HINSTANCE  hInstance;
    union {
        HICON   hIcon;
        LPCTSTR pszIcon;
    };
    LPCTSTR  pszCaption;
    UINT     nPages;
    union {
        UINT    nStartPage;
        LPCTSTR pStartPage;
    };
    union {
        LPCPROPSHEETPAGE ppsp;
        HPROPSHEETPAGE   *phpage;
    };
    PFNPROPSHEETCALLBACK pfnCallback;
    union {
        HBITMAP hbmWatermark;
        LPCTSTR pszbmWatermark;
    };
    HPALETTE  hplWatermark;
    union {
        HBITMAP hbmHeader;
        LPCSTR  pszbmHeader;
    };
} PROPSHEETHEADER, *LPPROPSHEETHEADER;
```

## <a name="members"></a>Members

*dwSize* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Dimensione, in byte, della struttura. Il gestore della finestra delle proprietà utilizza questo membro per determinare la versione della struttura **PROPSHEETHEADER** in uso. Per ulteriori informazioni, vedere la sezione Osservazioni.

*dwFlags* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Flag che indicano le opzioni da utilizzare durante la creazione della pagina della finestra delle proprietà. Questo membro può essere una combinazione dei valori seguenti.

| Valore | Significato |
|-------|---------|
| PSH_DEFAULT (0x00000000) | Usa il significato predefinito per tutti i membri della struttura e crea una normale finestra delle proprietà. Questo flag ha un valore pari a zero e non è combinato con altri flag. |
| PSH_AEROWIZARD (0x00004000) | [Versione 6,00](common-control-versions.md) e successive. Crea una finestra delle proprietà della procedura guidata che usa lo stile Aero. È necessario impostare anche il flag di PSH_WIZARD. È necessario usare il modello di Apartment a thread singolo (STA). |
| PSH_HASHELP (0x00000200) | Consente di **visualizzare un pulsante** ? nelle pagine delle proprietà della finestra delle proprietà. Al momento della creazione della pagina, è necessario impostare anche il flag PSP_HASHELP nella struttura [PROPSHEETPAGE](pss-propsheetpage.md) della pagina. Se una delle pagine della finestra delle proprietà iniziale Abilita **un pulsante** ?, PSH_HASHELP verrà impostato automaticamente. Se nessuna delle pagine iniziali Abilita un pulsante?, è necessario impostare in modo esplicito PSH_HASHELP se si desidera visualizzare i pulsanti **della Guida in** qualsiasi pagina che potrebbe essere aggiunta in un secondo momento. Questo flag non è supportato in combinazione con PSH_AEROWIZARD.|
| PSH_HEADER (0x00080000) | [Versione 5,80](common-control-versions.md) e successive. Indica che verrà utilizzata una bitmap dell'intestazione con una procedura guidata Wizard97. È anche necessario impostare il flag di PSH_WIZARD97. Se viene impostato il flag di PSH_USEHBMHEADER, la bitmap dell'intestazione viene ottenuta dal membro *hbmHeader* . In caso contrario, la bitmap dell'intestazione viene ottenuta dal membro *pszbmHeader* . Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |
| PSH_HEADERBITMAP (0x08000000) | [Versione 6,00](common-control-versions.md) e successive. Il membro *pszbmHeader* specifica una bitmap visualizzata nell'area di intestazione. Deve essere usato in combinazione con PSH_AEROWIZARD. |
| PSH_MODELESS (0x00000400) | Fa in modo che la funzione [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) crei la finestra delle proprietà come finestra di dialogo non modale anziché come finestra di dialogo modale. Quando questo flag è impostato, [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) viene restituito immediatamente dopo la creazione della finestra di dialogo e il valore restituito da [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) è l'handle della finestra per la finestra di dialogo della finestra delle proprietà. Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |
| PSH_NOAPPLYNOW (0x00000080) | Rimuove il pulsante **applica** . Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |
| PSH_NOCONTEXTHELP (0x02000000) | [Versione 5,80](common-control-versions.md) e successive. Rimuove il pulsante della Guida sensibile al contesto ("?"), che è in genere presente sulla barra del titolo delle finestre delle proprietà. Questo flag non è valido per le procedure guidate. Per una descrizione di come rimuovere il pulsante della **Guida** della barra del titolo per le versioni precedenti dei controlli comuni, vedere [informazioni sulle finestre delle proprietà](property-sheets.md) . Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |
| PSH_NOMARGIN (0x10000000) | [Versione 6,00](common-control-versions.md) o successiva. Specifica che non viene inserito alcun margine tra la pagina e il frame. Deve essere usato in combinazione con PSH_AEROWIZARD. |
| PSH_PROPSHEETPAGE (0x00000008) | Usa il membro *ppSP* e ignora il membro *phpage* quando si creano le pagine per la finestra delle proprietà. |
| PSH_PROPTITLE (0x00000001) | Indica che *pszCaption* è il nome dell'elemento per cui vengono visualizzate le proprietà. Windows esegue una regolazione dipendente dalla versione e dalla lingua per la didascalia. Ad esempio, in inglese, la frase "Properties per" viene anteposta a un *pszCaption* non vuoto (e se *pszCaption* genera una didascalia vuota, il titolo è semplicemente "Properties"). Se questo flag viene omesso, pszCaption viene usato invariato.  |
| PSH_RESIZABLE (0x04000000) | Consente il ridimensionamento della procedura guidata da parte dell'utente. I pulsanti Ingrandisci e Riduci a icona vengono visualizzati nel frame della procedura guidata e il frame è ridimensionabile. Per utilizzare questo flag, è necessario impostare anche PSH_AEROWIZARD. |
| PSH_RTLREADING (0x00000800) | Imposta la finestra delle proprietà o la finestra della procedura guidata sull'ordine di lettura da destra a sinistra (RTL), appropriato per lingue come l'ebraico e l'arabo. Se questo flag non è specificato, la finestra delle proprietà viene impostata per impostazione predefinita sull'ordine di lettura da sinistra a destra (LTR) e le finestre della procedura guidata corrispondono all'ordine di lettura della pagina corrente. |
| PSH_STRETCHWATERMARK (0x00040000) | Estende la filigrana nelle creazioni guidate di tipo Wizard97. Questo flag non è supportato in combinazione con PSH_AEROWIZARD. Questo flag di stile è incluso solo per garantire la compatibilità con le versioni precedenti di alcune applicazioni. Il suo utilizzo non è consigliato ed è supportato solo dai controlli comuni versioni 4,0 e 4,01. Con i controlli comuni versione 5,80 e successive, questo flag viene ignorato. |
| PSH_USECALLBACK (0x00000100) | Chiama la funzione specificata dal parametro *pfnCallback* quando si verificano determinati eventi. Per ulteriori informazioni, vedere la descrizione della funzione di callback [PFNPROPSHEETCALLBACK](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) . |
| PSH_USEHBMHEADER (0x00100000) | [Versione 5,80](common-control-versions.md). Ottiene la bitmap dell'intestazione dal membro *hbmHeader* anziché dal membro *pszbmHeader* . È anche necessario impostare il flag di PSH_AEROWIZARD o il flag di PSH_WIZARD97 insieme al flag di PSH_HEADER. |
| PSH_USEHBMWATERMARK (0x00010000) | [Versione 5,80](common-control-versions.md). Ottiene la bitmap della filigrana dal membro *hbmWatermark* anziché dal membro *pszbmWatermark* . È inoltre necessario impostare PSH_WIZARD97 e PSH_WATERMARK. Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |
| PSH_USEHICON (0x00000002) | USA *HICON* come piccola icona nella barra del titolo della finestra di dialogo della finestra delle proprietà. |
| PSH_USEHPLWATERMARK (0x00020000) | [Versione 5,80](common-control-versions.md). Usa la struttura **HPALETTE** a cui fa riferimento il membro *hplWatermark* anziché la tavolozza predefinita per creare la bitmap della filigrana e/o la bitmap dell'intestazione per una procedura guidata Wizard97. È inoltre necessario impostare PSH_WIZARD97 e PSH_WATERMARK o PSH_HEADER. Questo flag non è supportato in combinazione con PSH_AEROWIZARD.  |
| PSH_USEICONID (0x00000004) | Utilizza *pszIcon* come nome della risorsa icona da caricare e utilizzare come piccola icona nella barra del titolo della finestra di dialogo della finestra delle proprietà. |
| PSH_USEPAGELANG (0x00200000) | [Versione 5,80](common-control-versions.md). Specifica che la lingua per la finestra delle proprietà verrà ricavata dalla risorsa della prima pagina. Questa pagina deve essere specificata dall'identificatore di risorsa. |
| PSH_USEPSTARTPAGE (0x00000040) | Usa il membro *pStartPage* anziché il membro *nStartPage* quando viene visualizzata la pagina iniziale della finestra delle proprietà. |
| PSH_WATERMARK (0x00008000) | [Versione 5,80](common-control-versions.md). Specifica che una bitmap della filigrana verrà utilizzata con una procedura guidata Wizard97 nelle pagine con lo stile PSP_HIDEHEADER. È anche necessario impostare il flag di PSH_WIZARD97. La bitmap della filigrana è ottenuta dal membro *pszbmWatermark* , a meno che non sia impostato PSH_USEHBMWATERMARK. In tal caso, la bitmap dell'intestazione viene ottenuta dal membro *hbmWatermark* . Questo flag non è supportato in combinazione con PSH_AEROWIZARD.  |
| PSH_WIZARD (0x00000020) | Crea una finestra delle proprietà della procedura guidata. Quando si utilizza PSH_AEROWIZARD, è necessario impostare anche questo flag. |
| PSH_WIZARD97 (0x01000000) | [Versione 5,80](common-control-versions.md). Crea una finestra delle proprietà di tipo Wizard97, che supporta le bitmap nell'intestazione delle pagine interne e sul lato sinistro delle pagine esterne. Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |
| PSH_WIZARDCONTEXTHELP (0x00001000) | Aggiunge un pulsante della **Guida** sensibile al contesto ("?"), che in genere è assente dalla barra del titolo di una procedura guidata. Questo flag non è valido per le finestre delle proprietà regolari. Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |
| PSH_WIZARDHASFINISH (0x00000010)  | Visualizza sempre il pulsante **fine** della procedura guidata. È inoltre necessario impostare PSH_WIZARD, PSH_WIZARD97 o PSH_AEROWIZARD. |
| PSH_WIZARD_LITE (0x00400000) | [Versione 5,80](common-control-versions.md). USA lo stile della procedura guidata-versione Lite. Questo stile ha un aspetto simile a quello di PSH_WIZARD97, ma viene implementato molto come PSH_WIZARD. Esistono alcune limitazioni relative alla formattazione delle pagine. Ad esempio, non sono presenti bordi applicati e lo stile del PSH_WIZARD_LITE non disegna le bitmap della filigrana e dell'intestazione nel modo in cui Wizard97. Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |

*hwndParent* 

Tipo: [HWND](../winprog/windows-data-types.md)

Handle per la finestra proprietaria della finestra delle proprietà.

*hInstance* 

Tipo: [HINSTANCE](../winprog/windows-data-types.md)

Handle per l'istanza da cui caricare l'icona, la risorsa di stringa del titolo, il nome della pagina iniziale, la bitmap dell'intestazione o la filigrana. Se il membro *pszIcon*, *pszCaption*, *pStartPage*, *pszbmHeader* o *pszbmWatermark* identifica una risorsa da caricare, è necessario specificare questo membro.

*hIcon* 

Tipo: [HICON](../winprog/windows-data-types.md)

Handle per l'icona da utilizzare come piccola icona nella barra del titolo della finestra di dialogo della finestra delle proprietà. Questo membro viene utilizzato se il membro *dwFlags* include PSH_USEHICON. Questo membro viene dichiarato come Unione con *pszIcon*.

*pszIcon* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

Icona risorsa da utilizzare come piccola icona nella barra del titolo della finestra di dialogo finestra delle proprietà. Questo membro viene utilizzato se il membro *dwFlags* include PSH_USEICONID. Questo membro può specificare l'identificatore della risorsa icona o l'indirizzo della stringa che specifica il nome della risorsa icona. In entrambi i casi, l'icona viene caricata dall'istanza fornita dal membro *HINSTANCE* . Questo membro viene dichiarato come Unione con *HICON*.

*pszCaption* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

Titolo della finestra di dialogo della finestra delle proprietà. Questo membro può specificare l'identificatore di una risorsa di tipo stringa (caricata dall'istanza specificata dal membro *HINSTANCE* ) o l'indirizzo di una stringa che specifica il titolo. Se il membro *dwFlags* include PSH_PROPTITLE, le proprietà della stringa **per** vengono inserite all'inizio del titolo. Questo campo viene ignorato per le procedure guidate Wizard97. Per le procedure guidate Aero, viene usata solo la stringa per la didascalia, indipendentemente dal fatto che sia impostato il flag PSH_PROPTITLE.

*nPages* 

Tipo: [uint](../winprog/windows-data-types.md)

Numero di pagine della finestra delle proprietà fornite nella matrice *ppSP* o *phpage* .

*nStartPage* 

Tipo: [uint](../winprog/windows-data-types.md)

Indice in base zero della pagina iniziale visualizzata quando viene creata la finestra di dialogo della finestra delle proprietà. Questo membro viene utilizzato se il membro *dwFlags* non include il flag PSH_USEPSTARTPAGE. Questo membro viene dichiarato come Unione con *pStartPage*.

*pStartPage* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

Nome della pagina iniziale visualizzata quando viene creata la finestra di dialogo della finestra delle proprietà. Questo membro viene utilizzato se il membro *dwFlags* include il flag PSH_USESTARTPAGE. Questo membro può specificare l'identificatore di una risorsa di tipo stringa (caricata dall'istanza specificata dal membro *HINSTANCE* ) o l'indirizzo di una stringa che specifica il nome. Il nome della pagina iniziale viene confrontato con le didascalie delle pagine. Questo membro viene dichiarato come Unione con *nStartPage*.

*ppsp* 

Tipo: **LPCPROPSHEETPAGE**

Puntatore a una matrice di strutture [PROPSHEETPAGE](pss-propsheetpage.md) che definiscono le pagine nella finestra delle proprietà. Se il membro *dwFlags* non include PSH_PROPSHEETPAGE, questo membro viene ignorato. Si noti che la struttura **PROPSHEETPAGE** è di dimensioni variabili. Le applicazioni che analizzano la matrice a cui fa riferimento *ppSP* devono prendere in considerazione le dimensioni di ogni pagina. Questo membro viene dichiarato come Unione con *phpage*.

*phpage* 

Tipo: **HPROPSHEETPAGE \***

Puntatore a una matrice di handle per le pagine della finestra delle proprietà. Questo membro viene utilizzato se il membro *dwFlags* non include PSH_PROPSHEETPAGE. Ogni handle deve essere stato creato da una chiamata precedente alla funzione [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . Quando viene restituita la funzione [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) , tutti gli handle HPROPSHEETPAGE nella matrice *phpage* sono stati eliminati definitivamente. Questo membro viene dichiarato come Unione con *ppSP*.

*pfnCallback* 

Tipo: **PFNPROPSHEETCALLBACK**

Puntatore a una funzione di callback definita dall'applicazione che viene chiamata quando si verificano determinati eventi. Per ulteriori informazioni sulla funzione di callback, vedere la descrizione della funzione di callback [PFNPROPSHEETCALLBACK](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) . Se il membro *dwFlags* non include PSH_USECALLBACK, questo membro viene ignorato.

*hbmWatermark* 

Tipo: [HBITMAP](../winprog/windows-data-types.md)

[Versione 5,80](common-control-versions.md) o successiva. Handle per la bitmap della filigrana. Se il membro *dwFlags* non include PSH_USEHBMWATERMARK, questo membro viene ignorato.

*pszbmWatermark* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

[Versione 5,80](common-control-versions.md) o successiva. Risorsa bitmap da usare come filigrana. Questo membro può specificare l'identificatore della risorsa bitmap o l'indirizzo della stringa che specifica il nome della risorsa bitmap. Se il membro *dwFlags* include PSH_USEHBMWATERMARK, questo membro viene ignorato.

*hplWatermark*

Tipo: [HPALETTE](../winprog/windows-data-types.md)

[Versione 5,80](common-control-versions.md) o successiva. Struttura **HPALETTE** utilizzata per disegnare la bitmap della filigrana e/o la bitmap dell'intestazione. Se il membro *dwFlags* non include PSH_USEHPLWATERMARK, questo membro viene ignorato.

*hbmHeader*

Tipo: [HBITMAP](../winprog/windows-data-types.md)

[Versione 5,80](common-control-versions.md) o successiva. Handle per la bitmap dell'intestazione. Se il membro *dwFlags* non include PSH_USEHBMHEADER, questo membro viene ignorato.

*pszbmHeader*

Tipo: [LPCSTR](../winprog/windows-data-types.md)

[Versione 5,80](common-control-versions.md) o successiva. Risorsa bitmap da utilizzare come intestazione. Questo membro può specificare l'identificatore della risorsa bitmap o l'indirizzo della stringa che specifica il nome della risorsa bitmap. Se il membro *dwFlags* include PSH_USEHBMHEADER, questo membro viene ignorato.

## <a name="remarks"></a>Commenti

Se l'utente sceglie un'impostazione, ad esempio caratteri di grandi dimensioni, che ingrandisce la finestra di dialogo, verrà ingrandita anche la filigrana disegnata nelle pagine di inizio e fine. Le dimensioni e la posizione della bitmap originale rimarranno invariate. L'area aggiuntiva verrà riempita con il colore del pixel nell'angolo superiore sinistro della bitmap.

Gli stili PSH_WIZARD, PSH_WIZARD97 e PSH_WIZARD_LITE non sono compatibili. È necessario impostare solo uno di questi flag di stile. PSH_AEROWIZARD deve essere combinato con PSH_WIZARD.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | \[Solo app desktop di Windows Vista\]                                    |
| Server minimo supportato | \[Solo app desktop Windows Server 2003\]                              |
| Intestazione                   | Prsht. h |
| Nomi Unicode e ANSI                   | **PROPSHEETHEADERW** (Unicode) e **PROPSHEETHEADERA** (ANSI) |
