---
title: Finestra di dialogo Imposta pagina
description: Visualizza una finestra di dialogo modale che consente all'utente di scegliere impostazioni che includono il tipo di carta, l'origine della carta, l'orientamento della pagina e la larghezza dei margini della pagina.
ms.assetid: debde0a0-07d4-46ed-a936-e517eab1852d
keywords:
- Windows Interfaccia utente,input utente
- Windows Interfaccia utente,Common Dialog Box Library
- input utente,Libreria di finestre di dialogo comuni
- acquisizione dell'input dell'utente, libreria di finestre di dialogo comune
- Libreria di finestre di dialogo comune
- finestre di dialogo comuni
- Imposta pagina - finestra di dialogo
- personalizzazione della finestra di dialogo Imposta pagina
- hook, finestra di dialogo Imposta pagina
- finestre di dialogo predefinite
- finestre di dialogo, Imposta pagina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af64357be8bd39217c6527dc81f7ac426f5e06e183de92b3bb479f4633c75d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741656"
---
# <a name="page-setup-dialog-box"></a>Finestra di dialogo Imposta pagina

Visualizza una finestra di dialogo modale che consente all'utente di impostare gli attributi seguenti della pagina stampata:

-   Tipo di carta (busta, legale, lettera e così via)
-   Origine della carta (alimentazione manuale, alimentazione a trattore, alimentatore di fogli e così via)
-   Orientamento della pagina (verticale o orizzontale)
-   Larghezza dei margini della pagina

Per creare e visualizzare una **finestra di** dialogo Imposta pagina, inizializzare una [**struttura PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) e passare la struttura [**alla funzione PageSetupDlg.**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) Tuttavia, gli attributi presentati nella finestra di dialogo variano a seconda delle funzionalità della stampante. Nella figura seguente viene illustrata una tipica **finestra di dialogo Imposta** pagina.

![imposta pagina - finestra di dialogo](images/pagesetupdialogboxxp.png)

Se l'utente fa clic sul pulsante **OK,** [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) restituisce **TRUE** dopo aver impostato vari membri nella [**struttura PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) per specificare le selezioni dell'utente. I **membri ptPaperSize** **e rtMargin** contengono i valori specificati dall'utente. I **membri hDevMode** **e hDevNames** contengono handle di memoria globali per le [**strutture DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) e [**DEVNAMES.**](/windows/win32/api/commdlg/ns-commdlg-devnames) Queste strutture contengono informazioni aggiuntive sulla pagina e informazioni sulla stampante. È possibile utilizzare queste informazioni per preparare l'output da inviare alla stampante selezionata.

