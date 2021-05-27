---
title: Struttura PROPSHEETPAGE (Prsht.h)
description: Definisce una pagina in una finestra delle proprietà.
keywords:
- Controlli Windows della struttura PROPSHEETPAGE
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
ms.openlocfilehash: 78e1d1e4e6b4b2067083443bdb5dc4db5df59558
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550346"
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

Dimensioni, in byte, della struttura .

*dwFlags* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Flag che indicano le opzioni da utilizzare durante la creazione della pagina della finestra delle proprietà. Questo membro può essere una combinazione dei valori seguenti.

| Valore | Significato |
|-------|---------|
| PSP_DEFAULT | Usa il significato predefinito per tutti i membri della struttura. Questo flag non è supportato quando si usa la procedura guidata in stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_DLGINDIRECT | Crea la pagina dal modello di finestra di dialogo in memoria a cui punta *il membro pResource.* La [funzione PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) presuppone che il modello in memoria non sia protetto da scrittura. Un modello di sola lettura causerà un'eccezione in alcune versioni di Windows. |
| PSP_HASHELP | Abilita il pulsante ? **della finestra** delle proprietà quando la pagina è attiva. Questo flag non è supportato quando si usa la procedura guidata in stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_HIDEHEADER | [Versione 5.80](common-control-versions.md) e successive. Fa sì che la finestra delle proprietà della procedura guidata nascondi l'area dell'intestazione quando viene selezionata la pagina. Se è stata specificata una filigrana, verrà disegnata sul lato sinistro della pagina. Questo flag deve essere impostato per le pagine di benvenuto e di completamento e omesso per le pagine interne. Questo flag non è supportato quando si usa la procedura guidata in stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_PREMATURE | [Versione 4.71](common-control-versions.md) o successiva. Determina la creazione della pagina quando viene creata la finestra delle proprietà. Se questo flag non viene specificato, la pagina non verrà creata fino a quando non viene selezionata la prima volta. Questo flag non è supportato quando si usa la procedura guidata in stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_RTLREADING | Inverte la direzione di *visualizzazione di pszTitle.* Le finestre normali visualizzano tutto il testo, *incluso pszTitle*, da sinistra a destra (LTR). Per lingue come l'ebraico o l'arabo che leggono da destra a sinistra (RTL), è possibile eseguire il mirroring di una finestra e tutto il testo verrà visualizzato RTL. Se PSP_RTLREADING è impostato, *pszTitle* leggerà invece RTL in una finestra padre normale e la durata (LTR) in una finestra padre con mirroring. |
| PSP_USECALLBACK | Chiama la funzione specificata dal membro *pfnCallback* durante la creazione o l'eliminazione della pagina della finestra delle proprietà definita da questa struttura. |
| PSP_USEFUSIONCONTEXT | [Versione 6.0](common-control-versions.md) e successive. Usare un contesto di attivazione. Per usare un contesto di attivazione, è necessario impostare questo flag e assegnare l'handle del contesto di attivazione *a hActCtx*. Vedere la sezione Osservazioni. |
| PSP_USEHEADERSUBTITLE | [Versione 5.80](common-control-versions.md) o successiva. Visualizza la stringa a cui punta il *membro pszHeaderSubTitle* come sottotitolo dell'area di intestazione di una pagina Wizard97. Per usare questo flag, è necessario impostare anche il flag PSH_WIZARD97 nel membro *dwFlags* della [struttura PROPSHEETHEADER](pss-propsheetheader.md) associata. Il flag PSP_USEHEADERSUBTITLE viene ignorato se PSP_HIDEHEADER è impostato. Nelle procedure guidate in stile Aereo il titolo viene visualizzato nella parte superiore dell'area client. |
| PSP_USEHEADERTITLE | [Versione 5.80](common-control-versions.md) o successiva. Visualizza la stringa a cui punta il *membro pszHeaderTitle* come titolo nell'intestazione di una pagina interna di Wizard97. È inoltre necessario impostare il flag PSH_WIZARD97 nel *membro dwFlags* della [struttura PROPSHEETHEADER](pss-propsheetheader.md) associata. Il flag PSP_USEHEADERTITLE viene ignorato se PSP_HIDEHEADER è impostato. Questo flag non è supportato quando si usa la procedura guidata in stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_USEHICON | Usa *hIcon* come icona piccola nella scheda della pagina. Questo flag non è supportato quando si usa la procedura guidata in stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)).  |
| PSP_USEICONID | Usa *pszIcon* come nome della risorsa icona da caricare e usare come icona piccola nella scheda della pagina. Questo flag non è supportato quando si usa la procedura guidata in stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_USEREFPARENT | Mantiene il conteggio dei riferimenti specificato dal *membro pcRefParent* per la durata della pagina della finestra delle proprietà creata da questa struttura. |
| PSP_USETITLE | Usa il *membro pszTitle* come titolo della finestra di dialogo della finestra delle proprietà anziché il titolo archiviato nel modello della finestra di dialogo. Questo flag non è supportato quando si usa la procedura guidata in stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |

