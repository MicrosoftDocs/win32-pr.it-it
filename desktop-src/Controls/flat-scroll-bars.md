---
title: Barre di scorrimento Flat
description: In Microsoft Internet Explorer 4,0 è stata introdotta una nuova tecnologia visiva denominata barre di scorrimento semplici.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fbbdb64aa9815cb56f5dc3bf55ffb17390db38
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730458"
---
# <a name="flat-scroll-bars"></a>Barre di scorrimento Flat

In Microsoft Internet Explorer 4,0 è stata introdotta una nuova tecnologia visiva denominata barre di scorrimento semplici. Dal punto di vista funzionale, le barre di scorrimento Flat funzionano esattamente come le barre di scorrimento standard. La differenza consiste nel fatto che è possibile personalizzare l'aspetto in modo più ampio rispetto alle barre di scorrimento standard.

Nella figura seguente è illustrata una finestra che contiene una barra di scorrimento piatta.

![Screenshot di una finestra che contiene una barra di scorrimento semplice](images/flatsb.jpg)

> [!Note]  
> Le barre di scorrimento Flat sono supportate dalle versioni Comctl32.dll da 4,71 a 5,82. Comctl32.dll versioni 6,00 e successive non supportano le barre di scorrimento flat.

 

## <a name="using-flat-scroll-bars"></a>Uso delle barre di scorrimento Flat

In questa sezione viene descritto come implementare le barre di scorrimento flat nell'applicazione.

### <a name="before-you-begin"></a>Prima di iniziare

Per usare le funzioni della barra di scorrimento Flat, è necessario includere COMmctrl. h nei file di origine e il collegamento a Comctl32. lib.

### <a name="adding-flat-scroll-bars-to-a-window"></a>Aggiunta di barre di scorrimento Flat a una finestra

Per aggiungere barre di scorrimento Flat a una finestra, chiamare [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passando l'handle alla finestra. Anziché utilizzare le funzioni della barra di scorrimento standard per modificare le barre di scorrimento, è necessario utilizzare la \_ funzione equivalente FlatSB xxx. Sono disponibili funzioni barra di scorrimento semplice per l'impostazione e il recupero delle informazioni di scorrimento, dell'intervallo e della posizione. Se le barre di scorrimento semplice non sono state inizializzate per la finestra, l'API della barra di scorrimento flat verrà rinviata alle funzioni standard corrispondenti, se usate. In questo modo è possibile attivare e disattivare le barre di scorrimento piatte senza dover scrivere codice condizionale.

Poiché un'applicazione potrebbe avere impostato metriche personalizzate per le barre di scorrimento Flat, non vengono aggiornate automaticamente quando le metriche di sistema cambiano. Quando le metriche della barra di scorrimento del sistema cambiano, viene trasmesso un messaggio [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) con il relativo *wParam* impostato su [**SPI \_ SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). Per aggiornare le barre di scorrimento Flat alle nuove metriche di sistema, le applicazioni devono gestire questo messaggio e modificare le proprietà dipendenti dalla metrica della barra di scorrimento flat in modo esplicito.

Per aggiornare le proprietà della barra di scorrimento, usare [**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop). Il frammento di codice seguente modifica le proprietà dipendenti dalla metrica della barra di scorrimento semplice nei valori di sistema correnti.


```
void FlatSB_UpdateMetrics(HWND hWnd)
{
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXVSCROLL, GetSystemMetrics(SM_CXVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHSCROLL, GetSystemMetrics(SM_CXHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVSCROLL, GetSystemMetrics(SM_CYVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYHSCROLL, GetSystemMetrics(SM_CYHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHTHUMB, GetSystemMetrics(SM_CXHTHUMB), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVTHUMB, GetSystemMetrics(SM_CYVTHUMB), TRUE);
}
```



### <a name="enhancing-flat-scroll-bars"></a>Miglioramento delle barre di scorrimento Flat

[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) consente di modificare le barre di scorrimento flat per personalizzare l'aspetto della finestra. Per le barre di scorrimento verticali è possibile modificare la larghezza della barra e l'altezza delle frecce di direzione. Per le barre di scorrimento orizzontali, è possibile modificare l'altezza della barra e la larghezza delle frecce di direzione. È anche possibile modificare il colore di sfondo delle barre di scorrimento orizzontale e verticale.

[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) consente inoltre di personalizzare il modo in cui vengono visualizzate le barre di scorrimento flat. Modificando le \_ Proprietà WSB Prop \_ VSTYLE e WSB \_ prop \_ HSTYLE è possibile impostare il tipo di barra di scorrimento che si desidera utilizzare. Sono disponibili tre stili.



|                    |                                                                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_modalità Encarta di FSB \_ | Viene visualizzata una barra di scorrimento flat standard. Quando il mouse viene spostato su un pulsante di direzione o sul pollice, tale parte della barra di scorrimento verrà visualizzata in 3D.             |
| \_modalità flat di FSB \_    | Viene visualizzata una barra di scorrimento flat standard. Quando il mouse viene spostato su un pulsante di direzione o sul pollice, tale parte della barra di scorrimento verrà visualizzata in colori invertiti. |
| \_modalità normale \_ FSB | Viene visualizzata una barra di scorrimento normale e non semplice. Non verrà applicato alcun effetto visivo speciale.                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a>Rimozione di barre di scorrimento Flat

Se si desidera rimuovere barre di scorrimento Flat dalla finestra, chiamare la funzione [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) , passando l'handle alla finestra. Questa funzione rimuove solo le barre di scorrimento semplici dalla finestra in fase di esecuzione. Quando la finestra viene distrutta, non è necessario chiamare questa funzione.

 

 