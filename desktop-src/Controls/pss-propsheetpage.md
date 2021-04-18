---
title: Struttura PROPSHEETPAGE (Prsht. h)
description: Definisce una pagina in una finestra delle proprietà.
keywords:
- Controlli di Windows della struttura PROPSHEETPAGE
topic_type:
- apiref
api_name:
- PROPSHEETPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/23/2021
ms.openlocfilehash: cdde3f27900c7599b33af706d8fac9f9e8127b6f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323831"
---
# <a name="propsheetpage-structure"></a>Struttura PROPSHEETPAGE

Definisce una pagina in una finestra delle proprietà.

## <a name="syntax"></a>Sintassi

```cpp
typedef struct {
    DWORD      dwSize;
    DWORD      dwFlags;
    HINSTANCE  hInstance;
    union {
        LPCSTR                 pszTemplate;
        PROPSHEETPAGE_RESOURCE pResource;
    };
    union {
        HICON  hIcon;
        LPCSTR pszIcon;
    };
    LPCSTR          pszTitle;
    DLGPROC         pfnDlgProc;
    LPARAM          lParam;
    LPFNPSPCALLBACK pfnCallback;
    UINT            *pcRefParent;
    LPCTSTR         pszHeaderTitle;
    LPCTSTR         pszHeaderSubTitle;
    HANDLE          hActCtx;
    union 
    {
        HBITMAP     hbmHeader;
        LPCSTR      pszbmHeader;
    }
} PROPSHEETPAGE, *LPPROPSHEETPAGE;
```

## <a name="members"></a>Members

*dwSize* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Dimensione, in byte, della struttura.

*dwFlags* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Flag che indicano le opzioni da utilizzare durante la creazione della pagina della finestra delle proprietà. Questo membro può essere una combinazione dei valori seguenti.

| Valore | Significato |
|-------|---------|
| PSP_DEFAULT | Usa il significato predefinito per tutti i membri della struttura. Questo flag non è supportato quando si utilizza la procedura guidata stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_DLGINDIRECT | Crea la pagina dal modello della finestra di dialogo in memoria a cui fa riferimento il membro di *preorigine* . La funzione [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) presuppone che il modello in memoria non sia protetto da scrittura. Un modello di sola lettura provocherà un'eccezione in alcune versioni di Windows. |
| PSP_HASHELP | Abilita il pulsante della **Guida** della finestra delle proprietà quando la pagina è attiva. Questo flag non è supportato quando si utilizza la procedura guidata stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_HIDEHEADER | [Versione 5,80](common-control-versions.md) e successive. Fa in modo che la finestra delle proprietà della procedura guidata nasconda l'area di intestazione quando la pagina è selezionata. Se è stata specificata una filigrana, questa verrà disegnata sul lato sinistro della pagina. Questo flag deve essere impostato per le pagine di benvenuto e di completamento e viene omesso per le pagine interne. Questo flag non è supportato quando si utilizza la procedura guidata stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_PREMATURE | [Versione 4,71](common-control-versions.md) o successiva. Determina la creazione della pagina al momento della creazione della finestra delle proprietà. Se questo flag non è specificato, la pagina non verrà creata finché non viene selezionata la prima volta. Questo flag non è supportato quando si utilizza la procedura guidata stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_RTLREADING | Inverte la direzione in cui viene visualizzato *pszTitle* . Normale Windows Visualizza tutto il testo, incluso *pszTitle*, da sinistra a destra (LTR). Per lingue come l'ebraico o l'arabo che legge da destra a sinistra (RTL), è possibile eseguire il mirroring di una finestra e visualizzare tutto il testo RTL. Se PSP_RTLREADING è impostato, *pszTitle* leggerà invece RTL in una normale finestra padre e LTR in una finestra padre con mirroring. |
| PSP_USECALLBACK | Chiama la funzione specificata dal membro *pfnCallback* durante la creazione o l'eliminazione definitiva della pagina della finestra delle proprietà definita da questa struttura. |
| PSP_USEFUSIONCONTEXT | [Versione 6,0](common-control-versions.md) e successive. Usare un contesto di attivazione. Per usare un contesto di attivazione, è necessario impostare questo flag e assegnare l'handle del contesto di attivazione a *hActCtx*. Vedere la sezione Osservazioni. |
| PSP_USEHEADERSUBTITLE | [Versione 5,80](common-control-versions.md) o successiva. Visualizza la stringa a cui fa riferimento il membro *pszHeaderSubTitle* come sottotitolo dell'area di intestazione di una pagina Wizard97. Per usare questo flag, è necessario impostare anche il flag PSH_WIZARD97 nel membro *dwFlags* della struttura [PROPSHEETHEADER](pss-propsheetheader.md) associata. Il flag PSP_USEHEADERSUBTITLE viene ignorato se è impostato PSP_HIDEHEADER. Nelle creazioni guidate di tipo Aero il titolo viene visualizzato nella parte superiore dell'area client. |
| PSP_USEHEADERTITLE | [Versione 5,80](common-control-versions.md) o successiva. Visualizza la stringa a cui fa riferimento il membro *pszHeaderTitle* come titolo nell'intestazione di una pagina interna di Wizard97. È inoltre necessario impostare il flag PSH_WIZARD97 nel membro *dwFlags* della struttura [PROPSHEETHEADER](pss-propsheetheader.md) associata. Il flag PSP_USEHEADERTITLE viene ignorato se è impostato PSP_HIDEHEADER. Questo flag non è supportato quando si utilizza la procedura guidata stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_USEHICON | USA *HICON* come icona piccola nella scheda della pagina. Questo flag non è supportato quando si utilizza la procedura guidata stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)).  |
| PSP_USEICONID | USA *pszIcon* come nome della risorsa icona da caricare e usare come icona piccola nella scheda della pagina. Questo flag non è supportato quando si utilizza la procedura guidata stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_USEREFPARENT | Mantiene il conteggio dei riferimenti specificato dal membro *pcRefParent* per la durata della pagina della finestra delle proprietà creata da questa struttura. |
| PSP_USETITLE | Usa il membro *pszTitle* come titolo della finestra di dialogo della finestra delle proprietà anziché come titolo archiviato nel modello della finestra di dialogo. Questo flag non è supportato quando si utilizza la procedura guidata stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |

