---
description: Quando l'utente fa clic con il pulsante destro del mouse su un membro di un tipo di file per visualizzare la finestra delle proprietà Proprietà, la shell chiama i gestori della finestra delle proprietà registrati per il tipo di file. Ogni gestore può aggiungere una pagina personalizzata alla finestra delle proprietà predefinita.
title: Come registrare e implementare un gestore della finestra delle proprietà per un tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce0451071ba1f454ffae9ca1444f30428909946442f5aead853e74095d0c0c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049807"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a>Come registrare e implementare un gestore della finestra delle proprietà per un tipo di file

Quando l'utente fa clic con il pulsante destro del mouse su un membro di un tipo di file per visualizzare la finestra delle proprietà Proprietà, la shell chiama i gestori della finestra delle proprietà registrati per il tipo di file. Ogni gestore può aggiungere una pagina personalizzata alla finestra delle proprietà predefinita.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   Shell

### <a name="prerequisites"></a>Prerequisiti

-   Conoscenza dei menu di scelta rapida

## <a name="instructions"></a>Istruzioni

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a>Passaggio 1: Registrazione di un gestore della finestra delle proprietà per un tipo di file

Oltre alla normale registrazione Component Object Model (COM), aggiungere una sottochiave **PropertySheetHandlers** alla sottochiave **shellex** della chiave ProgID dell'applicazione associata al tipo di file. Creare una sottochiave **di PropertySheetHandlers** con il nome del gestore e impostare il valore predefinito sul formato stringa del GUID dell'identificatore di classe (CLSID) del gestore della finestra delle proprietà.

Per aggiungere più di una pagina alla finestra delle proprietà, registrare un gestore per ogni pagina. Il numero massimo di pagine che una finestra delle proprietà può supportare è 32. Per registrare più gestori, creare una chiave sotto la **chiave shellex** per ogni gestore, con il valore predefinito impostato sul GUID CLSID del gestore. Non è necessario creare un oggetto distinto per ogni gestore, il che significa che più gestori possono avere tutti lo stesso valore GUID. Le pagine verranno visualizzate nell'ordine in cui le relative chiavi sono elencate in **shellex**.

Nell'esempio seguente viene illustrata una voce del Registro di sistema che abilita due gestori dell'estensione della finestra delle proprietà per un tipo di file myp di esempio. In questo esempio viene usato un oggetto separato per ogni pagina, ma è anche possibile usare un singolo oggetto per entrambi.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {Page 1 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet1.dll
            ThreadingModel = Apartment
      {Page 2 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet2.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         PropertySheetHandlers
            MyPropSheet1
               (Default) = {Page1 Property Sheet Handler CLSID GUID}
            MyPropSheet2
               (Default) = {Page2 Property Sheet Handler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a>Passaggio 2: Implementazione di un gestore della finestra delle proprietà per un tipo di file

Oltre all'implementazione generale illustrata [in](propsheet-handlers.md)Funzionamento dei gestori della finestra delle proprietà, un gestore della finestra delle proprietà per un tipo di file deve avere anche un'implementazione appropriata dell'interfaccia [**IShellPropSheetExt.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) Solo il [**metodo IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) richiede un'implementazione nontoken. La shell non chiama [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).

Il [**metodo IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) consente a un gestore della finestra delle proprietà di aggiungere una pagina a una finestra delle proprietà. Il metodo ha due parametri di input. Il primo, *lpfnAddPage*, è un puntatore a una funzione di callback [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) usata per fornire alla shell le informazioni necessarie per aggiungere la pagina alla finestra delle proprietà. Il secondo, *lParam,* è un valore definito dalla shell che non viene elaborato dal gestore. Viene semplicemente passato alla shell quando viene chiamata la funzione di callback.

La procedura generale per l'implementazione [**di AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) è la seguente.

**Implementazione del metodo AddPages**

1.  Assegnare i valori appropriati ai membri di una [**struttura PROPSHEETPAGE.**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) In particolare:
    -   Assegnare la variabile che contiene il conteggio dei riferimenti del gestore al **membro pcRefParent.** In questo modo si impedisce che l'oggetto gestore venga scaricato mentre la finestra delle proprietà è ancora visualizzata.
    -   È anche possibile implementare una funzione di callback [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) e assegnare il relativo puntatore a un **membro pfnCallback.** Questa funzione viene chiamata quando la pagina viene creata e quando sta per essere distrutta.
2.  Creare l'handle HPAGE della pagina passando la [**struttura PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) alla [**funzione CreatePropertySheetPage.**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea)
3.  Chiamare la funzione a cui punta *lpfnAddPage*. Impostare il primo parametro sull'handle HPAGE creato nel passaggio precedente. Impostare il secondo parametro sul *valore lParam* passato ad [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) dalla shell.
4.  Tutti i messaggi associati alla pagina verranno passati alla routine della finestra di dialogo assegnata al membro **pfnDlgProc** della [**struttura PROPSHEETPAGE.**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3)
5.  Se è stata assegnata una funzione di callback [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) a **pfnCallback,** questa verrà chiamata quando la pagina sta per essere distrutta. Il gestore può quindi eseguire le operazioni di pulizia necessarie, ad esempio il rilascio di tutti i riferimenti in esso presenti.

L'esempio di codice seguente illustra una semplice [**implementazione di AddPages.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)


```C++
STDMETHODIMP CShellPropSheetExt::AddPages(LPFNADDPROPSHEETPAGE, lpfnAddPage, LPARAM lParam)
{
    PROPSHEETPAGE  psp;
    HPROPSHEETPAGE hPage;

    psp.dwSize        = sizeof(psp);
    psp.dwFlags       = PSP_USEREFPARENT | PSP_USETITLE | PSP_USECALLBACK;
    psp.hInstance     = g_hInst;
    psp.pszTemplate   = MAKEINTRESOURCE(IDD_PAGEDLG);
    psp.hIcon         = 0;
    psp.pszTitle      = TEXT("Extension Page");
    psp.pfnDlgProc    = (DLGPROC)PageDlgProc;
    psp.pcRefParent   = &g_DllRefCount;
    psp.pfnCallback   = PageCallbackProc;
    psp.lParam        = (LPARAM)this;

    hPage = CreatePropertySheetPage(&psp);
            
    if(hPage) 
    {
        if(lpfnAddPage(hPage, lParam))
        {
            this->AddRef();
            return S_OK;
        }
        else
        {
            DestroyPropertySheetPage(hPage);
        }
    }
    else
    {
        return E_OUTOFMEMORY;
    }
    return E_FAIL;
}
```



La **variabile \_ g hInst** è l'handle di istanza per la DLL e IDD PAGEDLG è l'ID risorsa del modello di finestra \_ di dialogo della pagina. La **funzione PageDlgProc** è la procedura della finestra di dialogo che gestisce i messaggi della pagina. La **variabile \_ DllRefCount** g contiene il conteggio dei riferimenti dell'oggetto. Il [**metodo AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) chiama [**AddRef per**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementare il conteggio. Tuttavia, il conteggio dei riferimenti viene rilasciato dalla funzione di callback **PageCallbackProc** quando la pagina sta per essere distrutta.

## <a name="remarks"></a>Commenti

Per una descrizione generale di come registrare i gestori di estensioni della shell, vedere [Creazione di gestori di estensioni della shell.](handlers.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
