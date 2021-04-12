---
title: Mantenimento dello stato della barra multifunzione
description: Windows Ribon Framework (barra multifunzione) offre la possibilità di mantenere lo stato di un'ampia gamma di impostazioni utente e preferenze tra le sessioni dell'applicazione.
ms.assetid: f59e36be-8e3d-454a-b93c-9fc5fc5ecb47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a3b704151b657bdfe95845c8473a0fd197e87b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338311"
---
# <a name="persisting-ribbon-state"></a>Mantenimento dello stato della barra multifunzione

Windows Ribon Framework (barra multifunzione) offre la possibilità di mantenere lo stato di un'ampia gamma di impostazioni utente e preferenze tra le sessioni dell'applicazione.

-   [Introduzione](#introduction)
-   [Un'esperienza prevedibile](#a-predictable-experience)
-   [Salva le impostazioni della barra multifunzione](#save-ribbon-settings)
-   [Caricare le impostazioni della barra multifunzione](#load-ribbon-settings)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Diversi aspetti di una barra multifunzione, incluse le preferenze di configurazione e interazione, possono essere personalizzati da un utente in fase di esecuzione per migliorare l'usabilità e la produttività. Il Framework della barra multifunzione fornisce la funzionalità per mantenere queste impostazioni tra le sessioni dell'applicazione tramite due metodi definiti nell'implementazione dell'interfaccia [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) : [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) e [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).

## <a name="a-predictable-experience"></a>Un'esperienza prevedibile

Le [linee guida sull'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx) consigliano che, per offrire l'esperienza utente più prevedibile, le applicazioni Ribbon devono mantenere lo stato della barra multifunzione (a parte l'ultima scheda selezionata) quando l'applicazione viene chiusa. In questo modo, quando viene avviata la stessa applicazione, è possibile ripristinare le impostazioni e le personalizzazioni della sessione precedente e l'utente può prevedere di continuare a interagire con l'applicazione nello stesso modo in cui è stata lasciata.

Le impostazioni della barra multifunzione che possono essere modificate in fase di esecuzione e mantenute tra le sessioni dell'applicazione sono elencate nel menu di scelta rapida del comando. e comprendono:

-   Comandi aggiunti all'elenco di comandi della [barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md) dall'utente. Specificato da un oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) tramite la chiave della proprietà [ \_ \_ ItemsSource pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-itemssource.md) .

    Lo screenshot seguente mostra il comando del menu **di scelta rapida Aggiungi a barra di accesso rapido** .

    ![screenshot del menu di scelta rapida del comando sulla barra multifunzione di Microsoft Paint.](images/controls/qat-contextmenu-add.png)

-   Stato di ancoraggio della [barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md) preferito. Specificata dal valore [**\_ CONTROLDOCK dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) utente della chiave della proprietà [ \_ \_ QuickAccessToolbarDock pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) .

    Questa schermata mostra la barra di [accesso rapido](windowsribbon-controls-quickaccesstoolbar.md) nella posizione predefinita della barra del titolo dell'applicazione e la **barra di accesso rapido Visualizza sotto il comando del menu di scelta rapida della barra multifunzione** .

    ![screenshot del menu di scelta rapida del comando sulla barra multifunzione di Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    Questo screenshot mostra la [barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md) sotto la barra multifunzione.

    ![screenshot della barra di accesso rapido ancorata sotto la barra multifunzione.](images/controls/qat-dockbottom.png)

-   Stato ridotto a icona della barra multifunzione come specificato dal valore booleano della chiave della proprietà [ \_ ridotta a \_ icona dell'interfaccia utente pkey](windowsribbon-reference-properties-uipkey-minimized.md) .

    > [!Note]  
    > Lo stato ridotto a icona della barra multifunzione non è equivalente allo stato compresso della barra multifunzione. Quando lo stato è compresso, la barra multifunzione è completamente nascosta e non può essere interagito con. Il Framework richiama questo stato automaticamente se la dimensione della finestra dell'applicazione è ridotta, orizzontalmente o verticalmente, al punto in cui la barra multifunzione nasconde l'area di lavoro dell'applicazione. Il Framework ripristina la barra multifunzione quando vengono aumentate le dimensioni della finestra dell'applicazione.

     

    Questa schermata mostra il comando del menu di scelta rapida **della barra multifunzione** .

    ![screenshot del menu di scelta rapida del comando sulla barra multifunzione di Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    Questo screenshot mostra una barra multifunzione ridotta a icona.

    ![screenshot della barra multifunzione di Microsoft Paint ridotta a icona.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a>Salva le impostazioni della barra multifunzione

Il metodo [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) scrive una rappresentazione binaria dello stato della barra multifunzione persistente, descritta nella sezione precedente, in un oggetto [IStream](/windows/win32/api/objidl/nn-objidl-istream) . L'applicazione salva quindi il contenuto dell'oggetto IStream in un file o nel registro di sistema di Windows.

Nell'esempio seguente viene illustrato il codice di base necessario per scrivere lo stato della barra multifunzione in un oggetto [IStream](/windows/win32/api/objidl/nn-objidl-istream) usando il metodo [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .


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



## <a name="load-ribbon-settings"></a>Caricare le impostazioni della barra multifunzione

Il metodo [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) viene usato per recuperare le informazioni sullo stato della barra multifunzione permanenti archiviate come oggetto [IStream](/windows/win32/api/objidl/nn-objidl-istream) dal metodo [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) . Le informazioni nell'oggetto IStream vengono applicate all'interfaccia utente della barra multifunzione quando l'applicazione viene inizializzata.

Nell'esempio seguente viene illustrato il codice di base necessario per caricare lo stato della barra multifunzione da un oggetto [IStream](/windows/win32/api/objidl/nn-objidl-istream) con il metodo [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .


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



Per ottenere prestazioni ottimali, è necessario chiamare il metodo [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) dalla funzione di callback [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) durante la fase di inizializzazione del Framework, come illustrato nell'esempio seguente.


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



Più istanze della stessa applicazione del Framework della barra multifunzione possono gestire ogni stato della barra multifunzione indipendentemente da oggetti [IStream](/windows/win32/api/objidl/nn-objidl-istream) separati o come gruppo tramite un singolo oggetto IStream.

Quando si sincronizza lo stato della barra multifunzione in un gruppo di istanze dell'applicazione, ogni finestra di primo livello deve restare in attesa di una notifica di [ \_ attivazione WM](../inputdev/wm-activate.md) . La finestra di primo livello da disattivare Salva lo stato della barra multifunzione usando il metodo [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) e la finestra di primo livello attivata carica lo stato della barra multifunzione usando il metodo [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 