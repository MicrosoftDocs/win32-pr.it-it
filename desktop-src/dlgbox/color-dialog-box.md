---
title: Finestra di dialogo Colore
description: Visualizza una finestra di dialogo modale che consente all'utente di scegliere un valore di colore specifico.
ms.assetid: 248586b5-5068-4021-8407-56eb79243789
keywords:
- input utente,Libreria di finestre di dialogo comuni
- acquisizione dell'input dell'utente,Common Dialog Box Library
- Libreria di finestre di dialogo comuni
- finestre di dialogo comuni
- Finestra di dialogo Colore
- Finestra di dialogo Colore parziale
- Finestra di dialogo Colore completo
- Personalizzazione della finestra di dialogo Colore
- Modello di colore RGB
- Modello di colore HSL
- luminosità della saturazione della tonalità (HSL)
- HSL (luminosità saturazione tonalità)
- RGB (blu verde rosso)
- rosso verde blu (RGB)
- hook, finestra di dialogo Colore
- finestre di dialogo predefinite
- finestre di dialogo,Colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bdfb1543de80ac105d4a6012a0c95ff46cd8da1fef204ed573d14d05a6dfe9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726422"
---
# <a name="color-dialog-box"></a>Finestra di dialogo Colore

Visualizza una finestra di dialogo modale che consente all'utente di scegliere un valore di colore specifico. L'utente può scegliere un colore da un set di tavolozze di colori di base o personalizzate. In alternativa, l'utente può generare un valore di colore modificando i valori di colore RGB o tonalità, saturazione, luminosità (HSL) dell'interfaccia utente della finestra di dialogo. La **finestra** di dialogo Colore restituisce il valore RGB del colore selezionato dall'utente.

Per creare e visualizzare una finestra di dialogo **Colore,** inizializzare una [**struttura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) e passare la struttura alla [**funzione ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) Impostando valori di parametro diversi per la **struttura CHOOSECOLOR,** è possibile influire sul modo in cui viene visualizzata la finestra di dialogo Colore. Ad esempio, è possibile visualizzare una versione completa o parziale dell'interfaccia utente della finestra di dialogo. La figura seguente illustra la versione completa dell'interfaccia utente della **finestra di dialogo** Colore.

![finestra di dialogo dei colori](images/colordialogboxxp.png)

Se l'utente fa clic sul **pulsante OK,** [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) restituisce **TRUE.** Il **membro rgbResult** della struttura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) contiene il valore del colore RGB del colore selezionato dall'utente. Il valore del colore RGB specifica le intensità dei singoli colori rosso, verde e blu che costituiscono il colore selezionato. I singoli valori sono da 0 a 255. Usare le macro [**GetRValue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue)e [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue) per estrarre singoli colori da un valore di colore RGB.

Se l'utente annulla la **finestra di** dialogo Colore o si verifica un errore, [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) restituisce **FALSE** e il membro **rgbResult** non è definito. Per determinare la causa dell'errore, chiamare la [**funzione CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) per recuperare il valore di errore esteso.

In questa sezione vengono trattati gli argomenti seguenti

