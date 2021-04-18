---
title: Popup contesto
description: Un popup del contesto è il controllo principale nella visualizzazione ContextPopup del Framework della barra multifunzione di Windows.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77441cc3cdcc9212d27d2230d76d2618f1831ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300052"
---
# <a name="context-popup"></a>Popup contesto

Un popup del contesto è il controllo principale nella [**visualizzazione ContextPopup**](windowsribbon-element-contextpopup.md) del Framework della barra multifunzione di Windows. Si tratta di un sistema di menu di scelta rapida che viene esposto solo dal Framework come estensione di un'implementazione della barra multifunzione: il Framework non espone il popup del contesto come controllo indipendente.

-   [Componenti del popup di contesto](#context-popup)
-   [Implementare il popup del contesto](#implement-the-context-popup)
    -   [markup](#markup)
    -   [Codice](#code)
-   [Proprietà popup del contesto](#context-popup-properties)
-   [Argomenti correlati](#related-topics)

## <a name="components-of-the-context-popup"></a>Componenti del popup di contesto

Il popup del contesto è un contenitore logico per il menu di scelta rapida e Mini-Toolbar i controlli secondari esposti tramite gli elementi di markup [**ContextMenu**](windowsribbon-element-contextmenu.md) e [**MiniToolbar**](windowsribbon-element-minitoolbar.md) , rispettivamente:

-   Il [**ContextMenu**](windowsribbon-element-contextmenu.md) espone un menu di comandi e raccolte.
-   [**MiniToolbar**](windowsribbon-element-minitoolbar.md) espone una barra degli strumenti mobile di diversi comandi, raccolte e controlli complessi, ad esempio il [controllo del tipo di carattere](windowsribbon-controls-fontcontrol.md) e la [casella combinata](windowsribbon-controls-combobox.md).

Ogni sottocontrollo può essere visualizzato al massimo una volta in un popup del contesto.

Lo screenshot seguente illustra il popup di contesto e i relativi controlli secondari.

![screenshot con callout che mostrano i componenti dell'interfaccia utente contestuale della barra multifunzione.](images/controls/contextpopup.png)

Il contesto popup è puramente concettuale e non espone alcuna funzionalità dell'interfaccia utente, ad esempio il posizionamento o il ridimensionamento.

> [!Note]  
> Il popup di contesto viene in genere visualizzato facendo clic con il pulsante destro del mouse (o tramite il tasto di scelta rapida MAIUSC + F10) su un oggetto di interesse. Tuttavia, i passaggi necessari per visualizzare il popup del contesto sono definiti dall'applicazione.

 

## <a name="implement-the-context-popup"></a>Implementare il popup del contesto

Analogamente ad altri controlli Framework della barra multifunzione di Windows, il popup del contesto viene implementato tramite un componente di markup che specifica i dettagli di presentazione e un componente di codice che ne determina la funzionalità.

Nella tabella seguente sono elencati i controlli supportati da ogni sottocontrollo popup del contesto.



| Control                                                                  | Mini-Toolbar | Menu di scelta rapida |
|--------------------------------------------------------------------------|--------------|--------------|
| [Button](windowsribbon-controls-button.md)                              | x            | x            |
| [Casella di controllo](windowsribbon-controls-checkbox.md)                         | x            | x            |
| [ComboBox](windowsribbon-controls-combobox.md)                         | x            |              |
| [Pulsante a discesa](windowsribbon-controls-dropdownbutton.md)            | x            | x            |
| [Selezione colori a discesa](windowsribbon-controls-dropdowncolorpicker.md) | x            | x            |
| [Raccolta a discesa](windowsribbon-controls-dropdowngallery.md)          | x            | x            |
| [Controllo carattere](windowsribbon-controls-fontcontrol.md)                   | x            |              |
| [Pulsante della Guida](windowsribbon-controls-helpbutton.md)                     |              |              |
| [Raccolta della barra multifunzione](windowsribbon-controls-inribbongallery.md)          |              |              |
| [Spinner](windowsribbon-controls-spinner.md)                            |              |              |
| [Pulsante di divisione](windowsribbon-controls-splitbutton.md)                   | x            | x            |
| [Raccolta di pulsanti di suddivisione](windowsribbon-controls-splitbuttongallery.md)    | x            | x            |
| [Interruttore](windowsribbon-controls-togglebutton.md)                 | x            | x            |



 

### <a name="markup"></a>markup

Ogni sottocontrollo popup del contesto deve essere dichiarato singolarmente nel markup.

### <a name="mini-toolbar"></a>Mini-Toolbar

Quando si aggiungono controlli a una mini barra degli strumenti popup del contesto, è necessario considerare le due raccomandazioni seguenti:

-   I controlli devono essere altamente riconoscibili e fornire funzionalità evidenti. La familiarità è chiave, perché le etichette e le descrizioni comandi non vengono esposte per i controlli Mini-Toolbar.
-   Ogni comando esposto da un controllo deve essere presentato altrove nell'interfaccia utente della barra multifunzione. Il Mini-Toolbar non supporta la navigazione da tastiera.

Nell'esempio seguente viene illustrato il markup di base per un elemento [**MiniToolbar**](windowsribbon-element-minitoolbar.md) che contiene tre controlli [Button](windowsribbon-controls-button.md) .

> [!Note]  
> Viene specificato un elemento [**MenuGroup**](windowsribbon-element-menugroup.md) per ogni riga di controlli nella mini-barra degli strumenti.

 


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

Nell'esempio seguente viene illustrato il markup di base per un elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) che contiene tre controlli [Button](windowsribbon-controls-button.md) .

> [!Note]  
> Ogni set di controlli nell'elemento [**MenuGroup**](windowsribbon-element-menugroup.md) è separato da una barra orizzontale nel menu di scelta rapida.

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



Sebbene un popup del contesto possa contenere al massimo uno di ogni sottocontrollo, sono valide più dichiarazioni di elementi [**ContextMenu**](windowsribbon-element-contextmenu.md) e [**MiniToolbar**](windowsribbon-element-minitoolbar.md) nel markup della barra multifunzione. Questo consente a un'applicazione di supportare diverse combinazioni di menu di scelta rapida e controlli Mini-Toolbar, in base ai criteri definiti dall'applicazione, ad esempio il contesto dell'area di lavoro.

Per ulteriori informazioni, vedere l'elemento [**ContextMap**](windowsribbon-element-contextmap.md) .

Nell'esempio seguente viene illustrato il markup di base per l'elemento [**ContextPopup**](windowsribbon-element-contextpopup.md) .


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

Per richiamare un popup del contesto, viene chiamato il metodo [**IUIContextualUI:: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) quando la finestra di primo livello dell'applicazione Ribbon riceve una notifica di WM \_ ContextMenu.

Questo esempio illustra come gestire la notifica di WM \_ ContextMenu nel metodo WndProc () dell'applicazione Ribbon.


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



Nell'esempio seguente viene illustrato come un'applicazione Ribbon può mostrare il popup del contesto in una posizione dello schermo specifica usando il metodo [**IUIContextualUI:: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) .

GetCurrentContext () ha un valore `cmdContextMap` come definito nell'esempio di markup precedente.

g \_ pApplication è un riferimento all'interfaccia [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) .


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



Il riferimento a [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) può essere rilasciato prima che il popup del contesto venga eliminato, come illustrato nell'esempio precedente. Tuttavia, il riferimento deve essere rilasciato a un certo punto per evitare perdite di memoria.

> [!Caution]  
> Il Mini-Toolbar dispone di un effetto di dissolvenza incorporato basato sulla prossimità del puntatore del mouse. Per questo motivo, è consigliabile che il Mini-Toolbar venga visualizzato il più vicino possibile al puntatore del mouse. In caso contrario, a causa dei meccanismi di visualizzazione in conflitto, è possibile che l'Mini-Toolbar non esegua il rendering come previsto.

 

## <a name="context-popup-properties"></a>Proprietà popup del contesto

Non sono presenti chiavi di proprietà associate al controllo popup del contesto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Libreria di controlli Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[Esempio ContextPopup](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 