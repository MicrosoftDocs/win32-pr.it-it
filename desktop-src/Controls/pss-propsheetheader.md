---
title: Struttura PROPSHEETHEADER (Prsht.h)
description: Definisce il frame e le pagine di una finestra delle proprietà.
keywords:
- Struttura PROPSHEETHEADER Windows controlli
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
ms.openlocfilehash: 719982c1e17ab74dc5c624352625d226f8f4bef90ae84dce4f2b85d5dc2713f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085121"
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

Dimensione, in byte, di questa struttura. Il gestore della finestra delle proprietà usa questo membro per determinare la versione della **struttura PROPSHEETHEADER** in uso. Per ulteriori informazioni, vedere la sezione Osservazioni.

*dwFlags* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Flag che indicano le opzioni da utilizzare durante la creazione della pagina della finestra delle proprietà. Questo membro può essere una combinazione dei valori seguenti.

| Valore | Significato |
|-------|---------|
| PSH_DEFAULT (0x00000000) | Usa il significato predefinito per tutti i membri della struttura e crea una normale finestra delle proprietà. Questo flag ha valore zero e non viene combinato con altri flag. |
| PSH_AEROWIZARD (0x00004000) | [Versione 6.00](common-control-versions.md) e successive. Crea una finestra delle proprietà della procedura guidata che usa lo stile Aero. È PSH_WIZARD anche il flag di configurazione. È necessario usare il modello apartment a thread singolo (STA). |
| PSH_HASHELP (0x00000200) | Consente alle pagine della finestra delle proprietà di visualizzare un **pulsante ?** È anche necessario impostare il flag PSP_HASHELP nella struttura [PROPSHEETPAGE](pss-propsheetpage.md) della pagina quando viene creata la pagina. Se una delle pagine iniziali della finestra delle proprietà **abilita** un pulsante Guida, PSH_HASHELP automaticamente. Se nessuna delle pagine iniziali  abilita un pulsante Guida, è necessario impostare in modo esplicito PSH_HASHELP se si vogliono avere pulsanti della Guida in tutte le pagine che potrebbero essere aggiunte in un secondo momento. Questo flag non è supportato in combinazione con PSH_AEROWIZARD.|
| PSH_HEADER (0x00080000) | [Versione 5.80](common-control-versions.md) e successive. Indica che verrà usata una bitmap dell'intestazione con una procedura guidata97. È anche necessario impostare il flag PSH_WIZARD97. Se il flag PSH_USEHBMHEADER impostato, la bitmap dell'intestazione viene ottenuta dal *membro hbmHeader.* In caso contrario, la bitmap dell'intestazione viene ottenuta dal *membro pszbmHeader.* Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |
| PSH_HEADERBITMAP (0x08000000) | [Versione 6.00](common-control-versions.md) e successive. Il *membro pszbmHeader* specifica una bitmap visualizzata nell'area dell'intestazione. Deve essere usato in combinazione con PSH_AEROWIZARD. |
| PSH_MODELESS (0x00000400) | Fa in modo che la funzione [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) crei la finestra delle proprietà come finestra di dialogo non modale anziché come finestra di dialogo modale. Quando questo flag è impostato, [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) restituisce immediatamente dopo la creazione della finestra di dialogo e il valore restituito da [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) è l'handle della finestra della finestra di dialogo della finestra delle proprietà. Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |
| PSH_NOAPPLYNOW (0x00000080) | Rimuove il **pulsante** Applica. Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |
| PSH_NOCONTEXTHELP (0x02000000) | [Versione 5.80](common-control-versions.md) e successive. Rimuove il pulsante Guida sensibile al contesto ("?"), che in genere è presente nella barra del titolo delle finestre delle proprietà. Questo flag non è valido per le procedure guidate. Per [informazioni su come](property-sheets.md) rimuovere il pulsante  Guida della barra del titolo per le versioni precedenti dei controlli comuni, vedere Informazioni sulle finestre delle proprietà. Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |
| PSH_NOMARGIN (0x10000000) | [Versione 6.00](common-control-versions.md) o successiva. Specifica che non viene inserito alcun margine tra la pagina e il frame. Deve essere usato in combinazione con PSH_AEROWIZARD. |
| PSH_PROPSHEETPAGE (0x00000008) | Usa il *membro ppsp* e ignora il membro *phpage* durante la creazione delle pagine per la finestra delle proprietà. |
| PSH_PROPTITLE (0x00000001) | Indica che *pszCaption* è il nome dell'elemento per cui vengono visualizzate le proprietà. Windows esegue una regolazione dipendente dalla versione e dalla lingua per la didascalia. Ad esempio, in inglese, la frase "Properties for" viene anteposta a una *pszCaption* non vuota (e se *pszCaption* produce una didascalia vuota, il titolo è semplicemente "Properties"). Se questo flag viene omesso, pszCaption viene usato senza modifiche.  |
| PSH_RESIZABLE (0x04000000) | Consente il ridimensionamento della procedura guidata da parte dell'utente. I pulsanti Ingrandisci e Riduci a icona vengono visualizzati nel frame della procedura guidata e il frame è ridimensionabile. Per usare questo flag, è necessario impostare anche PSH_AEROWIZARD. |
| PSH_RTLREADING (0x00000800) | Imposta la finestra delle proprietà o la finestra della procedura guidata sull'ordine di lettura da destra a sinistra (RTL), appropriato per lingue come l'ebraico e l'arabo. Se questo flag non viene specificato, per impostazione predefinita le finestre delle finestre delle proprietà sono in ordine di lettura da sinistra a destra e le finestre della procedura guidata corrispondono all'ordine di lettura della pagina corrente. |
| PSH_STRETCHWATERMARK (0x00040000) | Estende il limite nelle procedure guidate in stile Wizard97. Questo flag non è supportato in combinazione con PSH_AEROWIZARD. Questo flag di stile è incluso solo per garantire la compatibilità con le versioni precedenti per determinate applicazioni. Non è consigliabile usarlo ed è supportato solo dalle versioni dei controlli comuni 4.0 e 4.01. Con i controlli comuni versione 5.80 e successive, questo flag viene ignorato. |
| PSH_USECALLBACK (0x00000100) | Chiama la funzione specificata dal *parametro pfnCallback* quando si verificano determinati eventi. Per altre informazioni, vedere la descrizione della funzione di callback [PFNPROPSHEETCALLBACK.](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) |
| PSH_USEHBMHEADER (0x00100000) | [Versione 5.80](common-control-versions.md). Ottiene la bitmap dell'intestazione *dal membro hbmHeader* anziché dal *membro pszbmHeader.* È anche necessario impostare il flag PSH_AEROWIZARD o il flag PSH_WIZARD97 insieme al flag PSH_HEADER. |
| PSH_USEHBMWATERMARK (0x00010000) | [Versione 5.80](common-control-versions.md). Ottiene la bitmap del limite dal *membro hbmWatermark* anziché dal *membro pszbmWatermark.* È anche necessario impostare PSH_WIZARD97 e PSH_WATERMARK. Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |
| PSH_USEHICON (0x00000002) | Usa *hIcon* come icona piccola nella barra del titolo della finestra di dialogo della finestra di dialogo delle proprietà. |
| PSH_USEHPLWATERMARK (0x00020000) | [Versione 5.80](common-control-versions.md). Usa la **struttura HPALETTE** a cui punta il membro *hplWatermark* anziché il riquadro predefinito per disegnare la bitmap del limite e/o la bitmap dell'intestazione per una procedura guidata Wizard97. È anche necessario impostare PSH_WIZARD97 e PSH_WATERMARK o PSH_HEADER. Questo flag non è supportato in combinazione con PSH_AEROWIZARD.  |
| PSH_USEICONID (0x00000004) | Usa *pszIcon* come nome della risorsa icona da caricare e usare come icona piccola nella barra del titolo della finestra di dialogo della finestra di dialogo delle proprietà. |
| PSH_USEPAGELANG (0x00200000) | [Versione 5.80](common-control-versions.md). Specifica che la lingua per la finestra delle proprietà verrà prelevata dalla risorsa della prima pagina. Tale pagina deve essere specificata dall'identificatore di risorsa. |
| PSH_USEPSTARTPAGE (0x00000040) | Usa il *membro pStartPage* anziché il membro *nStartPage* quando si visualizza la pagina iniziale della finestra delle proprietà. |
| PSH_WATERMARK (0x00008000) | [Versione 5.80](common-control-versions.md). Specifica che una bitmap del limite verrà usata con una procedura guidata Wizard97 nelle pagine con lo stile PSP_HIDEHEADER predefinito. È anche necessario impostare il flag PSH_WIZARD97. La bitmap del limite viene ottenuta dal *membro pszbmWatermark,* a meno PSH_USEHBMWATERMARK impostato. In tal caso, la bitmap dell'intestazione viene ottenuta dal *membro hbmWatermark.* Questo flag non è supportato in combinazione con PSH_AEROWIZARD.  |
| PSH_WIZARD (0x00000020) | Crea una finestra delle proprietà della procedura guidata. Quando si PSH_AEROWIZARD, è necessario impostare anche questo flag. |
| PSH_WIZARD97 (0x01000000) | [Versione 5.80](common-control-versions.md). Crea una finestra delle proprietà in stile Wizard97, che supporta le bitmap nell'intestazione delle pagine interne e sul lato sinistro delle pagine esterne. Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |
| PSH_WIZARDCONTEXTHELP (0x00001000) | Aggiunge un pulsante della **Guida** sensibile al contesto ("?"), che in genere è assente dalla barra del titolo di una procedura guidata. Questo flag non è valido per le normali finestre delle proprietà. Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |
| PSH_WIZARDHASFINISH (0x00000010)  | Visualizza sempre il **pulsante** Fine nella procedura guidata. È anche necessario impostare PSH_WIZARD, PSH_WIZARD97 o PSH_AEROWIZARD. |
| PSH_WIZARD_LITE (0x00400000) | [Versione 5.80](common-control-versions.md). Usa lo stile Wizard-lite. Questo stile è simile all'aspetto PSH_WIZARD97, ma viene implementato in modo analogo PSH_WIZARD. Esistono poche restrizioni sulla formattazione delle pagine. Ad esempio, non sono presenti bordi applicati e lo stile PSH_WIZARD_LITE non disegna le bitmap del limite e dell'intestazione come in Wizard97. Questo flag non è supportato in combinazione con PSH_AEROWIZARD. |

