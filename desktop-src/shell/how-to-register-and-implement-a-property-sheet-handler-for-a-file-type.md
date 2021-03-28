---
description: Quando l'utente fa clic con il pulsante destro del mouse su un membro di un tipo di file per visualizzare la finestra delle proprietà delle proprietà, la shell chiama i gestori della finestra delle proprietà registrati per il tipo di file. Ogni gestore può aggiungere una pagina personalizzata alla finestra delle proprietà predefinita.
title: Come registrare e implementare un gestore della finestra delle proprietà per un tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cf54886f7819fa910da23393c6db488ddfee72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994664"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a>Come registrare e implementare un gestore della finestra delle proprietà per un tipo di file

Quando l'utente fa clic con il pulsante destro del mouse su un membro di un tipo di file per visualizzare la finestra delle proprietà delle proprietà, la shell chiama i gestori della finestra delle proprietà registrati per il tipo di file. Ogni gestore può aggiungere una pagina personalizzata alla finestra delle proprietà predefinita.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   Shell

### <a name="prerequisites"></a>Prerequisiti

-   Conoscenza dei menu di scelta rapida

## <a name="instructions"></a>Istruzioni

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a>Passaggio 1: registrazione di un gestore della finestra delle proprietà per un tipo di file

Oltre alla normale registrazione di Component Object Model (COM), aggiungere una sottochiave **PropertySheetHandlers** alla sottochiave **ShellEx** della chiave ProgID dell'applicazione associata al tipo di file. Creare una sottochiave di **PropertySheetHandlers** con il nome del gestore e impostare il valore predefinito sul formato stringa del GUID dell'identificatore di classe (CLSID) del gestore della finestra delle proprietà.

Per aggiungere più di una pagina alla finestra delle proprietà, registrare un gestore per ogni pagina. Il numero massimo di pagine che una finestra delle proprietà può supportare è 32. Per registrare più gestori, creare una chiave sotto la chiave **ShellEx** per ogni gestore, con il valore predefinito impostato sul GUID del gestore CLSID. Non è necessario creare un oggetto distinto per ogni gestore, il che significa che più gestori possono avere lo stesso valore GUID. Le pagine verranno visualizzate nell'ordine in cui le chiavi sono elencate in **ShellEx**.

Nell'esempio seguente viene illustrata una voce del registro di sistema che consente due gestori di estensioni della finestra delle proprietà per un tipo di file con estensione MYP. In questo esempio viene usato un oggetto separato per ogni pagina, ma è anche possibile usare un singolo oggetto per entrambi.

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

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a>Passaggio 2: implementazione di un gestore della finestra delle proprietà per un tipo di file

Oltre all'implementazione generale illustrata nel funzionamento dei [gestori della finestra delle proprietà](propsheet-handlers.md), un gestore della finestra delle proprietà per un tipo di file deve avere anche un'implementazione appropriata dell'interfaccia [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . Solo il metodo [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) richiede un'implementazione non token. La shell non chiama [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).

Il metodo [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) consente a un gestore della finestra delle proprietà di aggiungere una pagina a una finestra delle proprietà. Il metodo ha due parametri di input. Il primo, *lpfnAddPage*, è un puntatore a una funzione di callback [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) utilizzata per fornire la shell con le informazioni necessarie per aggiungere la pagina alla finestra delle proprietà. Il secondo *lParam* è un valore definito dalla shell che non viene elaborato dal gestore. Viene semplicemente passata di nuovo alla shell quando viene chiamata la funzione di callback.

Di seguito è riportata la procedura generale per l'implementazione di [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) .

**Implementazione del metodo AddPages**

1.  Assegnare i valori appropriati ai membri di una struttura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) . In particolare:
    -   Assegnare la variabile che include il conteggio dei riferimenti del gestore al membro **pcRefParent** . Questa procedura impedisce che l'oggetto gestore venga scaricato mentre è ancora in corso la visualizzazione della finestra delle proprietà.
    -   È anche possibile implementare una funzione di callback [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) e assegnare il relativo puntatore a un membro **pfnCallback** . Questa funzione viene chiamata quando la pagina viene creata e quando sta per essere eliminata definitivamente.
2.  Creare l'handle HPAGE della pagina passando la struttura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) alla funzione [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) .
3.  Chiamare la funzione a cui punta *lpfnAddPage*. Impostare il primo parametro sull'handle HPAGE creato nel passaggio precedente. Impostare il secondo parametro sul valore *lParam* passato a [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) dalla Shell.
4.  Tutti i messaggi associati alla pagina verranno passati alla routine della finestra di dialogo assegnata al membro **pfnDlgProc** della struttura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .
5.  Se è stata assegnata una funzione di callback [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) a **pfnCallback**, questa verrà chiamata quando la pagina sta per essere eliminata definitivamente. Il gestore può quindi eseguire le operazioni di pulizia necessarie, ad esempio il rilascio di tutti i riferimenti che possiede.

Nell'esempio di codice seguente viene illustrata un'implementazione semplice di [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) .


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



La variabile **g \_ hInst** è l'handle dell'istanza per la dll e IDD \_ PAGEDLG è l'ID risorsa del modello di finestra di dialogo della pagina. La funzione **PageDlgProc** è la routine della finestra di dialogo che gestisce i messaggi della pagina. La variabile **g \_ DllRefCount** include il conteggio dei riferimenti dell'oggetto. Il metodo [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) chiama [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) per incrementare il conteggio. Tuttavia, il conteggio dei riferimenti viene rilasciato dalla funzione di callback, **PageCallbackProc**, quando la pagina sta per essere eliminata definitivamente.

## <a name="remarks"></a>Commenti

Per informazioni generali su come registrare i gestori di estensioni della shell, vedere [creazione di gestori di estensioni della shell](handlers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
