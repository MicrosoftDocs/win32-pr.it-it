---
title: Barre di scorrimento flat
description: Microsoft Internet Explorer 4.0 ha introdotto una nuova tecnologia visiva denominata barre di scorrimento flat.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e56db4ee987a6d8cdc7b185f5db0f8d89540453
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423891"
---
# <a name="flat-scroll-bars"></a>Barre di scorrimento flat

Microsoft Internet Explorer 4.0 ha introdotto una nuova tecnologia visiva denominata barre di scorrimento flat. Dal punto di vista funzionale, le barre di scorrimento flat si comportano esattamente come le barre di scorrimento standard. La differenza è che è possibile personalizzarne l'aspetto in misura maggiore rispetto alle barre di scorrimento standard.

La figura seguente mostra una finestra che contiene una barra di scorrimento semplice.

![Screenshot di una finestra che contiene una barra di scorrimento semplice](images/flatsb.jpg)

> [!Note]  
> Le barre di scorrimento flat sono supportate Comctl32.dll versioni da 4.71 a 5.82. Comctl32.dll versioni 6.00 e successive non supportano barre di scorrimento flat.

 

## <a name="using-flat-scroll-bars"></a>Uso di barre di scorrimento flat

Questa sezione descrive come implementare barre di scorrimento flat nell'applicazione.

### <a name="before-you-begin"></a>Prima di iniziare

Per usare le funzioni della barra di scorrimento flat, è necessario includere Commctrl.h nei file di origine e collegarsi a Comctl32.lib.

### <a name="adding-flat-scroll-bars-to-a-window"></a>Aggiunta di barre di scorrimento flat a una finestra

Per aggiungere barre di scorrimento flat a una finestra, chiamare [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passando l'handle alla finestra. Anziché usare le funzioni standard della barra di scorrimento per modificare le barre di scorrimento, è necessario usare la funzione XXX FlatSB \_ equivalente. Sono disponibili funzioni della barra di scorrimento flat per l'impostazione e il recupero delle informazioni di scorrimento, dell'intervallo e della posizione. Se le barre di scorrimento flat non sono state inizializzate per la finestra, l'API della barra di scorrimento flat rimanda alle funzioni standard corrispondenti, se presenti. In questo modo è possibile attivare e disattivare le barre di scorrimento flat senza dover scrivere codice condizionale.

Poiché un'applicazione può aver impostato metriche personalizzate per le barre di scorrimento flat, non vengono aggiornate automaticamente quando le metriche di sistema cambiano. Quando le metriche della barra di scorrimento del sistema cambiano, viene trasmesso un messaggio [**WM \_ SETTINGCHANGE,**](/windows/desktop/winmsg/wm-settingchange) con *wParam* impostato su [**SPI \_ SETNONCLIENTMETRICS.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) Per aggiornare le barre di scorrimento flat alle nuove metriche di sistema, le applicazioni devono gestire questo messaggio e modificare in modo esplicito le proprietà dipendenti dalla metrica della barra di scorrimento flat.

Per aggiornare le proprietà della barra di scorrimento, [**usare FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop). Il frammento di codice seguente modifica le proprietà dipendenti dalla metrica di una barra di scorrimento semplice nei valori di sistema correnti.


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



### <a name="enhancing-flat-scroll-bars"></a>Miglioramento delle barre di scorrimento flat

[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) consente di modificare le barre di scorrimento flat per personalizzare l'aspetto della finestra. Per le barre di scorrimento verticali, è possibile modificare la larghezza della barra e l'altezza delle frecce di direzione. Per le barre di scorrimento orizzontali, è possibile modificare l'altezza della barra e la larghezza delle frecce di direzione. È anche possibile modificare il colore di sfondo delle barre di scorrimento orizzontale e verticale.

[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) consente anche di personalizzare la modalità di visualizzazione delle barre di scorrimento flat. Modificando le proprietà WSB PROP VSTYLE e \_ \_ WSB \_ PROP HSTYLE, è possibile impostare il tipo di barra di scorrimento \_ da usare. Sono disponibili tre stili.



|   Stile                 |   Descrizione                                                                                                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODALITÀ \_ FSB \_ ENCARTA | Viene visualizzata una barra di scorrimento semplice standard. Quando il mouse si sposta su un pulsante di direzione o sul cursore, tale parte della barra di scorrimento verrà visualizzata in 3D.             |
| FSB \_ FLAT \_ MODE    | Viene visualizzata una barra di scorrimento semplice standard. Quando il mouse si sposta su un pulsante di direzione o sul cursore, tale parte della barra di scorrimento verrà visualizzata con colori invertiti. |
| MODALITÀ REGOLARE \_ \_ FSB | Viene visualizzata una barra di scorrimento normale e nonflat. Non verrà applicato alcun effetto visivo speciale.                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a>Rimozione di barre di scorrimento flat

Per rimuovere le barre di scorrimento flat dalla finestra, chiamare la [**funzione UninitializeFlatSB,**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) passando l'handle alla finestra. Questa funzione rimuove le barre di scorrimento flat dalla finestra solo in fase di esecuzione. Non è necessario chiamare questa funzione quando la finestra viene distrutta.

 

 