*hInstance* 

Tipo: [HINSTANCE](../winprog/windows-data-types.md)

Handle per l'istanza da cui caricare un'icona o una risorsa di stringa. Se il membro *pszIcon*, *pszTitle*, *pszHeaderTitle* o *pszHeaderSubTitle* identifica una risorsa da caricare, è necessario specificare *HINSTANCE* .

*pszTemplate* 

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Modello della finestra di dialogo da utilizzare per creare la pagina. Questo membro può specificare l'identificatore di risorsa del modello o l'indirizzo di una stringa che specifica il nome del modello. Se il flag di PSP_DLGINDIRECT nel membro *dwFlags* è impostato, *pszTemplate* viene ignorato. Questo membro è dichiarato come Unione con *PreSource*.

*pResource* 

Tipo: **LPCDLGTEMPLATE**

Puntatore a un modello di finestra di dialogo in memoria. La funzione [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) presuppone che il modello non sia protetto da scrittura. Un modello di sola lettura provocherà un'eccezione in alcune versioni di Windows. Per utilizzare questo membro, è necessario impostare il flag di PSP_DLGINDIRECT nel membro *dwFlags* . Questo membro viene dichiarato come Unione con *pszTemplate*.

*hIcon* 

Tipo: [HICON](../winprog/windows-data-types.md)

Handle per l'icona da utilizzare come icona nella scheda della pagina. Se il membro *dwFlags* non include PSP_USEHICON, questo membro viene ignorato. Questo membro viene dichiarato come Unione con *pszIcon*.

*pszIcon* 

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Icona risorsa da usare come icona nella scheda della pagina. Questo membro può specificare l'identificatore della risorsa icona o l'indirizzo della stringa che specifica il nome della risorsa icona. Per utilizzare questo membro, è necessario impostare il flag di PSP_USEICONID nel membro *dwFlags* . Questo membro viene dichiarato come Unione con *HICON*.

*pszTitle* 

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Titolo della finestra di dialogo della finestra delle proprietà. Questo titolo sostituisce il titolo specificato nel modello della finestra di dialogo. Questo membro può specificare l'identificatore di una risorsa di tipo stringa o l'indirizzo di una stringa che specifica il titolo. Per utilizzare questo membro, è necessario impostare il flag di PSP_USETITLE nel membro *dwFlags* .

*pfnDlgProc* 

Tipo: **DLGPROC**

Puntatore alla routine della finestra di dialogo per la pagina. Poiché le pagine vengono create come finestre di dialogo non modali, la routine della finestra di dialogo non deve chiamare la funzione [EndDialog](/windows/win32/api/winuser/nf-winuser-enddialog) .

*lParam* 

Tipo: [lParam](../winprog/windows-data-types.md)

