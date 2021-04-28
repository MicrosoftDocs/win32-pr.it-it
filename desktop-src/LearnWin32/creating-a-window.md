---
title: Creazione di una finestra
description: Creazione di una finestra
ms.assetid: e036519f-26b5-436c-b909-bb280d758e81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea5ec39187b389405d3c6d8eca475944278a3d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103969"
---
# <a name="creating-a-window"></a>Creazione di una finestra

## <a name="window-classes"></a>Classi di finestra

Una *classe finestra* definisce un set di comportamenti che possono avere in comune diverse finestre. Ad esempio, in un gruppo di pulsanti, ogni pulsante ha un comportamento simile quando l'utente fa clic sul pulsante. Naturalmente, i pulsanti non sono completamente identici. ogni pulsante visualizza la propria stringa di testo e ha le proprie coordinate dello schermo. I dati univoci per ogni finestra sono denominati *dati di istanza*.

Ogni finestra deve essere associata a una classe finestra, anche se il programma crea una sola istanza di tale classe. È importante comprendere che una classe finestra non è una "classe" nel senso C++. Si tratta piuttosto di una struttura di dati usata internamente dal sistema operativo. Le classi finestra vengono registrate con il sistema in fase di esecuzione. Per registrare una nuova classe finestra, iniziare compilando una [**struttura WNDCLASS:**](/windows/win32/api/winuser/ns-winuser-wndclassa)

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

È necessario impostare i membri della struttura seguenti:

- **lpfnWndProc** è un puntatore a una funzione definita dall'applicazione denominata *routine della* finestra o "proc finestra". La routine della finestra definisce la maggior parte del comportamento della finestra. La procedura della finestra verrà esaminata in dettaglio più avanti. Per il momento, è sufficiente considerarlo come un riferimento in avanti.
- **hInstance è** l'handle per l'istanza dell'applicazione. Ottenere questo valore dal *parametro hInstance* di **wWinMain**.
- **lpszClassName** è una stringa che identifica la classe della finestra.

I nomi delle classi sono locali per il processo corrente, quindi il nome deve essere univoco solo all'interno del processo. Tuttavia, anche i controlli Windows standard hanno classi . Se si usa uno di questi controlli, è necessario selezionare i nomi delle classi che non sono in conflitto con i nomi delle classi del controllo. Ad esempio, la classe della finestra per il controllo pulsante è denominata "Button".

La [**struttura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ha altri membri non illustrati qui. È possibile impostarli su zero, come illustrato in questo esempio, o compilarli. La documentazione MSDN descrive la struttura in dettaglio.

Passare quindi l'indirizzo della [**struttura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) alla [**funzione RegisterClass.**](/windows/desktop/api/winuser/nf-winuser-registerclassa) Questa funzione registra la classe della finestra con il sistema operativo.

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a>Creazione della finestra

Per creare una nuova istanza di una finestra, chiamare la [**funzione CreateWindowEx:**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)

```C++
HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}
```

È possibile leggere le descrizioni dettagliate dei parametri in MSDN, ma di seguito è disponibile un breve riepilogo:

- Il primo parametro consente di specificare alcuni comportamenti facoltativi per la finestra, ad esempio le finestre trasparenti. Impostare questo parametro su zero per i comportamenti predefiniti.
- `CLASS_NAME` è il nome della classe della finestra. Definisce il tipo di finestra che si sta creando.
- Il testo della finestra viene usato in modi diversi da tipi diversi di finestre. Se la finestra ha una barra del titolo, il testo viene visualizzato nella barra del titolo.
- Lo stile della finestra è un set di flag che definiscono parte dell'aspetto di una finestra. La costante **WS \_ OVERLAPPEDWINDOW è** in realtà di diversi flag combinati con or bit per **bit.** Insieme, questi flag forniscono alla finestra una barra del titolo, un bordo, un menu di sistema e **i pulsanti Riduci** a icona e **Ingrandisci.** Questo set di flag è lo stile più comune per una finestra dell'applicazione di primo livello.
- Per posizione e dimensioni, la costante **CW \_ USEDEFAULT indica** l'uso dei valori predefiniti.
- Il parametro successivo imposta una finestra padre o una finestra proprietaria per la nuova finestra. Impostare l'elemento padre se si sta creando una finestra figlio. Per una finestra di primo livello, impostare su **NULL.**
- Per una finestra dell'applicazione, il parametro successivo definisce il menu per la finestra. In questo esempio non viene utilizzato un menu, quindi il valore è **NULL.**
- *hInstance è* l'handle di istanza, descritto in precedenza. Vedere [WinMain: punto di ingresso dell'applicazione.](winmain--the-application-entry-point.md)
- L'ultimo parametro è un puntatore a dati arbitrari di tipo **void \***. È possibile usare questo valore per passare una struttura di dati alla routine della finestra. Verrà illustrato un modo possibile per usare questo parametro nella sezione Gestione [dello stato dell'applicazione.](managing-application-state-.md)

[**CreateWindowEx restituisce**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) un handle per la nuova finestra oppure zero se la funzione non riesce. Per visualizzare la finestra, ovvero renderla visibile, passare l'handle della finestra alla [**funzione ShowWindow:**](/windows/desktop/api/winuser/nf-winuser-showwindow)

```C++
ShowWindow(hwnd, nCmdShow);
```

Il *parametro hwnd* è l'handle di finestra restituito [**da CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Il *parametro nCmdShow* può essere usato per ridurre a icona o ingrandire una finestra. Il sistema operativo passa questo valore al programma tramite la **funzione wWinMain.**

Ecco il codice completo per creare la finestra. Tenere presente `WindowProc` che è ancora solo una dichiarazione con inoltro di una funzione.

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;

RegisterClass(&wc);

// Create the window.

HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}

ShowWindow(hwnd, nCmdShow);
```

È stata creata una finestra. Al momento, la finestra non contiene contenuto né interagisce con l'utente. In un'applicazione GUI reale, la finestra rispondeva agli eventi dell'utente e del sistema operativo. La sezione successiva descrive come i messaggi finestra forniscono questo tipo di interattività.

### <a name="next"></a>Prossima

[Messaggi di finestra](window-messages.md)