*hInstance* 

Tipo: [HINSTANCE](../winprog/windows-data-types.md)

Handle all'istanza da cui caricare un'icona o una risorsa stringa. Se il membro *pszIcon*, *pszTitle*, *pszHeaderTitle* o *pszHeaderSubTitle* identifica una risorsa da caricare, è necessario specificare *hInstance.*

*pszTemplate* 

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Modello di finestra di dialogo da utilizzare per creare la pagina. Questo membro può specificare l'identificatore di risorsa del modello o l'indirizzo di una stringa che specifica il nome del modello. Se il flag PSP_DLGINDIRECT nel membro *dwFlags* è impostato, *pszTemplate* viene ignorato. Questo membro viene dichiarato come unione con *pResource*.

*pResource* 

Tipo: **LPCDLGTEMPLATE**

Puntatore a un modello di finestra di dialogo in memoria. La [funzione PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) presuppone che il modello non sia protetto da scrittura. Un modello di sola lettura causerà un'eccezione in alcune versioni di Windows. Per usare questo membro, è necessario impostare il flag PSP_DLGINDIRECT nel *membro dwFlags.* Questo membro viene dichiarato come unione con *pszTemplate*.

*hIcon* 

Tipo: [HICON](../winprog/windows-data-types.md)

Handle per l'icona da usare come icona nella scheda della pagina. Se il *membro dwFlags* non include PSP_USEHICON, questo membro viene ignorato. Questo membro viene dichiarato come unione con *pszIcon*.

*pszIcon* 

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Risorsa icona da usare come icona nella scheda della pagina. Questo membro può specificare l'identificatore della risorsa icona o l'indirizzo della stringa che specifica il nome della risorsa icona. Per usare questo membro, è necessario impostare il flag PSP_USEICONID nel *membro dwFlags.* Questo membro viene dichiarato come unione con *hIcon*.

*pszTitle* 

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Titolo della finestra di dialogo della finestra delle proprietà. Questo titolo sostituisce il titolo specificato nel modello di finestra di dialogo. Questo membro può specificare l'identificatore di una risorsa stringa o l'indirizzo di una stringa che specifica il titolo. Per usare questo membro, è necessario impostare il flag PSP_USETITLE nel *membro dwFlags.*

*pfnDlgProc* 

Tipo: **DLGPROC**

Puntatore alla procedura della finestra di dialogo per la pagina. Poiché le pagine vengono create come finestre di dialogo non modali, la routine della finestra di dialogo non deve chiamare la [funzione EndDialog.](/windows/win32/api/winuser/nf-winuser-enddialog)

*lParam* 

Tipo: [LPARAM](../winprog/windows-data-types.md)

Quando la pagina viene creata, una copia della struttura **PROPSHEETPAGE** della pagina viene passata alla routine della finestra di dialogo con un WM_INITDIALOG [messaggio.](../dlgbox/wm-initdialog.md) Il *membro lParam* viene fornito per consentire di passare informazioni specifiche dell'applicazione alla procedura della finestra di dialogo. Non ha alcun effetto sulla pagina stessa.

*pfnCallback* 

Tipo: **LPFNPSPCALLBACK**

