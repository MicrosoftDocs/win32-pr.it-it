---
title: Finestra di dialogo Colore
description: Visualizza una finestra di dialogo modale che consente all'utente di scegliere un valore di colore specifico.
ms.assetid: 248586b5-5068-4021-8407-56eb79243789
keywords:
- input utente, libreria finestra di dialogo comune
- acquisizione dell'input dell'utente, libreria finestra di dialogo comune
- Libreria finestra di dialogo comune
- finestre di dialogo comuni
- Finestra di dialogo Colore
- finestra di dialogo colore parziale
- finestra di dialogo colori completi
- personalizzazione della finestra di dialogo colore
- Modello colori RGB
- Modello di colore HSL
- HSL (Hue Saturation luminosità)
- HSL (Hue Saturation luminosità)
- RGB (rosso verde blu)
- blu verde rosso (RGB)
- Hook, finestra di dialogo colore
- finestre di dialogo predefinite
- finestre di dialogo, colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb90150f49ea7bed4edac53af40ba89e0459946
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/19/2020
ms.locfileid: "104552351"
---
# <a name="color-dialog-box"></a>Finestra di dialogo Colore

Visualizza una finestra di dialogo modale che consente all'utente di scegliere un valore di colore specifico. L'utente può scegliere un colore da un set di tavolozze dei colori di base o personalizzato. In alternativa, l'utente può generare un valore di colore modificando i valori di colore RGB o Hue, Saturation, luminosità (HSL) dell'interfaccia utente della finestra di dialogo. La finestra di dialogo **colore** restituisce il valore RGB del colore selezionato dall'utente.

Per creare e visualizzare una finestra di dialogo **colore** , inizializzare una struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) e passare la struttura alla funzione [**le CHOOSECOLOR.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) . Impostando valori di parametro diversi per la struttura **le CHOOSECOLOR.** , è possibile influire sul modo in cui viene visualizzata la finestra di dialogo colore. Ad esempio, è possibile visualizzare una versione completa o parziale dell'interfaccia utente della finestra di dialogo. Nella figura seguente viene illustrata la versione dell'interfaccia utente completa della finestra di dialogo **colore** .

![finestra di dialogo dei colori](images/colordialogboxxp.png)

Se l'utente fa clic sul pulsante **OK** , [**le CHOOSECOLOR.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) restituisce **true**. Il membro **rgbResult** della struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) contiene il valore di colore RGB del colore selezionato dall'utente. Il valore di colore RGB specifica le intensità dei singoli colori rosso, verde e blu che compongono il colore selezionato. I singoli valori sono compresi tra 0 e 255. Usare le macro [**GetRValue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue)e [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue) per estrarre i singoli colori da un valore di colore RGB.

Se l'utente annulla la finestra di dialogo **colore** o si verifica un errore, [**le CHOOSECOLOR.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) restituisce **false** e il membro **rgbResult** non è definito. Per determinare la cause dell'errore, chiamare la funzione [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) per recuperare il valore di errore esteso.

In questa sezione vengono trattati gli argomenti seguenti:

