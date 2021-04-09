---
title: Finestra di dialogo Imposta pagina
description: Visualizza una finestra di dialogo modale che consente all'utente di scegliere le impostazioni che includono il tipo di carta, l'origine della carta, l'orientamento della pagina e la larghezza dei margini della pagina.
ms.assetid: debde0a0-07d4-46ed-a936-e517eab1852d
keywords:
- Interfaccia utente di Windows, input utente
- Interfaccia utente di Windows, libreria finestra di dialogo comune
- input utente, libreria finestra di dialogo comune
- acquisizione dell'input dell'utente, libreria finestra di dialogo comune
- Libreria finestra di dialogo comune
- finestre di dialogo comuni
- Imposta pagina - finestra di dialogo
- personalizzazione della finestra di dialogo Imposta pagina
- Hook, finestra di dialogo Imposta pagina
- finestre di dialogo predefinite
- finestre di dialogo, Imposta pagina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b9a8f7f30a8313017dc3a124cdccb7d00c872b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118410"
---
# <a name="page-setup-dialog-box"></a>Finestra di dialogo Imposta pagina

Visualizza una finestra di dialogo modale che consente all'utente di impostare gli attributi seguenti della pagina stampata:

-   Il tipo di carta (busta, legale, lettera e così via)
-   Origine della carta (feed manuale, feed del trattore, alimentatore del foglio e così via)
-   Orientamento della pagina (verticale o orizzontale)
-   Larghezza dei margini della pagina

Per creare e visualizzare una finestra di dialogo di **impostazione della pagina** , inizializzare una struttura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) e passare la struttura alla funzione [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) . Tuttavia, gli attributi presentati nella finestra di dialogo variano a seconda delle funzionalità della stampante. Nella figura seguente viene illustrata una tipica finestra di dialogo di **impostazione della pagina** .

![finestra di dialogo Imposta pagina](images/pagesetupdialogboxxp.png)

Se l'utente fa clic sul pulsante **OK** , [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) restituisce **true** dopo avere impostato diversi membri nella struttura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) per specificare le selezioni dell'utente. I membri **ptPaperSize** e **rtMargin** contengono i valori specificati dall'utente. I membri **hDevMode** e **hDevNames** contengono handle di memoria globali per le strutture [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) e [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) . Queste strutture contengono informazioni aggiuntive sulla pagina, nonché informazioni sulla stampante. È possibile utilizzare queste informazioni per preparare l'output da inviare alla stampante selezionata.

