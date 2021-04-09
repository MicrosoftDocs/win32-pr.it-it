---
title: Finestra di dialogo Tipo di carattere
description: La finestra di dialogo tipo di carattere consente all'utente di scegliere gli attributi per un tipo di carattere logico, ad esempio la famiglia di caratteri e lo stile del carattere associato, le dimensioni del punto, gli effetti (sottolineato, l'attacco e il colore del testo) e uno script (o set di caratteri).
ms.assetid: e8a996aa-4e34-45d0-a325-9c20b1a6ce07
keywords:
- Interfaccia utente di Windows, input utente
- Interfaccia utente di Windows, libreria finestra di dialogo comune
- input utente, libreria finestra di dialogo comune
- acquisizione dell'input dell'utente, libreria finestra di dialogo comune
- Libreria finestra di dialogo comune
- finestre di dialogo comuni
- Tipo di carattere (finestra di dialogo)
- personalizzazione della finestra di dialogo carattere
- flag, finestra di dialogo carattere
- flag di inizializzazione
- finestre di dialogo predefinite
- finestre di dialogo, carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a752ce53ecf496c58efb0c346a8c3d67c4f1b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047297"
---
# <a name="font-dialog-box"></a>Finestra di dialogo Tipo di carattere

La finestra di dialogo **tipo di carattere** consente all'utente di scegliere gli attributi per un tipo di carattere logico, ad esempio la famiglia di caratteri e lo stile del carattere associato, le dimensioni del punto, gli effetti (sottolineato, l'attacco e il colore del testo) e uno script (o set di caratteri).

Per creare e visualizzare una finestra di dialogo **tipo di carattere** , inizializzare una struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) e passare la struttura alla funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .

Lo screenshot seguente mostra una finestra di dialogo tipica del **tipo di carattere** .

![screenshot che mostra la finestra di dialogo tipo di carattere](images/fontdialogboxxp.png)

Se l'utente fa clic sul pulsante **OK** , la funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) restituisce **true** e imposta le informazioni sulla selezione dell'utente nella struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .

Se l'utente annulla la finestra di dialogo **tipo di carattere** o si verifica un errore, [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) restituisce **false** e il contenuto della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) non è definito. È possibile determinare la provocazione di un errore utilizzando la funzione [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) per recuperare il valore di errore esteso.

In questa sezione vengono descritti gli argomenti seguenti.

