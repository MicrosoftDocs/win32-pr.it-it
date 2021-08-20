---
title: Sottoclassare i controlli
description: Se un controllo esegue quasi tutto ciò che si vuole, ma sono necessarie alcune altre funzionalità, è possibile modificare o aggiungere funzionalità al controllo originale sottoclassandolo.
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2e338deca61c4aac07fca431e77492f53f168540cfbbcf7596b8540ba5369f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168581"
---
# <a name="subclassing-controls"></a>Sottoclassare i controlli

Se un controllo esegue quasi tutto ciò che si vuole, ma sono necessarie alcune altre funzionalità, è possibile modificare o aggiungere funzionalità al controllo originale sottoclassandolo. Una sottoclasse può avere tutte le funzionalità di una classe esistente, nonché qualsiasi funzionalità aggiuntiva che si vuole assegnare.

Questo documento illustra come vengono create le sottoclassi e include gli argomenti seguenti.

-   [Sottoclassare i controlli prima ComCtl32.dll versione 6](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [Archiviazione dei dati utente](#storing-user-data)
    -   [Svantaggi dell'approccio alla sottoclasse precedente](#disadvantages-of-the-old-subclassing-approach)
-   [Sottoclassare i controlli usando ComCtl32.dll versione 6](#subclassing-controls-using-comctl32dll-version-6)
    -   [SetWindowSubclass](#setwindowsubclass)
    -   [GetWindowSubclass](#getwindowsubclass)
    -   [RemoveWindowSubclass](#removewindowsubclass)
    -   [DefSubclassProc](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a>Sottoclassare i controlli prima ComCtl32.dll versione 6

È possibile inserire un controllo in una sottoclasse e archiviare i dati utente all'interno di un controllo . Questa operazione viene utilizzata quando si usano versioni di ComCtl32.dll precedenti alla versione 6. La creazione di sottoclassi con versioni precedenti di ComCtl32.dll presenta alcuni svantaggi.

Per creare un nuovo controllo, è meglio iniziare con uno dei Windows comuni ed estenderlo in base a una particolare esigenza. Per estendere un controllo , creare un controllo e sostituire la routine della finestra esistente con una nuova. La nuova procedura intercetta i messaggi del controllo e agisce su di essi o li passa alla procedura originale per l'elaborazione predefinita. Usare la [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) o [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) per sostituire il WNDPROC del controllo. L'esempio di codice seguente illustra come sostituire un WNDPROC.


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a>Archiviazione dei dati utente

È possibile archiviare i dati utente con una singola finestra. Questi dati possono essere usati dalla nuova routine della finestra per determinare come disegnare il controllo o dove inviare determinati messaggi. Ad esempio, è possibile usare i dati per archiviare un puntatore di classe C++ alla classe che rappresenta il controllo. L'esempio di codice seguente illustra come usare [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) per archiviare i dati con una finestra.


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a>Svantaggi dell'approccio alla sottoclasse precedente

L'elenco seguente illustra alcuni degli svantaggi dell'uso dell'approccio descritto in precedenza per la sottoclassazione di un controllo.

-   La routine della finestra può essere sostituita una sola volta.
-   È difficile rimuovere una sottoclasse dopo la creazione.
-   L'associazione di dati privati a una finestra non è efficiente.
-   Per chiamare la routine successiva in una catena di sottoclassi, non è possibile eseguire il cast della routine finestra precedente e chiamarla, è necessario chiamarla usando la [**funzione CallWindowProc.**](/windows/desktop/api/winuser/nf-winuser-callwindowproca)

## <a name="subclassing-controls-using-comctl32dll-version-6"></a>Sottoclassare i controlli usando ComCtl32.dll versione 6

> [!Note]  
> ComCtl32.dll versione 6 è solo Unicode. I controlli comuni supportati da ComCtl32.dll versione 6 non devono essere sottoclassati (o superclassati) con le procedure della finestra ANSI.

 

ComCtl32.dll versione 6 contiene quattro funzioni che semplificano la creazione di sottoclassi ed eliminano gli svantaggi descritti in precedenza. Le nuove funzioni incapsulano la gestione coinvolta in più set di dati di riferimento, pertanto lo sviluppatore può concentrarsi sulle funzionalità di programmazione e non sulla gestione delle sottoclassi. Le funzioni di sottoclassazione sono:

-   [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a>SetWindowSubclass

Questa funzione viene usata per sottoclassare inizialmente una finestra. Ogni sottoclasse viene identificata in modo univoco dall'indirizzo di *pfnSubclass* e *dalla relativa uIdSubclass*. Entrambi sono parametri della [**funzione SetWindowSubclass.**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) Diverse sottoclassi possono condividere la stessa routine di sottoclasse e l'ID può identificare ogni chiamata. Per modificare i dati di riferimento, è possibile effettuare chiamate successive a **SetWindowSubclass**. Il vantaggio importante è che ogni istanza di sottoclasse ha i propri dati di riferimento.

La dichiarazione di una routine di sottoclasse è leggermente diversa da una normale routine della finestra perché include due dati aggiuntivi: l'ID della sottoclasse e i dati di riferimento. Gli ultimi due parametri della dichiarazione di funzione seguente lo mostrano.


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



Ogni volta che un messaggio viene ricevuto dalla nuova routine della finestra, vengono inclusi un ID sottoclasse e dati di riferimento.

> [!Note]  
> Tutte le stringhe passate alla routine sono stringhe Unicode anche se Unicode non è specificato come definizione del preprocessore.

 

Nell'esempio seguente viene illustrata una struttura di implementazione di una routine finestra per un controllo sottoclassato.


```
LRESULT CALLBACK OwnerDrawButtonProc(HWND hWnd, UINT uMsg, WPARAM wParam,
                               LPARAM lParam, UINT_PTR uIdSubclass, DWORD_PTR dwRefData)
{
    switch (uMsg)
    {
    case WM_PAINT:
        .
        .
        .
        return TRUE;
    // Other cases...
    } 
    return DefSubclassProc(hWnd, uMsg, wParam, lParam);
}
```



La routine della finestra può essere associata al controllo nel gestore [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) della routine della finestra di dialogo, come illustrato nell'esempio seguente.


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a>GetWindowSubclass

Questa funzione recupera informazioni su una sottoclasse. Ad esempio, è possibile usare [**GetWindowSubclass per**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) accedere ai dati di riferimento.

### <a name="removewindowsubclass"></a>RemoveWindowSubclass

Questa funzione rimuove le sottoclassi. [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) in combinazione con [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) consente di aggiungere e rimuovere in modo dinamico le sottoclassi.

### <a name="defsubclassproc"></a>DefSubclassProc

La [**funzione DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) chiama il gestore successivo nella catena di sottoclassi. La funzione recupera anche l'ID appropriato e i dati di riferimento e passa le informazioni alla routine della finestra successiva.

 

 