*hwndParent* 

Tipo: [HWND](../winprog/windows-data-types.md)

Handle per la finestra proprietaria della finestra delle proprietà.

*hInstance* 

Tipo: [HINSTANCE](../winprog/windows-data-types.md)

Handle per l'istanza da cui caricare l'icona, la risorsa della stringa del titolo, il nome della pagina iniziale, la bitmap dell'intestazione o la filigrana. Se il membro *pszIcon*, *pszCaption*, *pStartPage*, *pszbmHeader* o *pszbmWatermark* identifica una risorsa da caricare, è necessario specificare questo membro.

*hIcon* 

Tipo: [HICON](../winprog/windows-data-types.md)

Handle per l'icona da utilizzare come icona piccola nella barra del titolo della finestra di dialogo della finestra di dialogo delle proprietà. Questo membro viene usato se *il membro dwFlags* include PSH_USEHICON. Questo membro viene dichiarato come unione con *pszIcon*.

*pszIcon* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

Risorsa icona da usare come icona piccola nella barra del titolo della finestra di dialogo della finestra di dialogo delle proprietà. Questo membro viene usato se *il membro dwFlags* include PSH_USEICONID. Questo membro può specificare l'identificatore della risorsa icona o l'indirizzo della stringa che specifica il nome della risorsa icona. In entrambi i casi, l'icona viene caricata dall'istanza fornita dal *membro hInstance.* Questo membro viene dichiarato come unione con *hIcon*.

