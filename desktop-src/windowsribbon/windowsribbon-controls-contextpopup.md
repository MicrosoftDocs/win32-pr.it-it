---
title: Popup del contesto
description: Un popup di contesto è il controllo principale nella visualizzazione ContextPopup del framework Windows della barra multifunzione.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15424aa8b2b82580218eb3663e4b157bce321fdde027e03101ce2cf38626aac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964415"
---
# <a name="context-popup"></a>Popup del contesto

Un popup di contesto è il controllo principale nella [**visualizzazione ContextPopup**](windowsribbon-element-contextpopup.md) del framework Windows della barra multifunzione. Si tratta di un sistema di menu di scelta rapida completo esposto solo dal framework come estensione a un'implementazione della barra multifunzione. Il framework non espone il popup di contesto come controllo indipendente.

-   [Componenti del popup di contesto](#context-popup)
-   [Implementare il popup di contesto](#implement-the-context-popup)
    -   [markup](#markup)
    -   [Codice](#code)
-   [Proprietà popup di contesto](#context-popup-properties)
-   [Argomenti correlati](#related-topics)

## <a name="components-of-the-context-popup"></a>Componenti del popup di contesto

Context Popup è un contenitore logico per il menu di scelta rapida e Mini-Toolbar sotto-controlli esposti rispettivamente tramite gli elementi di markup [**ContextMenu**](windowsribbon-element-contextmenu.md) e [**MiniToolbar:**](windowsribbon-element-minitoolbar.md)

-   [**ContextMenu**](windowsribbon-element-contextmenu.md) espone un menu di comandi e raccolte.
-   [**MiniToolbar espone**](windowsribbon-element-minitoolbar.md) una barra degli strumenti mobile di vari comandi, raccolte e controlli complessi, ad esempio il controllo [Carattere](windowsribbon-controls-fontcontrol.md) e la [casella combinata.](windowsribbon-controls-combobox.md)

Ogni sotto-controllo può essere visualizzato al massimo una volta in un popup di contesto.

La schermata seguente illustra il popup di contesto e i relativi sotto-controlli costitutivi.

![Screenshot con callout che mostrano i componenti contestuali dell'interfaccia utente della barra multifunzione.](images/controls/contextpopup.png)

Context Popup è puramente concettuale e non espone alcuna funzionalità dell'interfaccia utente, ad esempio il posizionamento o il ridimensionamento.

> [!Note]  
> Il popup di contesto viene in genere visualizzato facendo clic con il pulsante destro del mouse (o tramite i tasti di scelta rapida MAIUSC+F10) su un oggetto di interesse. Tuttavia, i passaggi necessari per visualizzare il popup di contesto sono definiti dall'applicazione.

 

## <a name="implement-the-context-popup"></a>Implementare il popup di contesto

Analogamente ad altri controlli Windows del framework della barra multifunzione, Context Popup viene implementato tramite un componente di markup che specifica i dettagli della presentazione e un componente di codice che ne regola le funzionalità.

Nella tabella seguente sono elencati i controlli supportati da ogni sotto-controllo Popup di contesto.



| Control                                                                  | Mini-Toolbar | Menu di scelta rapida |
|--------------------------------------------------------------------------|--------------|--------------|
| [Button](windowsribbon-controls-button.md)                              | x            | x            |
| [Casella di controllo](windowsribbon-controls-checkbox.md)                         | x            | x            |
| [ComboBox](windowsribbon-controls-combobox.md)                         | x            |              |
| [Pulsante a discesa](windowsribbon-controls-dropdownbutton.md)            | x            | x            |
| [Elenco a discesa Selezione colori](windowsribbon-controls-dropdowncolorpicker.md) | x            | x            |
| [Raccolta a discesa](windowsribbon-controls-dropdowngallery.md)          | x            | x            |
| [Controllo Carattere](windowsribbon-controls-fontcontrol.md)                   | x            |              |
| [Pulsante ?](windowsribbon-controls-helpbutton.md)                     |              |              |
| [Raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md)          |              |              |
| [Spinner](windowsribbon-controls-spinner.md)                            |              |              |
| [Pulsante Dividi](windowsribbon-controls-splitbutton.md)                   | x            | x            |
| [Raccolta pulsanti di divisione](windowsribbon-controls-splitbuttongallery.md)    | x            | x            |
| [Interruttore](windowsribbon-controls-togglebutton.md)                 | x            | x            |



 

### <a name="markup"></a>markup

Ogni sotto-controllo Popup di contesto deve essere dichiarato singolarmente nel markup.

### <a name="mini-toolbar"></a>Mini-Toolbar

Quando si aggiungono controlli a una barra degli strumenti popup di contesto, è necessario prendere in considerazione le due raccomandazioni seguenti:

-   I controlli devono essere altamente riconoscibili e fornire funzionalità ovvie. La familiarità è fondamentale, perché le etichette e le descrizioni comando non vengono esposte per Mini-Toolbar controlli.
-   Ogni comando esposto da un controllo deve essere presentato altrove nell'interfaccia utente della barra multifunzione. Il Mini-Toolbar non supporta la navigazione tramite tastiera.

L'esempio seguente illustra il markup di base per un [**elemento MiniToolbar**](windowsribbon-element-minitoolbar.md) che contiene tre [controlli Button.](windowsribbon-controls-button.md)

> [!Note]  
> Viene [**specificato un elemento MenuGroup**](windowsribbon-element-menugroup.md) per ogni riga di controlli nella barra degli strumenti rapida.

 


```C++
<MiniToolbar Name="MiniToolbar">
  <MenuGroup>
    <Button CommandName="cmdButton1" />
    <Button CommandName="cmdButton2" />
    <Button CommandName="cmdButton3" />
  </MenuGroup>
</MiniToolbar>
```



### <a name="context-menu"></a>Menu di scelta rapida

L'esempio seguente illustra il markup di base per [**un elemento ContextMenu**](windowsribbon-element-contextmenu.md) che contiene tre [controlli](windowsribbon-controls-button.md) Button.

> [!Note]  
> Ogni set di controlli [**nell'elemento MenuGroup**](windowsribbon-element-menugroup.md) è separato da una barra orizzontale nel menu di scelta rapida.

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



Anche se un popup di contesto può contenere al massimo uno di ogni sotto-controllo, sono valide più dichiarazioni di elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) e [**MiniToolbar**](windowsribbon-element-minitoolbar.md) nel markup della barra multifunzione. Ciò consente a un'applicazione di supportare varie combinazioni di menu di scelta rapida e controlli Mini-Toolbar, in base ai criteri definiti dall'applicazione, ad esempio il contesto dell'area di lavoro.

Per altre informazioni, vedere [**l'elemento ContextMap.**](windowsribbon-element-contextmap.md)

Nell'esempio seguente viene illustrato il markup di base per [**l'elemento ContextPopup.**](windowsribbon-element-contextpopup.md)


```C++
<ContextPopup>
  <ContextPopup.MiniToolbars>
    <MiniToolbar Name="MiniToolbar">
      <MenuGroup>
        <Button CommandName="cmdButton1" />
        <Button CommandName="cmdButton2" />
        <Button CommandName="cmdButton3" />
      </MenuGroup>
    </MiniToolbar>
  </ContextPopup.MiniToolbars>
  <ContextPopup.ContextMenus>
    <ContextMenu Name="ContextMenu">
      <MenuGroup>
        <Button CommandName="cmdCut" />
        <Button CommandName="cmdCopy" />
        <Button CommandName="cmdPaste" />
      </MenuGroup>
    </ContextMenu>
  </ContextPopup.ContextMenus>
  <ContextPopup.ContextMaps>
    <ContextMap CommandName="cmdContextMap" ContextMenu="ContextMenu" MiniToolbar="MiniToolbar"/>
  </ContextPopup.ContextMaps>
</ContextPopup>
```



### <a name="code"></a>Codice

Per richiamare un popup di contesto, il [**metodo IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) viene chiamato quando la finestra di primo livello dell'applicazione barra multifunzione riceve una notifica WM \_ CONTEXTMENU.

Questo esempio illustra come gestire la notifica WM \_ CONTEXTMENU nel metodo WndProc() dell'applicazione barra multifunzione.


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



L'esempio seguente illustra come un'applicazione barra multifunzione può visualizzare il popup di contesto in una posizione specifica dello schermo usando il [**metodo IUIContextualUI::ShowAtLocation.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation)

GetCurrentContext() ha un valore `cmdContextMap` di come definito nell'esempio di markup precedente.

g \_ pApplication è un riferimento all'interfaccia [**IUIFramework.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)


```C++
HRESULT ShowContextualUI(POINT& ptLocation, HWND hWnd)
{
  GetDisplayLocation(ptLocation, hWnd);

  HRESULT hr = E_FAIL;

  IUIContextualUI* pContextualUI = NULL;
 
  if (SUCCEEDED(g_pFramework->GetView(
                                g_pApplication->GetCurrentContext(), 
                                IID_PPV_ARGS(&pContextualUI))))
  {
    hr = pContextualUI->ShowAtLocation(ptLocation.x, ptLocation.y);
    pContextualUI->Release();
  }

  return hr;
}
```



Il riferimento a [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) può essere rilasciato prima che context Popup venga chiuso, come illustrato nell'esempio precedente. Tuttavia, il riferimento deve essere rilasciato a un certo punto per evitare perdite di memoria.

> [!Caution]  
> Il Mini-Toolbar ha un effetto di dissolvenza incorporato basato sulla prossimità del puntatore del mouse. Per questo motivo, è consigliabile che il Mini-Toolbar visualizzato il più vicino possibile al puntatore del mouse. In caso contrario, a causa dei meccanismi di visualizzazione in conflitto, il Mini-Toolbar potrebbe non essere visualizzato come previsto.

 

## <a name="context-popup-properties"></a>Proprietà popup di contesto

Non sono presenti chiavi di proprietà associate al controllo Context Popup.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Libreria di controlli Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[Esempio di ContextPopup](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 