-   [Finestre di dialogo a colori completi e parziali](#full-and-partial-color-dialog-boxes)
-   [Personalizzazione della finestra di dialogo Colore](#customizing-the-color-dialog-box)
    -   [Per fornire un modello personalizzato per la finestra di dialogo Colore](#to-provide-a-custom-template-for-the-color-dialog-box)
    -   [Per abilitare una procedura hook per la finestra di dialogo Colore](#to-enable-a-hook-procedure-for-the-color-dialog-box)
-   [Modelli a colori usati dalla finestra di dialogo Colore](#color-models-used-by-the-color-dialog-box)
    -   [Modello di colore RGB](#rgb-color-model)
    -   [Modello di colore HSL](#hsl-color-model)
    -   [Conversione di valori HSL in valori RGB](#converting-hsl-values-to-rgb-values)

## <a name="full-and-partial-color-dialog-boxes"></a>Finestre di dialogo a colori completi e parziali

La finestra di dialogo Colore ha una versione completa e una versione parziale dell'interfaccia utente. La versione completa include i controlli di base e include controlli aggiuntivi che consentono all'utente di creare colori personalizzati. La versione parziale include controlli che visualizzano le tavolozze dei colori di base e personalizzate da cui l'utente può selezionare un valore di colore.

La versione parziale della finestra di dialogo Colore include un **pulsante Definisci colori** personalizzati. L'utente può fare clic su questo pulsante per visualizzare la versione completa. È possibile indirizzare la finestra di dialogo Colore per visualizzare sempre la versione completa impostando il flag **CC \_ FULLOPEN** nel membro **Flags** della [**struttura CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) Per impedire all'utente di creare colori personalizzati, è possibile impostare il flag **CC \_ PREVENTFULLOPEN** per disabilitare il **pulsante Definisci colori** personalizzati.

I colori di base rappresentano una selezione dei colori disponibili nel dispositivo specificato. Il numero effettivo di colori visualizzati è determinato dal driver di visualizzazione. Ad esempio, un driver VGA visualizza 48 colori e un driver di visualizzazione monocromatico visualizza solo 16.

I colori personalizzati sono quelli specificati dall'utente o creati dall'utente. Quando si crea una finestra di dialogo Colore, è necessario usare il membro **lpCustColors** della struttura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) per specificare i valori iniziali per i 16 colori personalizzati. Se la versione completa della finestra di dialogo Colore è aperta, l'utente può creare un colore personalizzato usando uno dei metodi seguenti:

-   Spostamento del cursore nel controllo dello spettro dei colori e nel controllo di scorrimento luminosità
-   Digitazione di valori RGB nei controlli di modifica **Rosso,** **Verde** **e** Blu
-   Digitazione di valori HSL nei controlli di modifica **Hue,** **Sat** e **Lum**

Per aggiungere un nuovo colore personalizzato alla visualizzazione dei colori personalizzati, l'utente può fare clic sul pulsante Aggiungi **a colori** personalizzati. In questo modo la finestra di dialogo copia anche il valore RGB del nuovo colore nell'elemento corrispondente nella matrice a cui punta il membro **lpCustColors.** Per mantenere i nuovi colori personalizzati tra le chiamate a [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)), è necessario allocare memoria statica per la matrice. Per altre informazioni sui modelli di colore RGB e HSL, vedere [Modelli di colore usati dalla finestra di dialogo Colore](#color-models-used-by-the-color-dialog-box).

## <a name="customizing-the-color-dialog-box"></a>Personalizzazione della finestra di dialogo Colore

Per personalizzare una finestra di dialogo Colore, è possibile usare uno dei metodi seguenti:

-   Specificare i valori nella [**struttura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) quando si crea la finestra di dialogo
-   Fornire un modello personalizzato
-   Fornire una procedura hook

È possibile modificare l'aspetto e il comportamento della finestra di dialogo Colore impostando i flag nel membro **Flags** della [**struttura CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) Ad esempio, è possibile impostare il flag **CC \_ SOLIDCOLOR** per indirizzare la finestra di dialogo in modo da visualizzare solo i colori a tinta unita. Per fare in modo che la finestra di dialogo seleziona inizialmente un colore diverso dal nero, impostare il flag **\_ CC RGBINIT** e specificare un colore nel **membro rgbResult.**

È possibile fornire un modello personalizzato per la finestra di dialogo Colore, ad esempio se si desidera includere controlli aggiuntivi univoci per l'applicazione. La [**funzione ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) usa il modello personalizzato al posto del modello predefinito.

### <a name="to-provide-a-custom-template-for-the-color-dialog-box"></a>Per fornire un modello personalizzato per la finestra di dialogo Colore

1.  Creare il modello personalizzato modificando il modello predefinito specificato nel file Color.dlg. Gli identificatori di controllo usati nel modello predefinito della finestra di dialogo Colore sono definiti nel file Color.dlg.
2.  Usare la [**struttura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) per abilitare il modello come segue:
    -   Se il modello personalizzato è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il flag **CC \_ ENABLETEMPLATE** nel **membro Flags.** Usare i **membri hInstance** **e lpTemplateName** della struttura per identificare il modulo e il nome della risorsa.

        oppure

    -   Se il modello personalizzato è già in memoria, impostare il flag **\_ CC ENABLETEMPLATEHANDLE.** Usare il **membro hInstance** per identificare l'oggetto di memoria che contiene il modello.

È possibile fornire una [**procedura hook CCHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc) per la finestra di dialogo Colore. La procedura hook può elaborare i messaggi inviati alla finestra di dialogo. Può anche usare i messaggi registrati per controllare il comportamento della finestra di dialogo. Se si usa un modello personalizzato per definire controlli aggiuntivi, è necessario fornire una procedura hook per elaborare l'input per i controlli.

### <a name="to-enable-a-hook-procedure-for-the-color-dialog-box"></a>Per abilitare una procedura hook per la finestra di dialogo Colore

1.  Impostare il flag **\_ CC ENABLEHOOK** nel **membro Flags** della [**struttura CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
2.  Specificare l'indirizzo della procedura hook nel membro **lpfnHook.**

Dopo l'elaborazione [**del messaggio WM \_ INITDIALOG,**](wm-initdialog.md) la routine della finestra di dialogo invia un **messaggio WM \_ INITDIALOG** alla procedura hook. Il *parametro lParam* di questo messaggio è un puntatore alla struttura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) usata per inizializzare la finestra di dialogo.

La finestra di dialogo invia il [**messaggio registrato COLOROKSTRING**](colorokstring.md) alla procedura hook quando l'utente fa clic sul **pulsante OK.** La procedura hook può rifiutare il colore selezionato e forzare la finestra di dialogo a rimanere aperta restindo zero quando riceve questo messaggio. La procedura hook può forzare la finestra di dialogo a selezionare un colore specifico inviando il [**messaggio registrato SETRGBSTRING**](setrgbstring.md) alla finestra di dialogo. Per usare questi messaggi registrati, è necessario passare le costanti **COLOROKSTRING** e **SETRGBSTRING** alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere un identificatore di messaggio. È quindi possibile usare l'identificatore per rilevare ed elaborare i messaggi inviati dalla finestra di dialogo o per inviare messaggi alla finestra di dialogo.

## <a name="color-models-used-by-the-color-dialog-box"></a>Modelli a colori usati dalla finestra di dialogo Colore

L'estensione dei colori personalizzati della finestra di dialogo Colore consente all'utente di specificare un colore usando valori RGB o HSL. Tuttavia, la [**struttura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) usa solo valori RGB per segnalare i colori creati o selezionati dall'utente.

-   [Modello colore RGB](#rgb-color-model)
-   [Modello colori HSL](#hsl-color-model)
-   [Conversione di valori HSL in valori RGB](#converting-hsl-values-to-rgb-values)

### <a name="rgb-color-model"></a>Modello colore RGB

Il modello RGB viene usato per designare i colori per schermi e altri dispositivi che emettono luce. I valori validi di rosso, verde e blu sono compreso tra 0 e 255, con 0 che indica l'intensità minima e 255 che indica l'intensità massima. Nella figura seguente viene illustrato come combinare i colori primari rosso, verde e blu per produrre altri quattro colori. Per i dispositivi di visualizzazione, il colore nero risulta quando i valori rosso, verde e blu sono impostati su 0. Nella tecnologia di visualizzazione, il nero è l'assenza di tutti i colori.

![cerchi rosso, verde e blu sovrapposti](images/rgbcolormodel.png)

La tabella seguente elenca otto colori del modello RGB e i relativi valori RGB associati.



| Color   | Valori RGB    |
|---------|---------------|
| Red     | 255, 0, 0     |
| Green   | 0, 255, 0     |
| Blu    | 0, 0, 255     |
| azzurro    | 0, 255, 255   |
| Fucsia | 255, 0, 255   |
| Giallo  | 255, 255, 0   |
| White   | 255, 255, 255 |
| Nero   | 0, 0, 0       |



 

Il sistema archivia i colori interni come valori RGB a 32 bit con il formato esadecimale seguente: 0x00bbggrr.

Il byte meno significativo contiene un valore per l'intensità relativa del rosso. il secondo byte contiene un valore verde. e il terzo byte contiene un valore per blu. Il byte più significativo deve essere zero.

È possibile usare la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) per ottenere un valore RGB in base alle intensità specificate per i componenti rosso, verde e blu. Usare le macro [**GetRValue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue), [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue)e [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue) per estrarre singoli colori da un valore di colore RGB.

### <a name="hsl-color-model"></a>Modello colori HSL

Nella finestra di dialogo Colore sono disponibili controlli per la specifica di valori HSL. La figura seguente mostra il controllo dello spettro dei colori e il controllo della diapositiva luminosità visualizzati nella finestra di dialogo Colore . La figura mostra anche gli intervalli di valori che l'utente può specificare con questi controlli.

![spettro di colori e scala di luminosità](images/colordialogranges.png)

Nella finestra di dialogo Colore i valori di saturazione e luminosità devono essere nell'intervallo compreso tra 0 e 240 e il valore della tonalità deve essere compreso nell'intervallo da 0 a 239.

### <a name="converting-hsl-values-to-rgb-values"></a>Conversione di valori HSL in valori RGB

La procedura della finestra di dialogo Comdlg32.dll per la finestra di dialogo Colore contiene il codice che converte i valori HSL nei valori RGB corrispondenti. La tabella seguente elenca otto colori del modello RGB e i valori HSL e RGB associati.



| Color   | HSL (valori)      | Valori RGB      |
|---------|-----------------|-----------------|
| Red     | (0, 240, 120)   | (255, 0, 0)     |
| Giallo  | (40, 240, 120)  | (255, 255, 0)   |
| Green   | (80, 240, 120)  | (0, 255, 0)     |
| azzurro    | (120, 240, 120) | (0, 255, 255)   |
| Blu    | (160, 240, 120) | (0, 0, 255)     |
| Fucsia | (200, 240, 120) | (255, 0, 255)   |
| White   | (0, 0, 240)     | (255, 255, 255) |
| Nero   | (0, 0, 0)       | (0, 0, 0)       |



 

 

 