-   [Flag di inizializzazione della finestra di dialogo carattere](#font-dialog-box-initialization-flags)
-   [Personalizzazione della finestra di dialogo tipo di carattere nelle versioni precedenti di Windows](#customizing-the-font-dialog-box-on-earlier-versions-of-windows)
-   [Personalizzazione della finestra di dialogo tipo di carattere in Windows 7](#customizing-the-font-dialog-box-on-windows-7)

## <a name="font-dialog-box-initialization-flags"></a>Flag di inizializzazione della finestra di dialogo carattere

Prima di chiamare [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), è necessario che il membro dei **flag** della struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) specifichi **CF \_ SCREENFONTS**, **CF \_ PRINTERFONTS** o CF per indicare se nella finestra di dialogo sono elencati i tipi di carattere della schermata, i tipi di carattere della stampante o entrambi. **\_** Se si specifica **CF \_ PRINTERFONTS** o **CF \_ both**, il membro **HDC** della struttura **ChooseFont** deve specificare un handle per un contesto di dispositivo per la stampante.

Se è impostato il flag **CF \_ PRINTERFONTS** o **CF \_** , l'etichetta Descrizione tipo di carattere viene visualizzata nella parte inferiore della finestra di dialogo tipo di **carattere** .

A partire da Windows 7, i flag CF **\_ PRINTERFONTS**, **CF \_ SCREENFONTS**, **CF \_ both** e **CF \_ WYSIWYG** non vengono più usati dalla funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per l'enumerazione del tipo di carattere. Sono obsolete in Windows 7. Tuttavia, il flag **CF \_ PRINTERFONTS** mantiene una funzione: per visualizzare l'etichetta della descrizione del tipo di carattere nella parte inferiore della finestra di dialogo tipo di **carattere** .

È possibile usare il membro **Flags** per abilitare o disabilitare alcuni dei controlli della finestra di dialogo del **tipo di carattere** ed è possibile usare il membro **Flags** insieme ad altri membri [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per controllare i valori iniziali di alcuni controlli.

**Per visualizzare i controlli che consentono all'utente di selezionare le opzioni di attacco, sottolineatura e colore:**

-   Imposta il **flag \_ degli effetti CF** . È possibile usare il membro **rgbColors** della struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per specificare un colore iniziale del carattere.

**Per specificare i valori iniziali per il tipo di carattere, lo stile del carattere, le dimensioni, l'attacco e la sottolineatura controlli della finestra di dialogo:**

1.  Per specificare i valori iniziali per il tipo di carattere, lo stile del carattere, le dimensioni, l'attacco e la sottolineatura controlli della finestra di dialogo:
2.  Impostare il **flag CF \_ INITTOLOGFONTSTRUCT** nel membro **Flags** , insieme ai membri della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) a cui punta **LPLOGFONT**, per specificare i valori iniziali per gli attributi del tipo di carattere.
3.  È anche possibile usare i **flag \_ CF NOFACESEL**, **CF \_ NOSTYLESEL** e **CF \_ NOSIZESEL** per impedire alla finestra di dialogo **tipo di carattere** di visualizzare i valori iniziali per i controlli corrispondenti. Questa operazione è utile quando si utilizza una selezione di testo con più di un carattere tipografico, uno stile o una dimensione del punto. Questi valori verranno impostati nei **flag** anche quando [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) restituisce, se l'utente non ha selezionato un valore corrispondente.

**Per inizializzare il controllo dello stile del tipo di carattere sul nome di uno stile specificato**

-   Impostare il flag **CF \_ USESTYLE** e usare il membro **lpszStyle** per specificare il nome dello stile.

> [!Note]  
> Per globalizzare l'applicazione, specificare lo stile usando i membri **lfWeight** e **LfItalic** della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) a cui punta **LPLOGFONT**. Il nome dello stile può variare a seconda della lingua dell'interfaccia utente del sistema.

 

**Per visualizzare il pulsante applica**

-   Impostare il flag **CF \_ Apply** e fornire una procedura di hook per elaborare i messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) per il pulsante **applica** . La procedura hook può inviare il messaggio [**WM \_ ChooseFont \_ GETLOGFONT**](wm-choosefont-getlogfont.md) alla finestra di dialogo per recuperare l'indirizzo della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che contiene le selezioni correnti per il tipo di carattere.

**Per visualizzare il pulsante?**

-   Impostare il flag **CF \_ SHOWHELP** . Il membro **hwndOwner** deve identificare la finestra per ricevere il messaggio registrato [**HELPMSGSTRING**](helpmsgstring.md) quando l'utente fa clic sul pulsante della **Guida** .

**Per limitare i tipi di carattere visualizzati nella finestra di dialogo**

-   Impostare qualsiasi combinazione dei flag **CF \_ TTONLY**, **CF \_ FIXEDPITCHONLY**, **CF \_ NOVECTORFONTS**, **CF \_ NOVERTFONTS**, **CF \_ SCALABLEONLY** e **CF \_ WYSIWYG** . È anche possibile limitare gli stili disponibili visualizzati nella finestra di dialogo per alcuni tipi di carattere usando il valore **CF \_ NoSimulations** .

A partire da Windows 7, l'elenco dei tipi di carattere visualizzati nella finestra di dialogo viene limitato in base ai tipi di carattere visualizzati dall'utente. Per rimuovere la restrizione, impostare il flag **CF \_ INACTIVEFONTS** .

**Per limitare i nomi dei caratteri tipografici, gli stili e le dimensioni dei punti che l'utente può specificare**

1.  Impostare il flag **CF \_ FORCEFONTEXIST** per impedire all'utente di specificare solo nomi di caratteri tipografici validi, stili e dimensioni di punti elencati nella finestra di dialogo.
2.  Impostare il flag **CF \_ LIMITSIZE** per impedire all'utente di specificare le dimensioni dei punti nell'intervallo specificato dai membri **nSizeMin** e **nSizeMax** .

**Per limitare o disabilitare la casella combinata script**

-   Impostare il **flag \_ CF NOSCRIPTSEL** per disabilitare la casella combinata **script** oppure impostare il flag **CF \_ SELECTSCRIPT** per limitare le selezioni nella casella combinata **script** a un set di caratteri specificato.

## <a name="customizing-the-font-dialog-box-on-earlier-versions-of-windows"></a>Personalizzazione della finestra di dialogo tipo di carattere nelle versioni precedenti di Windows

È possibile specificare un modello personalizzato per la finestra di dialogo **tipo di carattere** , ad esempio se si desidera includere controlli aggiuntivi che siano univoci per l'applicazione. La funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) usa il modello personalizzato al posto del modello predefinito.

**Per fornire un modello personalizzato per la finestra di dialogo tipo di carattere**

1.  Creare il modello personalizzato modificando il modello predefinito specificato nel file font. dlg. Gli identificatori di controllo usati nel modello di finestra di dialogo del tipo di carattere predefinito vengono definiti nel file Dlgs. h.
2.  Utilizzare la struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per abilitare il modello nel modo seguente:
    -   Se il modello personalizzato è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il flag **CF \_ ENABLETEMPLATE** nel membro **Flags** . Usare i membri **HINSTANCE** e **lpTemplateName** della struttura per identificare il modulo e il nome della risorsa.
    -   Se il modello personalizzato è già in memoria, impostare il flag **CF \_ ENABLETEMPLATEHANDLE** . Usare il membro **HINSTANCE** per identificare l'oggetto memoria che contiene il modello.

È possibile specificare una procedura di hook [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) per la finestra di dialogo **tipo di carattere** . La procedura hook può elaborare i messaggi inviati alla finestra di dialogo e inviare messaggi alla finestra di dialogo. Se si usa un modello personalizzato per definire controlli aggiuntivi, è necessario fornire una procedura di hook per elaborare l'input per i controlli.

**Per abilitare una routine hook per la finestra di dialogo tipo di carattere**

1.  Impostare il flag **CF \_ ENABLEHOOK** nel membro **Flags** della struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .
2.  Specificare l'indirizzo della routine hook nel membro **lpfnHook** .

Dopo l'elaborazione del messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) , la routine della finestra di dialogo Invia un messaggio **WM \_ INITDIALOG** alla routine hook. Il parametro *lParam* di questo messaggio è un puntatore alla struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) utilizzata per inizializzare la finestra di dialogo.

La procedura di hook può inviare i messaggi [**WM \_ ChooseFont \_ GETLOGFONT**](wm-choosefont-getlogfont.md), [**WM \_ ChooseFont \_ SETLOGFONT**](wm-choosefont-setlogfont.md)e [**WM \_ ChooseFont \_ Flags**](wm-choosefont-setflags.md) alla finestra di dialogo per ottenere e impostare i valori correnti e i flag della finestra di dialogo.

## <a name="customizing-the-font-dialog-box-on-windows-7"></a>Personalizzazione della finestra di dialogo tipo di carattere in Windows 7

Lo screenshot seguente mostra una finestra di dialogo tipica dei **tipi di carattere** in Windows 7.

![screenshot che mostra il tipo di carattere DIALOB box](images/fontdialogboxwin7.png)

Nelle versioni precedenti di Windows, il file di modello font. dlg contiene un modello ChooseFont predefinito. Il file di modello font. dlg in Windows 7 contiene due modelli predefiniti: il modello predefinito di versioni precedenti di Windows e il nuovo modello ChooseFont di Windows 7. Pertanto, quando si Personalizza la finestra di dialogo **tipo di carattere** in Windows 7, è necessario considerare i seguenti problemi.

1.  Utilizzare il nuovo modello quando si creano modelli personalizzati per le applicazioni eseguite in Windows 7. Questo nuovo modello contiene un controllo collegamento su cui l'utente può fare clic per avviare la finestra del **Pannello di controllo dei tipi di carattere** , come illustrato nella schermata seguente.

    ![screenshot che mostra il pannello di controllo dei tipi di carattere in Windows 7](images/fontcontrolpanelforwin7.png)

2.  Per utilizzare questo controllo collegamento, è necessario che nell'applicazione chiamante venga utilizzato il COMCTL32.DLL versione 6 o successiva. In caso contrario, la funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) restituisce un errore quando tenta di creare il controllo dei collegamenti nel modello personalizzato. Per determinare se il controllo è abilitato, compilare l'applicazione chiamante sulla versione di COMCTL32.DLL 6,0. Per altre informazioni, vedere [Abilitazione degli stili di visualizzazione con i controlli comuni](/previous-versions//ms649781(v=vs.85)).
3.  Se l'applicazione usa COMCTL32.DLL versione 5,0 o precedente, quando si crea un modello personalizzato è necessario eseguire le operazioni seguenti:

    -   Specificare il controllo come **pulsante**. Il controllo usato per avviare il **Pannello di controllo dei tipi di carattere** verrà visualizzato come pulsante anziché come collegamento.
    -   Sostituire il testo seguente in font. dlg:

        `CONTROL         "<A>Show more fonts</A>", IDC_MANAGE_LINK, "SysLink", WS_TABSTOP, 7, 199, 227, 9`

        con il testo seguente:

        `PUSHBUTTON      "S&how more fonts", IDC_MANAGE_LINK, 7, 199, 74, 14 , WS_TABSTOP`

    -   Per assicurarsi che l'applicazione usi un modello personalizzato, è necessario specificare un modello personalizzato con il flag **CF \_ ENABLETEMPLATE** , creare un modello personalizzato basato sul modello ChooseFont di Windows 7 e, facoltativamente, abilitare una procedura hook.

        Se si abilita una procedura hook senza creare un modello personalizzato, verrà caricato il modello ChooseFont predefinito per le versioni precedenti di Windows.

> [!Note]  
> È necessario specificare il tipo di controllo del **controllo** o del **pulsante** nel nuovo modello, a seconda della versione di COMMCTL.DLL eseguita per la compilazione dell'applicazione. Si noti inoltre che le funzionalità specifiche di Windows 7, ad esempio la visualizzazione WYSIWYG degli elenchi di tipi di carattere e le famiglie estese, non sono disponibili quando le applicazioni vengono eseguite in versioni precedenti del sistema operativo Windows.

 

 

 