Puntatore a una funzione di callback definita dall'applicazione che viene chiamata quando viene creata la pagina e quando sta per essere distrutta. Per altre informazioni sulla funzione di callback, vedere [Funzione di callback LPFNPSPCALLBACKA](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka). Per usare questo membro, è necessario impostare il flag PSP_USECALLBACK nel membro *dwFlags.*

*pcRefParent* 

Tipo: [UINT*](../winprog/windows-data-types.md)

Puntatore al valore del conteggio dei riferimenti. Per usare questo membro, è necessario impostare il flag PSP_USEREFPARENT nel membro *dwFlags.*

> [!NOTE]
> Quando viene creata una pagina della finestra delle proprietà, il valore a cui punta *pcRefParent* viene incrementato. Per creare una pagina della finestra delle proprietà in modo implicito, impostare il flag PSH_PROPSHEETPAGE nel membro *dwFlags* di [PROPSHEETHEADER](pss-propsheetheader.md) e chiamare la [funzione PropertySheet.](/windows/win32/api/prsht/nf-prsht-propertysheeta) È possibile eseguire questa operazione in modo esplicito usando [la funzione CreatePropertySheetPage.](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) Quando una pagina della finestra delle proprietà viene distrutta, il valore a cui punta il *membro pcRefParent* viene decrementato. Questa operazione viene eseguita automaticamente quando la finestra delle proprietà viene distrutta. È possibile eliminare in modo esplicito una pagina della finestra delle proprietà usando la [funzione DestroyPropertySheetPage.](/windows/win32/api/prsht/nf-prsht-destroypropertysheetpage)

*pszHeaderTitle* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

[Versione 5.80](common-control-versions.md) o successiva. Titolo dell'area dell'intestazione. Per usare questo membro nella procedura guidata di tipo Wizard97, è necessario eseguire anche le operazioni seguenti:

* Impostare il PSP_USEHEADERTITLE flag nel *membro dwFlags.*
* Impostare il PSH_WIZARD97 flag nel *membro dwFlags* della struttura [PROPSHEETHEADER della](pss-propsheetheader.md) pagina.
* Assicurarsi che il flag PSP_HIDEHEADER nel *membro dwFlags* non sia impostato.

*pszHeaderSubTitle* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

[Versione 5.80](common-control-versions.md) o successiva. Sottotitolo dell'area dell'intestazione. Per usare questo membro, è necessario eseguire le operazioni seguenti:

* Impostare il PSP_USEHEADERSUBTITLE flag nel *membro dwFlags.*
* Impostare il PSH_WIZARD97 flag nel *membro dwFlags* della struttura [PROPSHEETHEADER della](pss-propsheetheader.md) pagina.
* Assicurarsi che il flag PSP_HIDEHEADER nel *membro dwFlags* non sia impostato.

> [!NOTE]
> Questo membro viene ignorato quando si usa la procedura guidata stile Aero ([PSH_AEROWIZARD](pss-propsheetheader.md))

*hActCtx* 

Tipo: [HANDLE](../winprog/windows-data-types.md)

[Versione 6.0](common-control-versions.md) o successiva. Handle del contesto di attivazione. Impostare questo membro sull'handle restituito quando si crea il contesto di attivazione [con CreateActCtx](/windows/win32/api/winbase/nf-winbase-createactctxa). Il sistema attiverà questo contesto prima di creare la finestra di dialogo. Non è necessario usare questo membro se si usa un manifesto globale.

*hbmHeader* 

Tipo: [HBITMAP](../winprog/windows-data-types.md)

Questo membro viene dichiarato come unione con *pszbmHeader*.

*pszbmHeader*

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Questo membro viene dichiarato come unione con *hbmHeader*.

## <a name="remarks"></a>Commenti

Comctl32.dll versione 6 e successive non sono ridistribuibili. Per usare Comctl32.dll versione 6 o successiva, specificare il file DLL in un manifesto. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Solo app desktop di Windows Vista \[\]                                    |
| Server minimo supportato | Solo app desktop di Windows Server 2003 \[\]                              |
| Intestazione                   | Prsht.h |
| Nomi Unicode e ANSI                   | **PROPSHEETHEADERW** (Unicode) e **PROPSHEETHEADERA** (ANSI) |