-   [Finestre di dialogo colori completi e parziali](#full-and-partial-color-dialog-boxes)
-   [Personalizzazione della finestra di dialogo colore](#customizing-the-color-dialog-box)
    -   [Per fornire un modello personalizzato per la finestra di dialogo colore](#to-provide-a-custom-template-for-the-color-dialog-box)
    -   [Per abilitare una routine hook per la finestra di dialogo colore](#to-enable-a-hook-procedure-for-the-color-dialog-box)
-   [Modelli di colore utilizzati dalla finestra di dialogo colore](#color-models-used-by-the-color-dialog-box)
    -   [Modello colori RGB](#rgb-color-model)
    -   [Modello di colore HSL](#hsl-color-model)
    -   [Conversione dei valori HSL in valori RGB](#converting-hsl-values-to-rgb-values)

## <a name="full-and-partial-color-dialog-boxes"></a>Finestre di dialogo colori completi e parziali

Nella finestra di dialogo colore sono presenti una versione completa e una versione parziale dell'interfaccia utente. La versione completa include i controlli di base e dispone di controlli aggiuntivi che consentono all'utente di creare colori personalizzati. La versione parziale include controlli che visualizzano le tavolozze dei colori di base e personalizzate da cui l'utente può selezionare un valore di colore.

La versione parziale della finestra di dialogo colore include un pulsante **Definisci colori personalizzati** . L'utente può fare clic su questo pulsante per visualizzare la versione completa. È possibile indicare alla finestra di dialogo colore di visualizzare sempre la versione completa impostando il flag **\_ FULLOPEN CC** nel membro **Flags** della struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) . Per impedire all'utente di creare colori personalizzati, è possibile impostare il **flag \_ PREVENTFULLOPEN di CC** per disabilitare il pulsante **Definisci colori personalizzati** .

I colori di base rappresentano una selezione dei colori disponibili nel dispositivo specificato. Il numero effettivo di colori visualizzato è determinato dal driver di visualizzazione. Ad esempio, un driver VGA Visualizza 48 colori e un driver di visualizzazione monocromatico Visualizza solo 16.

I colori personalizzati sono quelli specificati dall'utente o creati dall'utente. Quando si crea una finestra di dialogo colore, è necessario usare il membro **lpCustColors** della struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) per specificare i valori iniziali per i 16 colori personalizzati. Se la versione completa della finestra di dialogo colore è aperta, l'utente può creare un colore personalizzato per uno dei metodi seguenti:

-   Spostare il cursore nel controllo dello spettro dei colori e nel controllo della diapositiva di luminosità
-   Digitazione di valori RGB nei controlli di modifica **rosso**, **verde** e **blu**
-   Digitazione di valori HSL nei controlli di modifica **Hue**, **Sat** e **Lum**

Per aggiungere un nuovo colore personalizzato alla visualizzazione colori personalizzati, l'utente può fare clic sul pulsante **Aggiungi a colori personalizzati** . In questo modo, la finestra di dialogo Copia il valore RGB del nuovo colore nell'elemento corrispondente nella matrice a cui punta il membro **lpCustColors** . Per mantenere i nuovi colori personalizzati tra le chiamate a [**le CHOOSECOLOR.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)), è necessario allocare memoria statica per la matrice. Per ulteriori informazioni sui modelli di colore RGB e HSL, vedere [modelli di colore utilizzati dalla finestra di dialogo colore](#color-models-used-by-the-color-dialog-box).

## <a name="customizing-the-color-dialog-box"></a>Personalizzazione della finestra di dialogo colore

Per personalizzare una finestra di dialogo colore, è possibile utilizzare uno dei metodi seguenti:

-   Specificare i valori nella struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) quando si crea la finestra di dialogo
-   Fornire un modello personalizzato
-   Fornire una routine hook

È possibile modificare l'aspetto e il comportamento della finestra di dialogo colore impostando i flag nel membro **Flags** della struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) . Ad esempio, è possibile impostare il flag **CC \_ SolidColor** per indicare alla finestra di dialogo di visualizzare solo i colori a tinta unita. Per fare in modo che la finestra di dialogo selezioni inizialmente un colore diverso da nero, impostare il flag **\_ RGBINIT CC** e specificare un colore nel membro **rgbResult** .

È possibile specificare un modello personalizzato per la finestra di dialogo colore, ad esempio se si desidera includere controlli aggiuntivi che siano univoci per l'applicazione. La funzione [**le CHOOSECOLOR.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) usa il modello personalizzato al posto del modello predefinito.

### <a name="to-provide-a-custom-template-for-the-color-dialog-box"></a>Per fornire un modello personalizzato per la finestra di dialogo colore

1.  Creare il modello personalizzato modificando il modello predefinito specificato nel file color. dlg. Gli identificatori di controllo utilizzati nel modello di finestra di dialogo colore predefinito vengono definiti nel file color. dlg.
2.  Utilizzare la struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) per abilitare il modello nel modo seguente:
    -   Se il modello personalizzato è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il flag **\_ ENABLETEMPLATE CC** nel membro **Flags** . Usare i membri **HINSTANCE** e **lpTemplateName** della struttura per identificare il modulo e il nome della risorsa.

        oppure

    -   Se il modello personalizzato è già in memoria, impostare il flag **CC \_ ENABLETEMPLATEHANDLE** . Usare il membro **HINSTANCE** per identificare l'oggetto memoria che contiene il modello.

È possibile specificare una procedura di hook [**CCHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc) per la finestra di dialogo colore. La procedura hook può elaborare i messaggi inviati alla finestra di dialogo. Può inoltre utilizzare i messaggi registrati per controllare il comportamento della finestra di dialogo. Se si usa un modello personalizzato per definire controlli aggiuntivi, è necessario fornire una procedura di hook per elaborare l'input per i controlli.

### <a name="to-enable-a-hook-procedure-for-the-color-dialog-box"></a>Per abilitare una routine hook per la finestra di dialogo colore

1.  Impostare il **flag \_ ENABLEHOOK CC** nel membro **Flags** della struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) .
2.  Specificare l'indirizzo della routine hook nel membro **lpfnHook** .

Dopo l'elaborazione del messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) , la routine della finestra di dialogo Invia un messaggio **WM \_ INITDIALOG** alla routine hook. Il parametro *lParam* di questo messaggio è un puntatore alla struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) utilizzata per inizializzare la finestra di dialogo.

La finestra di dialogo Invia il messaggio registrato [**COLOROKSTRING**](colorokstring.md) alla procedura hook quando l'utente fa clic sul pulsante **OK** . La routine hook può rifiutare il colore selezionato e forzare la finestra di dialogo in modo che rimanga aperta restituendo zero quando riceve il messaggio. La procedura hook consente di forzare la finestra di dialogo per selezionare un colore specifico inviando il messaggio registrato [**SETRGBSTRING**](setrgbstring.md) alla finestra di dialogo. Per usare questi messaggi registrati, è necessario passare le costanti **COLOROKSTRING** e **SETRGBSTRING** alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere un identificatore di messaggio. È quindi possibile utilizzare l'identificatore per rilevare ed elaborare i messaggi inviati dalla finestra di dialogo o per inviare messaggi alla finestra di dialogo.

## <a name="color-models-used-by-the-color-dialog-box"></a>Modelli di colore utilizzati dalla finestra di dialogo colore

L'estensione colori personalizzati della finestra di dialogo colore consente all'utente di specificare un colore utilizzando i valori RGB o HSL. Tuttavia, la struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) utilizza solo valori RGB per segnalare i colori creati o selezionati dall'utente.

-   [Modello colori RGB](#rgb-color-model)
-   [Modello di colore HSL](#hsl-color-model)
-   [Conversione dei valori HSL in valori RGB](#converting-hsl-values-to-rgb-values)

### <a name="rgb-color-model"></a>Modello colori RGB

Il modello RGB viene usato per definire i colori per le visualizzazioni e altri dispositivi che emettono luce. I valori di rosso, verde e blu validi sono compresi tra 0 e 255, con 0 indicante l'intensità minima e 255 che indicano l'intensità massima. Nella figura seguente viene illustrato il modo in cui i colori primari rosso, verde e blu possono essere combinati per produrre quattro colori aggiuntivi. (Per i dispositivi di visualizzazione, il colore nero risulta quando i valori rosso, verde e blu sono impostati su 0. Nella tecnologia di visualizzazione, il nero è l'assenza di tutti i colori.

![cerchi sovrapposti rosso, verde e blu](images/rgbcolormodel.png)

La tabella seguente elenca otto colori del modello RGB e i valori RGB associati.



| Colore   | Valori RGB    |
|---------|---------------|
| Red     | 255, 0,0     |
| Green   | 0, 255, 0     |
| Blu    | 0, 0, 255     |
| azzurro    | 0, 255, 255   |
| Fucsia | 255, 0, 255   |
| Giallo  | 255, 255, 0   |
| White   | 255, 255, 255 |
| Nero   | 0, 0, 0       |



 

Il sistema archivia i colori interni come valori RGB a 32 bit il cui formato esadecimale è il seguente: 0x00bbggrr.

Il byte di ordine inferiore contiene un valore per l'intensità relativa del rosso; il secondo byte contiene un valore per il verde; e il terzo byte contiene un valore per il blu. Il byte di ordine superiore deve essere zero.

È possibile usare la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) per ottenere un valore RGB basato sulle intensità specificate per i componenti rosso, verde e blu. Usare le macro [**GetRValue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue), [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue)e [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue) per estrarre i singoli colori da un valore di colore RGB.

### <a name="hsl-color-model"></a>Modello di colore HSL

Nella finestra di dialogo colore sono disponibili controlli per specificare i valori HSL. Nella figura seguente vengono mostrati il controllo dello spettro dei colori e il controllo della diapositiva di luminosità visualizzati nella finestra di dialogo colore. L'illustrazione mostra anche gli intervalli di valori che l'utente può specificare con questi controlli.

![spettro di colore e scala della luminosità](images/colordialogranges.png)

Nella finestra di dialogo colore i valori di saturazione e luminosità devono essere compresi tra 0 e 240 e il valore di tonalità deve essere compreso tra 0 e 239.

### <a name="converting-hsl-values-to-rgb-values"></a>Conversione dei valori HSL in valori RGB

La procedura della finestra di dialogo disponibile in Comdlg32.dll per la finestra di dialogo colore contiene codice che converte i valori HSL nei valori RGB corrispondenti. La tabella seguente elenca otto colori del modello RGB e i relativi valori HSL e RGB associati.



| Colore   | HSL (valori)      | Valori RGB      |
|---------|-----------------|-----------------|
| Red     | (0, 240, 120)   | (255, 0, 0)     |
| Giallo  | (40, 240, 120)  | (255, 255, 0)   |
| Green   | (80, 240, 120)  | (0, 255, 0)     |
| azzurro    | (120, 240, 120) | (0, 255, 255)   |
| Blu    | (160, 240, 120) | (0, 0, 255)     |
| Fucsia | (200, 240, 120) | (255, 0, 255)   |
| White   | (0, 0, 240)     | (255, 255, 255) |
| Nero   | (0, 0, 0)       | (0, 0, 0)       |



 

 

 
