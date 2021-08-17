---
title: Finestra di dialogo Tipo di carattere
description: La finestra di dialogo Carattere consente all'utente di scegliere gli attributi per un tipo di carattere logico, ad esempio la famiglia di caratteri e lo stile del carattere associato, le dimensioni del punto, gli effetti (sottolineatura, barratura e colore del testo) e uno script (o set di caratteri).
ms.assetid: e8a996aa-4e34-45d0-a325-9c20b1a6ce07
keywords:
- Windows Interfaccia utente,input utente
- Windows Interfaccia utente,Common Dialog Box Library
- input utente,Libreria di finestre di dialogo comuni
- acquisizione dell'input dell'utente, libreria di finestre di dialogo comune
- Libreria di finestre di dialogo comune
- finestre di dialogo comuni
- Tipo di carattere (finestra di dialogo)
- Personalizzazione del tipo di carattere - finestra di dialogo
- flags,Finestra di dialogo Tipo di carattere
- flag di inizializzazione
- finestre di dialogo predefinite
- finestre di dialogo, Tipo di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8544fcb60e499a360f60d1701863a11138d3f16fb06a770a9a2763800d908e12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785901"
---
# <a name="font-dialog-box"></a>Finestra di dialogo Tipo di carattere

La finestra **di** dialogo Carattere consente all'utente di scegliere gli attributi per un tipo di carattere logico, ad esempio la famiglia di caratteri e lo stile del carattere associato, le dimensioni del punto, gli effetti (sottolineatura, barratura e colore del testo) e uno script (o set di caratteri).

Per creare e visualizzare una **finestra di dialogo** Tipo di carattere, inizializzare una struttura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) e passare la struttura alla [**funzione ChooseFont.**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)

Lo screenshot seguente mostra una tipica finestra **di dialogo Tipo** di carattere.

![Screenshot che mostra la finestra di dialogo del tipo di carattere](images/fontdialogboxxp.png)

Se l'utente fa clic sul pulsante **OK,** la funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) restituisce **TRUE** e imposta le informazioni sulla selezione dell'utente nella [**struttura CHOOSEFONT.**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)