*pszCaption* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

Titolo della finestra di dialogo della finestra di dialogo delle proprietà. Questo membro può specificare l'identificatore di una risorsa stringa (caricata dall'istanza specificata dal membro *hInstance)* o l'indirizzo di una stringa che specifica il titolo. Se il *membro dwFlags* include PSH_PROPTITLE, la stringa **Properties per** viene inserita all'inizio del titolo. Questo campo viene ignorato per le procedure guidate wizard97. Per le procedure guidate di Aero, la sola stringa viene usata per la didascalia, indipendentemente dal fatto che il flag PSH_PROPTITLE impostato.

*nPages* 

Tipo: [UINT](../winprog/windows-data-types.md)

Numero di pagine della finestra delle proprietà fornite nella matrice *ppsp* *o phpage.*

*nStartPage* 

Tipo: [UINT](../winprog/windows-data-types.md)

Indice in base zero della pagina iniziale visualizzata quando viene creata la finestra di dialogo della finestra delle proprietà. Questo membro viene usato se il *membro dwFlags* non include il flag PSH_USEPSTARTPAGE. Questo membro viene dichiarato come unione con *pStartPage*.

*pStartPage* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

Nome della pagina iniziale visualizzata quando viene creata la finestra di dialogo della finestra delle proprietà. Questo membro viene usato se il *membro dwFlags* include PSH_USESTARTPAGE flag. Questo membro può specificare l'identificatore di una risorsa stringa (caricata dall'istanza specificata dal membro *hInstance)* o l'indirizzo di una stringa che specifica il nome. Il nome della pagina iniziale viene abbinato alle didascalie delle pagine. Questo membro viene dichiarato come unione con *nStartPage*.