Se l'utente annulla la finestra **di dialogo Imposta** pagina o si verifica un errore, [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) restituisce **FALSE.** Per determinare la causa dell'errore, chiamare la [**funzione CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) per recuperare il valore di errore esteso.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Inizializzazione della finestra di dialogo Imposta pagina](#initializing-the-page-setup-dialog-box)
-   [Personalizzazione della finestra di dialogo Imposta pagina](#customizing-the-page-setup-dialog-box)
-   [Personalizzazione della pagina di esempio](#customizing-the-sample-page)

## <a name="initializing-the-page-setup-dialog-box"></a>Inizializzazione della finestra di dialogo Imposta pagina

Per impostazione predefinita, **nella finestra di** dialogo Imposta pagina vengono visualizzate informazioni sulla stampante predefinita corrente. Per indirizzare la finestra di dialogo alla visualizzazione di informazioni su una stampante specifica, impostare i membri di una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) o [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) e assegnare gli handle di memoria globali di queste strutture al membro corrispondente in [**PAGESETUPDLG.**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) Se si specifica il nome di una stampante non attualmente installata, nella finestra di dialogo viene visualizzato un messaggio di errore. Per impedire la visualizzazione dei messaggi di errore nella finestra di dialogo, usare il **valore \_ PSD NOWARNING.** Per recuperare informazioni sulla stampante predefinita senza visualizzare la finestra di dialogo **Imposta** pagina, usare il **valore PSD \_ RETURNDEFAULT.**

Se il sistema di misurazione predefinito è pollici, la finestra di dialogo usa i millesima di pollici come unità di misura predefinita. Se il sistema di misurazione predefinito è metrica, la finestra di dialogo usa centesimi di millimetri come unità di misura predefinita. Per eseguire l'override dell'unità di misura predefinita, impostare il flag **\_ PSD INHUNDREDTHSOFMILLIMETERS** o **PSD \_ INTHOUSANDTHSOFINCHES** nel membro **Flags** della [**struttura PAGESETUPDLG.**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)

Per impostazione predefinita, i valori iniziali per i margini sono di un pollice. Se si imposta il flag **MARGINS di \_ PSD,** nella finestra di dialogo vengono visualizzati i valori iniziali dei margini specificati nel **membro rtMargin.** I valori minimi predefiniti che l'utente può specificare per i margini sono i margini minimi consentiti dalla stampante. Se si imposta il flag **\_ PSD MINMARGINS,** la finestra di dialogo applica i margini minimi specificati nel **membro rtMinMargin.**

Per impedire agli utenti di selezionare determinate opzioni, impostare qualsiasi combinazione dei flag seguenti per disabilitare i controlli corrispondenti.



| Contrassegno                        | Significato                                                                  |
|-----------------------------|--------------------------------------------------------------------------|
| **PSD \_ DISABLEMARGINS**     | Disabilita i controlli di modifica in cui l'utente immette le impostazioni del margine. |
| **PSD \_ DISABLEORIENTATION** | Disabilita i pulsanti **di opzione Verticale** **e** Orizzontale.               |
| **PSD \_ DISABLEPAPER**       | Disabilita i controlli per la selezione del formato e dell'origine della carta.     |
| **PSD \_ DISABLEPRINTER**     | Disabilita il **pulsante** Stampante.                                         |



 

## <a name="customizing-the-page-setup-dialog-box"></a>Personalizzazione della finestra di dialogo Imposta pagina

È possibile fornire un  modello personalizzato per la finestra di dialogo Imposta pagina, ad esempio se si desidera includere controlli aggiuntivi univoci per l'applicazione. La [**funzione PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) usa il modello personalizzato al posto del modello predefinito.

**Per fornire un modello personalizzato per la finestra di dialogo Imposta pagina**

1.  Creare il modello personalizzato modificando il modello predefinito specificato nel file Prnsetup.dlg. Gli identificatori di controllo usati nel modello predefinito **della** finestra di dialogo Imposta pagina sono definiti nel file Dlgs.h.
2.  Usare la [**struttura PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) per abilitare il modello come segue:
    -   -   Se il modello personalizzato è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il flag **\_ ENABLEPAGESETUPTEMPLATE psd** nel **membro Flags.** Usare i **membri hInstance** **e lpPageSetupTemplateName** della struttura per identificare il modulo e il nome della risorsa.

            oppure

        -   Se il modello personalizzato è già in memoria, impostare il flag **\_ ENABLEPAGESETUPTEMPLATEHANDLE psd.** Usare il **membro hPageSetupTemplate** per identificare l'oggetto memoria che contiene il modello.

Per filtrare i messaggi inviati alla procedura della finestra di dialogo, è possibile specificare una routine hook [**PageSetupHook.**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) Se si usa un modello personalizzato per definire controlli aggiuntivi, è necessario fornire una procedura hook **PageSetupHook** per elaborare l'input per i controlli. È anche possibile fornire una procedura hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare il contenuto della pagina di esempio visualizzata nella finestra **di dialogo Imposta** pagina. Per altre informazioni sulla procedura hook **PagePaintHook,** vedere [Personalizzazione della pagina di esempio.](#customizing-the-sample-page)

**Per abilitare una procedura hook PageSetupHook**

1.  Impostare il flag **PSD \_ ENABLEPAGESETUPHOOK** nel **membro Flags** della [**struttura PAGESETUPDLG.**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
2.  Specificare l'indirizzo della procedura hook nel **membro lpfnPageSetupHook.**

Dopo [**l'elaborazione del messaggio WM \_ INITDIALOG,**](wm-initdialog.md) la procedura della finestra di dialogo invia un messaggio **WM \_ INITDIALOG** alla procedura hook [**PageSetupHook.**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) Il *parametro lParam* di questo messaggio è un puntatore alla [**struttura PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) usata per inizializzare la finestra di dialogo.

## <a name="customizing-the-sample-page"></a>Personalizzazione della pagina di esempio

La **finestra di dialogo** Imposta pagina include un'immagine di una pagina di esempio che mostra in che modo le selezioni dell'utente influiscono sull'aspetto dell'output stampato. L'immagine è costituita da un rettangolo che rappresenta il tipo di carta o busta selezionato, con un rettangolo a linee tratteggiate che rappresenta i margini correnti e caratteri parziali (testo greco) per mostrare l'aspetto del testo nella pagina stampata.

Quando si chiama la [**funzione PageSetupDlg,**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) è possibile fornire una procedura hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare l'aspetto della pagina di esempio.

**Per abilitare una routine hook PagePaintHook**

1.  Impostare il flag **PSD \_ ENABLEPAGEPAINTHOOK** nel **membro Flags** della [**struttura PAGESETUPDLG.**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
2.  Specificare l'indirizzo della procedura hook nel **membro lpfnPagePaintHook.**

Ogni volta che la finestra di dialogo sta per disegnare il contenuto della pagina di esempio, la procedura hook riceve i messaggi seguenti nell'ordine in cui sono elencati.



| Messaggio                                                  | Significato                                                                                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md)     | La finestra di dialogo sta per disegnare la pagina di esempio. La procedura hook può utilizzare questo messaggio per preparare il disegno del contenuto della pagina di esempio.     |
| [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)     | La finestra di dialogo sta per disegnare la pagina di esempio. Questo messaggio specifica il rettangolo di delimitazione della pagina di esempio.                               |
| [**\_MINMARGINRECT DI WM PSD \_**](wm-psd-minmarginrect.md)   | La finestra di dialogo sta per disegnare la pagina di esempio. Questo messaggio specifica il rettangolo del margine.                                                    |
| [**WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md)         | La finestra di dialogo sta per disegnare il rettangolo del margine.                                                                                            |
| [**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md)   | La finestra di dialogo sta per disegnare il testo greco all'interno del rettangolo del margine.                                                                      |
| [**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md)     | La finestra di dialogo sta per essere disegnata nel rettangolo del timbro della busta di una pagina di esempio della busta. Questo messaggio viene inviato solo per le buste.             |
| [**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md) | La finestra di dialogo sta per disegnare la parte relativa all'indirizzo del mittente di una pagina di esempio della busta. Questo messaggio viene inviato per buste e altri formati di carta. |



 

Se la routine hook restituisce **TRUE** per uno dei primi tre messaggi di una sequenza di disegno ([**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md), [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)o [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)), la finestra di dialogo non invia altri messaggi e non disegna nella pagina di esempio fino alla successiva necessità del sistema di ridisegnare la pagina di esempio. Se la routine hook restituisce **FALSE per** tutti e tre i messaggi, la finestra di dialogo invia i messaggi rimanenti della sequenza di disegno.

Se la routine hook restituisce **TRUE** per tutti i messaggi rimanenti in una sequenza di disegno, la finestra di dialogo non disegna la parte corrispondente della pagina di esempio. Se la routine hook restituisce **FALSE** per uno di questi messaggi, la finestra di dialogo disegna tale parte della pagina di esempio.

Per impedire alla finestra di dialogo di disegnare il contenuto della pagina di esempio, è possibile impostare il flag **PSD \_ DISABLEPAGEPAINTING.** Questo flag non influisce sulla procedura hook [**PagePaintHook,**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) che riceve comunque tutti i messaggi **\_ \_ \* PSD WM** e può disegnare il contenuto della pagina di esempio.

 

 