Quando viene creata la pagina, viene passata una copia della struttura **PROPSHEETPAGE** della pagina alla routine della finestra di dialogo con un messaggio [WM_INITDIALOG](/windows/win32/dlgbox/wm-initdialog) . Il membro *lParam* viene fornito per consentire di passare informazioni specifiche dell'applicazione alla routine della finestra di dialogo. Non ha alcun effetto sulla pagina stessa.

*pfnCallback* 

Tipo: **LPFNPSPCALLBACK**

Puntatore a una funzione di callback definita dall'applicazione che viene chiamata quando la pagina viene creata e quando sta per essere eliminata definitivamente. Per ulteriori informazioni sulla funzione di callback, vedere [funzione di callback LPFNPSPCALLBACKA](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka). Per utilizzare questo membro, è necessario impostare il flag di PSP_USECALLBACK nel membro *dwFlags* .

*pcRefParent* 

Tipo: [uint *](../winprog/windows-data-types.md)

Puntatore al valore del conteggio dei riferimenti. Per utilizzare questo membro, è necessario impostare il flag di PSP_USEREFPARENT nel membro *dwFlags* .

> [!NOTE]
> Quando viene creata una pagina della finestra delle proprietà, il valore a cui punta *pcRefParent* viene incrementato. È possibile creare una pagina della finestra delle proprietà in modo implicito impostando il flag di PSH_PROPSHEETPAGE nel membro *dwFlags* di [PROPSHEETHEADER](pss-propsheetheader.md) e chiamando la funzione [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) . È possibile eseguire questa operazione in modo esplicito tramite la funzione [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . Quando una pagina della finestra delle proprietà viene distrutta, il valore a cui fa riferimento il membro *pcRefParent* viene decrementato. Questo avviene automaticamente quando viene eliminata definitivamente la finestra delle proprietà. È possibile eliminare in modo esplicito una pagina della finestra delle proprietà utilizzando la funzione [DestroyPropertySheetPage](/windows/win32/api/prsht/nf-prsht-destroypropertysheetpage) .

*pszHeaderTitle* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

[Versione 5,80](common-control-versions.md) o successiva. Titolo dell'area di intestazione. Per utilizzare questo membro nella creazione guidata stile Wizard97, è necessario eseguire anche le operazioni seguenti:

* Impostare il flag di PSP_USEHEADERTITLE nel membro *dwFlags* .
* Impostare il flag PSH_WIZARD97 nel membro *dwFlags* della struttura [PROPSHEETHEADER](pss-propsheetheader.md) della pagina.
* Verificare che il flag di PSP_HIDEHEADER nel membro *dwFlags* non sia impostato.

*pszHeaderSubTitle* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

[Versione 5,80](common-control-versions.md) o successiva. Sottotitolo dell'area di intestazione. Per utilizzare questo membro, è necessario eseguire le operazioni seguenti:

* Impostare il flag di PSP_USEHEADERSUBTITLE nel membro *dwFlags* .
* Impostare il flag PSH_WIZARD97 nel membro *dwFlags* della struttura [PROPSHEETHEADER](pss-propsheetheader.md) della pagina.
* Verificare che il flag di PSP_HIDEHEADER nel membro *dwFlags* non sia impostato.

> [!NOTE]
> Questo membro viene ignorato quando si utilizza la procedura guidata stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md))

*hActCtx* 

Tipo: [handle](../winprog/windows-data-types.md)

[Versione 6,0](common-control-versions.md) o successiva. Handle del contesto di attivazione. Impostare questo membro sull'handle restituito quando si crea il contesto di attivazione con [CreateActCtx](/windows/win32/api/winbase/nf-winbase-createactctxa). Questo contesto verrà attivato dal sistema prima della creazione della finestra di dialogo. Non è necessario utilizzare questo membro se si utilizza un manifesto globale.

*hbmHeader* 

Tipo: [HBITMAP](../winprog/windows-data-types.md)

Questo membro viene dichiarato come Unione con *pszbmHeader*.

*pszbmHeader*

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Questo membro viene dichiarato come Unione con *hbmHeader*.

## <a name="remarks"></a>Commenti

Comctl32.dll versione 6 e successive non sono ridistribuibili. Per usare Comctl32.dll versione 6 o successiva, specificare il file con estensione dll in un manifesto. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | \[Solo app desktop di Windows Vista\]                                    |
| Server minimo supportato | \[Solo app desktop Windows Server 2003\]                              |
| Intestazione                   | Prsht. h |
| Nomi Unicode e ANSI                   | **PROPSHEETHEADERW** (Unicode) e **PROPSHEETHEADERA** (ANSI) |