*ppsp* 

Tipo: **LPCPROPSHEETPAGE**

Puntatore a una matrice di [strutture PROPSHEETPAGE](pss-propsheetpage.md) che definiscono le pagine nella finestra delle proprietà. Se il *membro dwFlags* non include PSH_PROPSHEETPAGE, questo membro viene ignorato. Si noti che la **struttura PROPSHEETPAGE** ha dimensioni variabili. Le applicazioni che analizzano la matrice a cui *punta ppsp* devono prendere in considerazione le dimensioni di ogni pagina. Questo membro viene dichiarato come unione con *phpage*.

*phpage* 

Tipo: **HPROPSHEETPAGE \***

Puntatore a una matrice di handle alle pagine della finestra delle proprietà. Questo membro viene usato se *il membro dwFlags* non include PSH_PROPSHEETPAGE. Ogni handle deve essere stato creato da una chiamata precedente alla [funzione CreatePropertySheetPage.](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) Quando la [funzione PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) viene restituita, tutti gli handle HPROPSHEETPAGE nella matrice *phpage* verranno distrutti. Questo membro viene dichiarato come unione con *ppsp*.

*pfnCallback* 

Tipo: **PFNPROPSHEETCALLBACK**

Puntatore a una funzione di callback definita dall'applicazione che viene chiamata quando si verificano determinati eventi. Per altre informazioni sulla funzione di callback, vedere la descrizione della funzione di callback [PFNPROPSHEETCALLBACK.](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) Se il *membro dwFlags* non include PSH_USECALLBACK, questo membro viene ignorato.

*hbmWatermark* 

Tipo: [HBITMAP](../winprog/windows-data-types.md)

[Versione 5.80](common-control-versions.md) o successiva. Handle per la bitmap del limite. Se il *membro dwFlags* non include PSH_USEHBMWATERMARK, questo membro viene ignorato.

*pszbmWatermark* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

[Versione 5.80](common-control-versions.md) o successiva. Risorsa bitmap da usare come limite. Questo membro può specificare l'identificatore della risorsa bitmap o l'indirizzo della stringa che specifica il nome della risorsa bitmap. Se il *membro dwFlags* include PSH_USEHBMWATERMARK, questo membro viene ignorato.

*hplWatermark*

Tipo: [HPALETTE](../winprog/windows-data-types.md)

[Versione 5.80](common-control-versions.md) o successiva. **Struttura HPALETTE** usata per disegnare la bitmap del limite e/o la bitmap dell'intestazione. Se il *membro dwFlags* non include PSH_USEHPLWATERMARK, questo membro viene ignorato.

*hbmHeader*

Tipo: [HBITMAP](../winprog/windows-data-types.md)

[Versione 5.80](common-control-versions.md) o successiva. Handle per la bitmap dell'intestazione. Se il *membro dwFlags* non include PSH_USEHBMHEADER, questo membro viene ignorato.

*pszbmHeader*

Tipo: [LPCSTR](../winprog/windows-data-types.md)

[Versione 5.80](common-control-versions.md) o successiva. Risorsa bitmap da usare come intestazione. Questo membro può specificare l'identificatore della risorsa bitmap o l'indirizzo della stringa che specifica il nome della risorsa bitmap. Se il *membro dwFlags* include PSH_USEHBMHEADER, questo membro viene ignorato.

## <a name="remarks"></a>Commenti

Se l'utente sceglie un'impostazione, ad esempio Caratteri grandi, che ingrandisce la finestra di dialogo, verrà ingrandita anche la filigrana disegnata nelle pagine iniziale e finale. Le dimensioni e la posizione della bitmap originale rimarranno invariate. L'area aggiuntiva verrà riempita con il colore del pixel nell'angolo superiore sinistro della bitmap.

Gli PSH_WIZARD, PSH_WIZARD97 e PSH_WIZARD_LITE sono reciprocamente incompatibili. È necessario impostare solo uno di questi flag di stile. PSH_AEROWIZARD deve essere combinato con PSH_WIZARD.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows Solo \[ app desktop di Vista\]                                    |
| Server minimo supportato | Windows Solo app desktop server 2003 \[\]                              |
| Intestazione                   | Prsht.h |
| Nomi Unicode e ANSI                   | **PROPSHEETHEADERW** (Unicode) e **PROPSHEETHEADERA** (ANSI) |
