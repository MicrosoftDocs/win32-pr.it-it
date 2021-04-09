---
title: Sottoclassi di controlli
description: Se un controllo esegue quasi tutte le operazioni desiderate, ma sono necessarie altre funzionalità, è possibile modificare o aggiungere funzionalità al controllo originale eseguendo una sottoclasse.
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c013ee317ddeee6ff80dc4a26982d40d7117950
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047460"
---
# <a name="subclassing-controls"></a>Sottoclassi di controlli

Se un controllo esegue quasi tutte le operazioni desiderate, ma sono necessarie altre funzionalità, è possibile modificare o aggiungere funzionalità al controllo originale eseguendo una sottoclasse. Una sottoclasse può includere tutte le funzionalità di una classe esistente, oltre a tutte le funzionalità aggiuntive che si desidera assegnare.

Questo documento illustra come vengono create le sottoclassi e include gli argomenti seguenti.

-   [Controlli di sottoclasse prima della ComCtl32.dll versione 6](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [Archiviazione dei dati utente](#storing-user-data)
    -   [Svantaggi del vecchio approccio di sottoclassi](#disadvantages-of-the-old-subclassing-approach)
-   [Sottoclassi di controlli con ComCtl32.dll versione 6](#subclassing-controls-using-comctl32dll-version-6)
    -   [SetWindowSubclass](#setwindowsubclass)
    -   [GetWindowSubclass](#getwindowsubclass)
    -   [RemoveWindowSubclass](#removewindowsubclass)
    -   [DefSubclassProc](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a>Controlli di sottoclasse prima della ComCtl32.dll versione 6

È possibile inserire un controllo in una sottoclasse e archiviare i dati utente all'interno di un controllo. Questa operazione viene eseguita quando si usano versioni di ComCtl32.dll precedenti alla versione 6. La creazione di sottoclassi con versioni precedenti di ComCtl32.dll presenta alcuni svantaggi.

Per creare un nuovo controllo, è preferibile iniziare con uno dei controlli comuni di Windows ed estenderlo per adattarsi a una particolare esigenza. Per estendere un controllo, creare un controllo e sostituire la relativa routine della finestra esistente con una nuova. La nuova procedura intercetta i messaggi del controllo e li agisce o li passa alla procedura originale per l'elaborazione predefinita. Utilizzare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) o [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) per sostituire l'oggetto WndProc del controllo. Nell'esempio di codice seguente viene illustrato come sostituire un oggetto WNDPROC.


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a>Archiviazione dei dati utente

Potrebbe essere necessario archiviare i dati utente con una singola finestra. Questi dati possono essere utilizzati dalla nuova procedura della finestra per determinare come creare il controllo o dove inviare determinati messaggi. Ad esempio, è possibile usare i dati per archiviare un puntatore di classe C++ alla classe che rappresenta il controllo. Nell'esempio di codice seguente viene illustrato come utilizzare il metodo [**seprop**](/windows/desktop/api/winuser/nf-winuser-setpropa) per archiviare i dati con una finestra.


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a>Svantaggi del vecchio approccio di sottoclassi

Nell'elenco seguente sono riportati alcuni degli svantaggi dell'utilizzo dell'approccio descritto in precedenza per la sottoclasse di un controllo.

-   La routine della finestra può essere sostituita solo una volta.
-   È difficile rimuovere una sottoclasse dopo che è stata creata.
-   L'associazione di dati privati a una finestra non è efficiente.
-   Per chiamare la procedura successiva in una catena di sottoclassi, non è possibile eseguire il cast della precedente routine della finestra e chiamarla, è necessario chiamarla tramite la funzione [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) .

## <a name="subclassing-controls-using-comctl32dll-version-6"></a>Sottoclassi di controlli con ComCtl32.dll versione 6

> [!Note]  
> ComCtl32.dll versione 6 è solo Unicode. I controlli comuni supportati da ComCtl32.dll versione 6 non devono essere sottoclassati (o sottoclassati) con le routine della finestra ANSI.

 

ComCtl32.dll versione 6 contiene quattro funzioni che semplificano la creazione di sottoclassi ed eliminano gli svantaggi descritti in precedenza. Le nuove funzioni incapsulano la gestione di più set di dati di riferimento, pertanto lo sviluppatore può concentrarsi sulle funzionalità di programmazione e non sulla gestione delle sottoclassi. Le funzioni di sottoclasse sono:

-   [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a>SetWindowSubclass

Questa funzione viene utilizzata per eseguire inizialmente la sottoclasse di una finestra. Ogni sottoclasse è identificata in modo univoco dall'indirizzo di *pfnSubclass* e del relativo *uIdSubclass*. Entrambi sono parametri della funzione [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) . Diverse sottoclassi possono condividere la stessa routine di sottoclasse e l'ID può identificare ogni chiamata. Per modificare i dati di riferimento, è possibile effettuare chiamate successive a **SetWindowSubclass**. Il vantaggio importante è che ogni istanza della sottoclasse ha i propri dati di riferimento.

La dichiarazione di una routine di sottoclasse è leggermente diversa da una routine normale della finestra perché contiene due elementi di dati aggiuntivi: l'ID della sottoclasse e i dati di riferimento. Gli ultimi due parametri della dichiarazione di funzione seguente mostrano questo.


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



Ogni volta che un messaggio viene ricevuto dalla nuova procedura della finestra, vengono inclusi un ID sottoclasse e i dati di riferimento.

> [!Note]  
> Tutte le stringhe passate alla routine sono stringhe Unicode anche se Unicode non è specificato come definizione del preprocessore.

 

Nell'esempio seguente viene illustrata un'implementazione di scheletro di una routine della finestra per un controllo sottoclassato.


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



La procedura della finestra può essere associata al controllo nel gestore [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) della routine della finestra di dialogo, come illustrato nell'esempio seguente.


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a>GetWindowSubclass

Questa funzione recupera le informazioni su una sottoclasse. Ad esempio, è possibile usare [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) per accedere ai dati di riferimento.

### <a name="removewindowsubclass"></a>RemoveWindowSubclass

Questa funzione rimuove le sottoclassi. [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) in combinazione con [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) consente di aggiungere e rimuovere in modo dinamico le sottoclassi.

### <a name="defsubclassproc"></a>DefSubclassProc

La funzione [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) chiama il gestore successivo nella catena di sottoclassi. La funzione recupera inoltre l'ID e i dati di riferimento appropriati e passa le informazioni alla successiva routine della finestra.

 

 