Se l'utente annulla la **finestra di** dialogo Tipo di carattere o si verifica un errore, [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) restituisce **FALSE** e il contenuto della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) non è definito. È possibile determinare la causa di un errore usando la [**funzione CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) per recuperare il valore di errore esteso.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Flag di inizializzazione della finestra di dialogo Tipo di carattere](#font-dialog-box-initialization-flags)
-   [Personalizzazione della finestra di dialogo Tipo di carattere nelle versioni precedenti di Windows](#customizing-the-font-dialog-box-on-earlier-versions-of-windows)
-   [Personalizzazione della finestra di dialogo Tipo di carattere Windows 7](#customizing-the-font-dialog-box-on-windows-7)

## <a name="font-dialog-box-initialization-flags"></a>Flag di inizializzazione della finestra di dialogo Tipo di carattere

Prima di chiamare [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), il membro **Flags** della struttura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) deve specificare **CF \_ SCREENFONTS**, **CF \_ PRINTERFONTS** o **CF \_ BOTH** per indicare se nella finestra di dialogo devono essere elencati i tipi di carattere della schermata, i tipi di carattere della stampante o entrambi. Se si specifica **CF \_ PRINTERFONTS** o **CF \_ BOTH,** il membro **hDC** della struttura **CHOOSEFONT** deve specificare un handle per un contesto di dispositivo per la stampante.

Se il flag **\_ CF PRINTERFONTS** o **CF \_ BOTH** è impostato, l'etichetta della descrizione del tipo di carattere viene visualizzata nella parte inferiore della **finestra di** dialogo Tipo di carattere.

A partire da Windows 7, i flag **CF \_ PRINTERFONTS**, **CF \_ SCREENFONTS**, **CF \_ BOTH** e **CF \_ WYSIWYG** non vengono più usati dalla funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per l'enumerazione dei tipi di carattere. Sono obsoleti in Windows 7. Tuttavia, il flag **\_ PRINTERFONTS cf mantiene** una funzione: per visualizzare l'etichetta della descrizione del tipo di carattere nella parte inferiore della finestra **di** dialogo Tipo di carattere.

È possibile usare il membro **Flags** per  abilitare o disabilitare alcuni controlli della finestra di dialogo Tipo di carattere e il membro **Flags** insieme ad altri membri [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per controllare i valori iniziali di alcuni controlli.

**Per visualizzare i controlli che consentono all'utente di selezionare le opzioni di barratura, sottolineatura e colore:**

-   Impostare il flag **\_ CF EFFECTS.** È possibile usare il **membro rgbColors** della struttura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per specificare un colore iniziale del carattere.

**Per specificare i valori iniziali per i controlli della finestra di dialogo Carattere, Stile carattere, Dimensioni, Barrato e Sottolineatura:**

1.  Per specificare i valori iniziali per i controlli della finestra di dialogo Carattere, Stile carattere, Dimensioni, Barrato e Sottolineatura:
2.  Impostare il flag **\_ CF INITTOLOGFONTSTRUCT** nel membro **Flags,** insieme ai membri della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) a cui punta **lpLogFont**, per specificare i valori iniziali per gli attributi del tipo di carattere.
3.  È anche possibile usare i flag **CF \_ NOFACESEL**, **CF \_ NOSTYLESEL** e **CF \_ NOSIZESEL** per impedire alla finestra di dialogo Carattere di visualizzare i valori iniziali per i controlli corrispondenti.  Ciò è utile quando si utilizza una selezione di testo con più caratteri tipografici, stili o dimensioni in punti. Questi valori verranno impostati anche in **Flag** quando [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) restituisce il risultato, se l'utente non ha selezionato un valore corrispondente.

**Per inizializzare il controllo Stile carattere con un nome di stile specificato**

-   Impostare il flag **\_ USESTYLE cf** e usare il membro **lpszStyle** per specificare il nome dello stile.

> [!Note]  
> Per globalizzare l'applicazione, specificare lo stile usando i membri **lfWeight** e **lfItalic** della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) a cui punta **lpLogFont**. Il nome dello stile può cambiare a seconda della lingua dell'interfaccia utente del sistema.

 

**Per visualizzare il pulsante Applica**

-   Impostare il flag **CF \_ APPLY** e fornire una procedura hook per elaborare [**i messaggi WM \_ COMMAND**](/windows/desktop/menurc/wm-command) per il **pulsante** Applica. La routine hook può inviare il messaggio [**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) alla finestra di dialogo per recuperare l'indirizzo della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che contiene le selezioni correnti per il tipo di carattere.

**Per visualizzare il pulsante ?**

-   Impostare il flag **CF \_ SHOWHELP.** Il **membro hwndOwner** deve identificare la finestra per ricevere il messaggio registrato [**helpMSGSTRING**](helpmsgstring.md) quando l'utente fa clic sul **pulsante ?** .

**Per limitare i tipi di carattere visualizzati nella finestra di dialogo**

-   Impostare qualsiasi combinazione dei flag **CF \_ TTONLY**, **CF \_ FIXEDPITCHONLY**, **CF \_ NOVECTORFONTS**, **CF \_ NOVERTFONTS**, **CF \_ SCALABLEONLY** e **CF \_ WYSIWYG.** È anche possibile limitare gli stili disponibili visualizzati nella finestra di dialogo per alcuni tipi di carattere usando il **valore CF \_ NOSIMULATIONS.**

A partire Windows 7, l'elenco dei tipi di carattere visualizzati nella finestra di dialogo è limitato in base ai tipi di carattere visualizzati dall'utente. Per rimuovere la restrizione, impostare il flag **\_ CF INACTIVEFONTS.**

**Per limitare i nomi dei caratteri tipografici, gli stili e le dimensioni dei punti che l'utente può specificare**

1.  Impostare il flag **CF \_ FORCEFONTEXIST** per limitare l'utente alla specifica di nomi di caratteri tipografici, stili e dimensioni dei punti validi elencati nella finestra di dialogo.
2.  Impostare il flag **CF \_ LIMITSIZE** per limitare l'utente alla specifica delle dimensioni dei punti nell'intervallo specificato dai membri **nSizeMin** **e nSizeMax.**

**Per limitare o disabilitare la casella combinata Script**

-   Impostare il flag **\_ CF NOSCRIPTSEL** per disabilitare la casella combinata **Script** oppure impostare il flag **CF \_ SELECTSCRIPT** per limitare le selezioni nella casella combinata **Script** a un set di caratteri specificato.

## <a name="customizing-the-font-dialog-box-on-earlier-versions-of-windows"></a>Personalizzazione della finestra di dialogo Tipo di carattere nelle versioni precedenti di Windows

È possibile fornire un  modello personalizzato per la finestra di dialogo Tipo di carattere, ad esempio se si desidera includere controlli aggiuntivi univoci per l'applicazione. La [**funzione ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) usa il modello personalizzato al posto del modello predefinito.

**Per fornire un modello personalizzato per la finestra di dialogo Tipo di carattere**

1.  Creare il modello personalizzato modificando il modello predefinito specificato nel file Font.dlg. Gli identificatori di controllo usati nel modello di finestra di dialogo Tipo di carattere predefinito sono definiti nel file Dlgs.h.
2.  Usare la [**struttura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per abilitare il modello come segue:
    -   Se il modello personalizzato è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il flag **\_ ENABLETEMPLATE cf** nel **membro Flags.** Usare i **membri hInstance** **e lpTemplateName** della struttura per identificare il modulo e il nome della risorsa.
    -   Se il modello personalizzato è già in memoria, impostare il flag **\_ CF ENABLETEMPLATEHANDLE.** Usare il **membro hInstance** per identificare l'oggetto memoria che contiene il modello.

È possibile specificare una procedura hook [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) per la finestra **di** dialogo Tipo di carattere . La routine hook può elaborare i messaggi inviati alla finestra di dialogo e inviare messaggi alla finestra di dialogo. Se si usa un modello personalizzato per definire controlli aggiuntivi, è necessario fornire una procedura hook per elaborare l'input per i controlli.

**Per abilitare una procedura hook per la finestra di dialogo Tipo di carattere**

1.  Impostare il flag **\_ CF ENABLEHOOK** nel **membro Flags** della [**struttura CHOOSEFONT.**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
2.  Specificare l'indirizzo della procedura hook nel **membro lpfnHook.**

Dopo [**l'elaborazione del messaggio WM \_ INITDIALOG,**](wm-initdialog.md) la routine della finestra di dialogo invia un **messaggio WM \_ INITDIALOG** alla routine hook. Il *parametro lParam* di questo messaggio è un puntatore alla struttura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) usata per inizializzare la finestra di dialogo.

La routine hook può inviare i messaggi [**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md), [**WM \_ CHOOSEFONT \_ SETLOGFONT**](wm-choosefont-setlogfont.md)e [**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) alla finestra di dialogo per ottenere e impostare i valori e i flag correnti della finestra di dialogo.

## <a name="customizing-the-font-dialog-box-on-windows-7"></a>Personalizzazione della finestra di dialogo Tipo di carattere Windows 7

Lo screenshot seguente mostra una tipica finestra **di dialogo** Tipo di carattere in Windows 7.

![Screenshot che mostra la casella dialob del tipo di carattere](images/fontdialogboxwin7.png)

Nelle versioni Windows versioni precedenti, il file di modello font.dlg contiene un modello ChooseFont predefinito. Il file di modello font.dlg in Windows 7 contiene due modelli predefiniti: il modello predefinito delle versioni precedenti di Windows e il nuovo modello ChooseFont Windows 7. Pertanto, quando si personalizza la finestra **di** dialogo Tipo di carattere Windows 7, è necessario considerare i problemi seguenti.

1.  Usare il nuovo modello quando si creano modelli personalizzati per le applicazioni eseguite in Windows 7. Questo nuovo modello contiene un controllo collegamento su cui l'utente può fare clic per avviare la finestra **Pannello di controllo** tipi di carattere, come illustrato nello screenshot seguente.

    ![Screenshot che mostra il pannello di controllo del tipo di carattere in Windows 7](images/fontcontrolpanelforwin7.png)

2.  Per usare questo controllo collegamento, l'applicazione chiamante deve usare COMCTL32.DLL versione 6 o successiva. In caso contrario, [**la funzione ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) restituisce un errore quando tenta di creare il controllo collegamento nel modello personalizzato. Per determinare se questo controllo è abilitato, compilare l'applicazione chiamante COMCTL32.DLL versione 6.0. Per altre informazioni, vedere [Abilitazione degli stili di visualizzazione con controlli comuni.](/previous-versions//ms649781(v=vs.85))
3.  Se l'applicazione COMCTL32.DLL versione 5.0 o precedente, è necessario eseguire le operazioni seguenti quando si crea un modello personalizzato:

    -   Specificare il controllo come **PUSHBUTTON.** Il controllo usato per avviare **l'Pannello di controllo** tipi di carattere verrà visualizzato come pulsante anziché come collegamento.
    -   Sostituire il testo seguente nel file font.dlg:

        `CONTROL         "<A>Show more fonts</A>", IDC_MANAGE_LINK, "SysLink", WS_TABSTOP, 7, 199, 227, 9`

        con il testo seguente:

        `PUSHBUTTON      "S&how more fonts", IDC_MANAGE_LINK, 7, 199, 74, 14 , WS_TABSTOP`

    -   Per assicurarsi che l'applicazione usi un modello personalizzato, è necessario specificare un modello personalizzato con il flag **\_ CF ENABLETEMPLATE,** creare un modello personalizzato basato sul modello ChooseFont di Windows 7 e quindi abilitare facoltativamente una procedura hook.

        Se si abilita una procedura hook senza creare un modello personalizzato, verrà caricato il modello ChooseFont predefinito per le versioni Windows precedenti.

> [!Note]  
> È necessario specificare il **tipo di** controllo CONTROL o **PUSHBUTTON** nel nuovo modello, a seconda della versione COMMCTL.DLL compilata dall'applicazione. Si noti inoltre che Windows 7 funzionalità specifiche, ad esempio la visualizzazione WYSIWYG di elenchi di tipi di carattere e famiglie estese, non sono disponibili quando le applicazioni vengono eseguite in versioni precedenti del sistema operativo Windows.

 

 

 