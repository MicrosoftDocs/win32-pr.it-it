---
title: Persistenza dello stato della barra multifunzione
description: Il Windows Ribon Framework (Ribbon) consente di mantenere lo stato di un'ampia gamma di impostazioni utente e preferenze tra le sessioni dell'applicazione.
ms.assetid: f59e36be-8e3d-454a-b93c-9fc5fc5ecb47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e506d1cc8138f569dc21b491cc11ed58411131c0dd80532c19043c5974995e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707953"
---
# <a name="persisting-ribbon-state"></a>Persistenza dello stato della barra multifunzione

Il Windows Ribon Framework (Ribbon) consente di mantenere lo stato di un'ampia gamma di impostazioni utente e preferenze tra le sessioni dell'applicazione.

-   [Introduzione](#introduction)
-   [Un'esperienza stimabile](#a-predictable-experience)
-   [Salvare la barra multifunzione Impostazioni](#save-ribbon-settings)
-   [Caricare la barra multifunzione Impostazioni](#load-ribbon-settings)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Diversi aspetti di una barra multifunzione, incluse le preferenze di configurazione e interazione, possono essere personalizzati da un utente in fase di esecuzione per migliorare l'usabilità e la produttività. Il framework della barra multifunzione offre la funzionalità per mantenere queste impostazioni tra le sessioni dell'applicazione tramite due metodi definiti nell'implementazione dell'interfaccia [**IUIRibbon:**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) e [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).

## <a name="a-predictable-experience"></a>Un'esperienza stimabile

Le [](https://msdn.microsoft.com/library/cc872782.aspx) linee guida sull'esperienza utente della barra multifunzione consigliano che, per offrire l'esperienza utente più prevedibile possibile, le applicazioni della barra multifunzione devono mantenere lo stato della barra multifunzione (a parte l'ultima scheda selezionata) quando l'applicazione viene chiusa. In questo modo, quando viene avviata la stessa applicazione, è possibile ripristinare le impostazioni e le personalizzazioni della sessione precedente e l'utente può aspettarsi di continuare a interagire con l'applicazione nello stesso modo in cui l'ha lasciata.

Le impostazioni della barra multifunzione che possono essere modificate in fase di esecuzione e mantenute tra le sessioni dell'applicazione sono elencate nel menu di scelta rapida Comando. includono:

-   Comandi aggiunti [all'elenco Comandi della barra](windowsribbon-controls-quickaccesstoolbar.md) di accesso rapido dall'utente. Specificato da un [**oggetto IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) tramite la chiave della proprietà [ \_ ItemsSource PKEY \_ dell'interfaccia](windowsribbon-reference-properties-uipkey-itemssource.md) utente.

    Lo screenshot seguente mostra il comando aggiungi al menu **di scelta rapida della barra** di accesso rapido.

    ![Screenshot del menu di scelta rapida dei comandi nella barra multifunzione di Microsoft Paint.](images/controls/qat-contextmenu-add.png)

-   Stato di [ancoraggio preferito della barra](windowsribbon-controls-quickaccesstoolbar.md) di accesso rapido. Specificato dal valore [**\_ CONTROLDOCK dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) utente della chiave della proprietà [UI \_ PKEY \_ QuickAccessToolbarDock.](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md)

    Questa schermata mostra la barra [di accesso rapido nella](windowsribbon-controls-quickaccesstoolbar.md) posizione predefinita della barra del titolo dell'applicazione e mostra la barra di accesso rapido sotto **il** comando del menu di scelta rapida della barra multifunzione.

    ![Screenshot del menu di scelta rapida dei comandi nella barra multifunzione di Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    Questa schermata mostra la barra [di accesso rapido sotto](windowsribbon-controls-quickaccesstoolbar.md) la barra multifunzione.

    ![Screenshot della barra di accesso rapido ancorata sotto la barra multifunzione.](images/controls/qat-dockbottom.png)

-   Stato ridotto a icona della barra multifunzione come specificato dal valore booleano della chiave della proprietà [ \_ PKEY \_ Minimized dell'interfaccia](windowsribbon-reference-properties-uipkey-minimized.md) utente.

    > [!Note]  
    > Lo stato ridotto a icona della barra multifunzione non equivale allo stato compresso della barra multifunzione. Quando è compressa, la barra multifunzione è completamente nascosta e non può essere interagita. Il framework richiama automaticamente questo stato se le dimensioni della finestra dell'applicazione sono ridotte, orizzontalmente o verticalmente, al punto che la barra multifunzione nasconde l'area di lavoro dell'applicazione. Il framework ripristina la barra multifunzione quando vengono aumentate le dimensioni della finestra dell'applicazione.

     

    Questa schermata mostra il comando **Riduci a icona del** menu di scelta rapida della barra multifunzione.

    ![Screenshot del menu di scelta rapida dei comandi nella barra multifunzione di Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    Questa schermata mostra una barra multifunzione ridotta a icona.

    ![Screenshot della barra multifunzione di Microsoft Paint ridotta a icona.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a>Salvare la barra multifunzione Impostazioni

Il [**metodo IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) scrive una rappresentazione binaria dello stato persistente della barra multifunzione (descritto nella sezione precedente) in un [oggetto IStream.](/windows/win32/api/objidl/nn-objidl-istream) L'applicazione salva quindi il contenuto dell'oggetto IStream in un file o nel Windows registro.

L'esempio seguente illustra il codice di base necessario per scrivere lo stato della barra multifunzione in un [oggetto IStream](/windows/win32/api/objidl/nn-objidl-istream) usando il [**metodo IUIRibbon::SaveSettingsToStream.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream)


```C++
// pRibbon        - Pointer to the IUIRibbon interface
// ppStatusStream - Pointer to the location of a newly created IStream object
HRESULT CApplication::SaveRibbonStatusToStream(
                        __in IUIRibbon *pRibbon, 
                        __out IStream **ppStatusStream)
{
  HRESULT hr = E_FAIL; 

  *ppStatusStream = NULL;
  IStream* pStream;
  if (SUCCEEDED(hr = CreateStreamOnHGlobal(
                       NULL,  // Internally allocate a new shared memory.
                       FALSE, // Free hGlobal after IStream object released.
                       &pStream)))
  {
    if (SUCCEEDED(hr = pRibbon->SaveSettingsToStream(*ppStatusStream)))
    {                  
      pStream->AddRef();
      *ppStatusStream = pStream;
    }
    pStream->Release();
  }
  return hr;
}
```



## <a name="load-ribbon-settings"></a>Caricare la barra multifunzione Impostazioni

Il [**metodo IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) viene usato per recuperare le informazioni sullo stato persistente della barra multifunzione archiviate come oggetto [IStream](/windows/win32/api/objidl/nn-objidl-istream) dal metodo [**IUIRibbon::SaveSettingsToStream.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) Le informazioni nell'oggetto IStream vengono applicate all'interfaccia utente della barra multifunzione quando l'applicazione viene inizializzata.

L'esempio seguente illustra il codice di base necessario per caricare lo stato della barra multifunzione da un [oggetto IStream](/windows/win32/api/objidl/nn-objidl-istream) con il [**metodo IUIRibbon::LoadSettingsFromStream.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream)


```C++
// pRibbon       - Pointer to the IUIRibbon interface
// pStatusStream - Pointer to the IStream object that contains the Ribbon state information
HRESULT CApplication::LoadRibbonStatusFromStream(
                        __in IUIRibbon *pRibbon, 
                        __in IStream *pStatusStream)
{     
  HRESULT hr = E_FAIL;
  if (pStatusStream)
  {
    // Set the stream position to the beginning first.
    LARGE_INTEGER liStart = {0, 0};
    ULARGE_INTEGER ulActual;
    pStatusStream->Seek(liStart, STREAM_SEEK_SET, &ulActual);
    hr = pRibbon->LoadSettingsFromStream(pStatusStream);
  }
  return hr;
}
```



Per prestazioni ottimali, il metodo [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) deve essere chiamato dalla funzione di callback [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) durante la fase di inizializzazione del framework, come illustrato nell'esempio seguente.


```C++
IFACEMETHODIMP CMyRibbonApplication::OnViewChanged(
                                       UINT nViewID, 
                                       __in UI_VIEWTYPE typeID, 
                                       __in IUnknown* pView, 
                                       UI_VIEWVERB verb, 
                                       INT iReasonCode)
{
  HRESULT hr = E_NOTIMPL;
  if (UI_VIEWVERB_CREATE == verb)
  {
    IUIRibbon* pRibbon = NULL;
    hr = pView->QueryInterface(IID_PPV_ARGS(&pRibbon));

    if (SUCCEEDED(hr))
    {
      hr = _LoadRibbonSettings(pRibbon);
      pRibbon->Release();
    }
  }
  return hr;
}

HRESULT CMyRibbonApplication::_LoadRibbonSettings(IUIRibbon* pRibbon)
{
  ...
  pRibbon->LoadSettingsFromStream(pStream);
  ...
}
```



Più istanze della stessa applicazione del framework della barra multifunzione possono gestire ogni stato della barra multifunzione in modo indipendente come oggetti [IStream](/windows/win32/api/objidl/nn-objidl-istream) separati o come gruppo tramite un singolo oggetto IStream.

Quando si sincronizza lo stato della barra multifunzione in un gruppo di istanze dell'applicazione, ogni finestra di primo livello deve restare in ascolto di una [notifica WM \_ ACTIVATE.](../inputdev/wm-activate.md) La finestra di primo livello disattivata salva lo stato della barra multifunzione usando il metodo [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) e la finestra di primo livello attivata carica lo stato della barra multifunzione usando il metodo [**IUIRibbon::LoadSettingsFromStream.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 