Se l'utente annulla la finestra di dialogo **Imposta pagina** o si verifica un errore, [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) restituisce **false**. Per determinare la cause dell'errore, chiamare la funzione [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) per recuperare il valore di errore esteso.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Inizializzazione della finestra di dialogo Imposta pagina](#initializing-the-page-setup-dialog-box)
-   [Personalizzazione della finestra di dialogo Imposta pagina](#customizing-the-page-setup-dialog-box)
-   [Personalizzazione della pagina di esempio](#customizing-the-sample-page)

## <a name="initializing-the-page-setup-dialog-box"></a>Inizializzazione della finestra di dialogo Imposta pagina

Per impostazione predefinita, nella finestra di dialogo **Imposta pagina** vengono visualizzate informazioni sulla stampante predefinita corrente. Per indicare alla finestra di dialogo di visualizzare informazioni su una stampante specifica, impostare i membri di una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) o [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) e assegnare gli handle di memoria globale di queste strutture al membro corrispondente in [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga). Se si specifica il nome di una stampante attualmente non installata, nella finestra di dialogo verrà visualizzato un messaggio di errore. Per impedire alla finestra di dialogo di visualizzare i messaggi di errore, usare il valore di **\_ Nowarning di PSD** . Per recuperare informazioni sulla stampante predefinita senza visualizzare la finestra di dialogo **Imposta pagina** , usare il **valore \_ RETURNDEFAULT di PSD** .

Se il sistema di misurazione predefinito è pollici, la finestra di dialogo utilizza i millesimi di pollice come unità di misura predefinita. Se il sistema di misurazione predefinito è metrica, la finestra di dialogo utilizza centesimi di millimetri come unità di misura predefinita. Per eseguire l'override dell'unità di misura predefinita, impostare il flag **PSD \_ INHUNDREDTHSOFMILLIMETERS** o **PSD \_ INTHOUSANDTHSOFINCHES** nel membro **Flags** della struttura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .

Per impostazione predefinita, i valori iniziali per i margini sono di un pollice. Se si imposta il flag dei **\_ margini PSD** , nella finestra di dialogo verranno visualizzati i valori dei margini iniziali specificati nel membro **rtMargin** . I valori minimi predefiniti che l'utente può specificare per i margini sono i margini minimi consentiti dalla stampante. Se si imposta il **flag \_ MINMARGINS di PSD** , la finestra di dialogo impone i margini minimi specificati nel membro **rtMinMargin** .

Per impedire agli utenti di selezionare determinate opzioni, impostare una combinazione dei flag seguenti per disabilitare i controlli corrispondenti.



| Contrassegno                        | Significato                                                                  |
|-----------------------------|--------------------------------------------------------------------------|
| **\_DISABLEMARGINS PSD**     | Disabilita i controlli di modifica in cui l'utente immette le impostazioni dei margini. |
| **\_DISABLEORIENTATION PSD** | Disabilita i pulsanti di opzione **verticale** e **orizzontale** .               |
| **\_DISABLEPAPER PSD**       | Disabilita i controlli per selezionare il formato della carta e l'origine della carta.     |
| **\_DISABLEPRINTER PSD**     | Disabilita il pulsante **stampante** .                                         |



 

## <a name="customizing-the-page-setup-dialog-box"></a>Personalizzazione della finestra di dialogo Imposta pagina

È possibile specificare un modello personalizzato per la finestra di dialogo **Imposta pagina** , ad esempio se si desidera includere controlli aggiuntivi che siano univoci per l'applicazione. La funzione [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) usa il modello personalizzato al posto del modello predefinito.

**Per fornire un modello personalizzato per la finestra di dialogo Imposta pagina**

1.  Creare il modello personalizzato modificando il modello predefinito specificato nel file prnsetup. dlg. Gli identificatori di controllo utilizzati nel modello di finestra di dialogo **Imposta pagina** predefinito sono definiti nel file Dlgs. h.
2.  Utilizzare la struttura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) per abilitare il modello nel modo seguente:
    -   -   Se il modello personalizzato è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il flag **PSD \_ ENABLEPAGESETUPTEMPLATE** nel membro **Flags** . Usare i membri **HINSTANCE** e **lpPageSetupTemplateName** della struttura per identificare il modulo e il nome della risorsa.

            oppure

        -   Se il modello personalizzato è già in memoria, impostare il **flag \_ ENABLEPAGESETUPTEMPLATEHANDLE di PSD** . Usare il membro **hPageSetupTemplate** per identificare l'oggetto memoria che contiene il modello.

Per filtrare i messaggi inviati alla routine della finestra di dialogo, è possibile specificare una procedura di hook [**PageSetupHook**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) . Se si usa un modello personalizzato per definire controlli aggiuntivi, è necessario fornire una procedura hook **PageSetupHook** per elaborare l'input per i controlli. Inoltre, è possibile fornire una procedura [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook per personalizzare il contenuto della pagina di esempio visualizzata dalla finestra di dialogo **Imposta pagina** . Per ulteriori informazioni sulla procedura di hook **PagePaintHook** , vedere [personalizzazione della pagina di esempio](#customizing-the-sample-page).

**Per abilitare una procedura PageSetupHook Hook**

1.  Impostare il **flag \_ ENABLEPAGESETUPHOOK di PSD** nel membro **Flags** della struttura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .
2.  Specificare l'indirizzo della routine hook nel membro **lpfnPageSetupHook** .

Dopo l'elaborazione del messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) , la routine della finestra di dialogo Invia un messaggio **WM \_ INITDIALOG** alla routine hook [**PageSetupHook**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) . Il parametro *lParam* di questo messaggio è un puntatore alla struttura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) utilizzata per inizializzare la finestra di dialogo.

## <a name="customizing-the-sample-page"></a>Personalizzazione della pagina di esempio

Nella finestra di dialogo **Imposta pagina** è inclusa un'immagine di una pagina di esempio in cui viene illustrato il modo in cui le selezioni dell'utente influiscono sull'aspetto dell'output stampato. L'immagine è costituita da un rettangolo che rappresenta il tipo di carta o busta selezionato, con un rettangolo della linea tratteggiata che rappresenta i margini correnti e i caratteri parziali (testo greco) per mostrare come appare il testo nella pagina stampata.

Quando si chiama la funzione [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , è possibile fornire una procedura di hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare l'aspetto della pagina di esempio.

**Per abilitare una procedura PagePaintHook Hook**

1.  Impostare il **flag \_ ENABLEPAGEPAINTHOOK di PSD** nel membro **Flags** della struttura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .
2.  Specificare l'indirizzo della routine hook nel membro **lpfnPagePaintHook** .

Ogni volta che la finestra di dialogo sta per creare il contenuto della pagina di esempio, la procedura di hook riceve i messaggi seguenti nell'ordine in cui sono elencati.



| Messaggio                                                  | Significato                                                                                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_PAGESETUPDLG PSD \_ WM**](wm-psd-pagesetupdlg.md)     | La finestra di dialogo sta per creare la pagina di esempio. La procedura hook può utilizzare questo messaggio per prepararsi a creare il contenuto della pagina di esempio.     |
| [**\_FULLPAGERECT PSD \_ WM**](wm-psd-fullpagerect.md)     | La finestra di dialogo sta per creare la pagina di esempio. Questo messaggio specifica il rettangolo delimitatore della pagina di esempio.                               |
| [**\_MINMARGINRECT PSD \_ WM**](wm-psd-minmarginrect.md)   | La finestra di dialogo sta per creare la pagina di esempio. Questo messaggio specifica il rettangolo del margine.                                                    |
| [**\_MARGINRECT PSD \_ WM**](wm-psd-marginrect.md)         | La finestra di dialogo sta per creare il rettangolo dei margini.                                                                                            |
| [**\_GREEKTEXTRECT PSD \_ WM**](wm-psd-greektextrect.md)   | La finestra di dialogo sta per creare il testo greco all'interno del rettangolo dei margini.                                                                      |
| [**\_ENVSTAMPRECT PSD \_ WM**](wm-psd-envstamprect.md)     | La finestra di dialogo sta per essere creata nel rettangolo del timbro della busta di una pagina di esempio della busta. Questo messaggio viene inviato solo per le buste.             |
| [**\_YAFULLPAGERECT PSD \_ WM**](wm-psd-yafullpagerect.md) | La finestra di dialogo sta per creare la parte dell'indirizzo restituito di una pagina di esempio della busta. Questo messaggio viene inviato per le buste e altri formati di carta. |



 

Se la procedura di hook restituisce **true** per uno dei primi tre messaggi di una sequenza di disegno ([**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md), [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)o [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)) la finestra di dialogo non invia più messaggi e non disegna nella pagina di esempio fino alla successiva necessità di ridisegnare la pagina di esempio. Se la routine hook restituisce **false** per tutti e tre i messaggi, la finestra di dialogo invierà i messaggi rimanenti della sequenza di disegno.

Se la procedura di hook restituisce **true** per uno dei messaggi rimanenti in una sequenza di disegno, nella finestra di dialogo non viene disegnata la parte corrispondente della pagina di esempio. Se la procedura di hook restituisce **false** per uno di questi messaggi, la finestra di dialogo disegna la parte della pagina di esempio.

Per evitare che la finestra di dialogo disegni il contenuto della pagina di esempio, è possibile impostare il flag **\_ DISABLEPAGEPAINTING di PSD** . Questo flag non influisce sulla procedura [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) Hook, che ancora riceve tutti i messaggi di **WM \_ PSD \_ \*** e può tracciare il contenuto della pagina di esempio.

 

 