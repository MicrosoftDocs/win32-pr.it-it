---
title: Creazione di una finestra
description: .
ms.assetid: e036519f-26b5-436c-b909-bb280d758e81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126f040d72fec423ad5b6f3ecb31bc780a3192b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399037"
---
# <a name="creating-a-window"></a>Creazione di una finestra

## <a name="window-classes"></a>Classi di finestra

Una *classe di finestra* definisce un set di comportamenti che possono avere più finestre in comune. Ad esempio, in un gruppo di pulsanti, ogni pulsante presenta un comportamento simile quando l'utente fa clic sul pulsante. Naturalmente, i pulsanti non sono completamente identici. ogni pulsante Visualizza la propria stringa di testo e presenta le proprie coordinate dello schermo. I dati univoci per ogni finestra sono denominati *dati dell'istanza*.

Ogni finestra deve essere associata a una classe della finestra, anche se il programma crea solo un'istanza di tale classe. È importante comprendere che una classe di finestra non è una "classe" nel senso di C++. Piuttosto, si tratta di una struttura di dati utilizzata internamente dal sistema operativo. Le classi finestra vengono registrate con il sistema in fase di esecuzione. Per registrare una nuova classe di finestra, iniziare compilando una struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) :

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

È necessario impostare i membri della struttura seguenti:

- **lpfnWndProc** è un puntatore a una funzione definita dall'applicazione denominata *routine della finestra* o "finestra proc". La routine della finestra definisce la maggior parte del comportamento della finestra. La procedura della finestra verrà esaminata in dettaglio in un secondo momento. Per il momento, è sufficiente considerarlo come riferimento in futuro.
- **HINSTANCE** è l'handle per l'istanza dell'applicazione. Ottenere questo valore dal parametro *HINSTANCE* di **wWinMain**.
- **lpszClassName** è una stringa che identifica la classe Window.

I nomi delle classi sono locali per il processo corrente, quindi il nome deve essere univoco solo all'interno del processo. Tuttavia, anche i controlli Windows standard hanno classi. Se si utilizza uno di questi controlli, è necessario selezionare i nomi delle classi che non sono in conflitto con i nomi delle classi di controlli. Ad esempio, la classe della finestra per il controllo Button è denominata "button".

La struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) contiene altri membri non mostrati qui. È possibile impostarli su zero, come illustrato in questo esempio, o compilarli. La documentazione di MSDN descrive in modo dettagliato la struttura.

Passare quindi l'indirizzo della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) alla funzione [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) . Questa funzione registra la classe della finestra con il sistema operativo.

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a>Creazione della finestra

Per creare una nuova istanza di una finestra, chiamare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) :

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

È possibile leggere le descrizioni dettagliate dei parametri in MSDN, ma di seguito è riportato un breve riepilogo:

- Il primo parametro consente di specificare alcuni comportamenti facoltativi per la finestra, ad esempio finestre trasparenti. Impostare questo parametro su zero per i comportamenti predefiniti.
- `CLASS_NAME` nome della classe della finestra. Definisce il tipo di finestra che si sta creando.
- Il testo della finestra viene utilizzato in modi diversi in base ai diversi tipi di finestre. Se la finestra dispone di una barra del titolo, il testo viene visualizzato nella barra del titolo.
- Lo stile della finestra è un set di flag che definiscono parte dell'aspetto di una finestra. La costante **WS \_ OVERLAPPEDWINDOW** è in realtà costituita da diversi flag combinati con un **or** bit per bit. Insieme, questi flag assegnano alla finestra una barra del titolo, un bordo, un menu di sistema e i pulsanti **Riduci a icona** e **Ingrandisci** . Questo set di flag rappresenta lo stile più comune per una finestra dell'applicazione di livello superiore.
- Per position e size, la costante **\_ usedefault (CW** indica di usare i valori predefiniti.
- Il parametro successivo imposta una finestra padre o una finestra proprietaria per la nuova finestra. Impostare l'elemento padre se si sta creando una finestra figlio. Per una finestra di primo livello, impostare su **null**.
- Per una finestra dell'applicazione, il parametro successivo definisce il menu per la finestra. In questo esempio non viene utilizzato un menu, pertanto il valore è **null**.
- *HINSTANCE* è l'handle dell'istanza, descritto in precedenza. Vedere [WinMain: punto di ingresso dell'applicazione](winmain--the-application-entry-point.md).
- L'ultimo parametro è un puntatore a dati arbitrari di tipo **void \***. È possibile utilizzare questo valore per passare una struttura di dati alla routine della finestra. Verrà illustrato un modo possibile per usare questo parametro nella sezione [gestione dello stato dell'applicazione](managing-application-state-.md).

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) restituisce un handle per la nuova finestra o zero se la funzione ha esito negativo. Per visualizzare la finestra, ovvero rendere visibile la finestra, passare l'handle della finestra alla funzione [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) :

```C++
ShowWindow(hwnd, nCmdShow);
```

Il parametro *HWND* è l'handle della finestra restituito da [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Il parametro *nCmdShow* può essere utilizzato per ridurre o ingrandire una finestra. Il sistema operativo passa questo valore al programma tramite la funzione **wWinMain** .

Ecco il codice completo per creare la finestra. Tenere presente che `WindowProc` è ancora una dichiarazione in diretta di una funzione.

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

Congratulazioni, è stata creata una finestra. A questo punto, la finestra non contiene contenuto né interagire con l'utente. In un'applicazione GUI reale la finestra risponderebbe agli eventi dell'utente e del sistema operativo. Nella sezione successiva viene descritto in che modo i messaggi della finestra forniscono questo tipo di interattività.

### <a name="next"></a>Prossima

[Messaggi finestra](window-messages.md)