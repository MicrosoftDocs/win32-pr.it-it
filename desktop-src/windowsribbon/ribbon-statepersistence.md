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
# <a name="persisting-ribbon-state"></a><span data-ttu-id="96fc7-103">Mantenimento dello stato della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="96fc7-103">Persisting Ribbon State</span></span>

<span data-ttu-id="96fc7-104">Windows Ribon Framework (barra multifunzione) offre la possibilità di mantenere lo stato di un'ampia gamma di impostazioni utente e preferenze tra le sessioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="96fc7-104">The Windows Ribon framework (Ribbon) provides the ability to preserve the state of a variety of user settings and preferences across application sessions.</span></span>

-   [<span data-ttu-id="96fc7-105">Introduzione</span><span class="sxs-lookup"><span data-stu-id="96fc7-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="96fc7-106">Un'esperienza prevedibile</span><span class="sxs-lookup"><span data-stu-id="96fc7-106">A Predictable Experience</span></span>](#a-predictable-experience)
-   [<span data-ttu-id="96fc7-107">Salva le impostazioni della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="96fc7-107">Save Ribbon Settings</span></span>](#save-ribbon-settings)
-   [<span data-ttu-id="96fc7-108">Caricare le impostazioni della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="96fc7-108">Load Ribbon Settings</span></span>](#load-ribbon-settings)
-   [<span data-ttu-id="96fc7-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="96fc7-109">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="96fc7-110">Introduzione</span><span class="sxs-lookup"><span data-stu-id="96fc7-110">Introduction</span></span>

<span data-ttu-id="96fc7-111">Diversi aspetti di una barra multifunzione, incluse le preferenze di configurazione e interazione, possono essere personalizzati da un utente in fase di esecuzione per migliorare l'usabilità e la produttività.</span><span class="sxs-lookup"><span data-stu-id="96fc7-111">Various aspects of a ribbon, including configuration and interaction preferences, can be customized by a user at run time to improve usability and productivity.</span></span> <span data-ttu-id="96fc7-112">Il Framework della barra multifunzione fornisce la funzionalità per mantenere queste impostazioni tra le sessioni dell'applicazione tramite due metodi definiti nell'implementazione dell'interfaccia [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) : [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) e [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).</span><span class="sxs-lookup"><span data-stu-id="96fc7-112">The Ribbon framework provides the functionality to preserve these settings across application sessions through two methods defined in the implementation of the [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) interface: [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) and [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).</span></span>

## <a name="a-predictable-experience"></a><span data-ttu-id="96fc7-113">Un'esperienza prevedibile</span><span class="sxs-lookup"><span data-stu-id="96fc7-113">A Predictable Experience</span></span>

<span data-ttu-id="96fc7-114">Le [linee guida sull'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx) consigliano che, per offrire l'esperienza utente più prevedibile, le applicazioni Ribbon devono mantenere lo stato della barra multifunzione (a parte l'ultima scheda selezionata) quando l'applicazione viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="96fc7-114">The [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) advise that, to provide the most predictable user experience possible, Ribbon applications should preserve the state of the ribbon (aside from the last selected tab) as the application is closed.</span></span> <span data-ttu-id="96fc7-115">In questo modo, quando viene avviata la stessa applicazione, è possibile ripristinare le impostazioni e le personalizzazioni della sessione precedente e l'utente può prevedere di continuare a interagire con l'applicazione nello stesso modo in cui è stata lasciata.</span><span class="sxs-lookup"><span data-stu-id="96fc7-115">In this way, when the same application is launched, the settings and customizations from the previous session can be restored and the user can expect to continue interacting with the application in the same way as they left it.</span></span>

<span data-ttu-id="96fc7-116">Le impostazioni della barra multifunzione che possono essere modificate in fase di esecuzione e mantenute tra le sessioni dell'applicazione sono elencate nel menu di scelta rapida del comando.</span><span class="sxs-lookup"><span data-stu-id="96fc7-116">Ribbon settings that can be modified at run time and preserved across application sessions are listed in the Command context menu.</span></span> <span data-ttu-id="96fc7-117">e comprendono:</span><span class="sxs-lookup"><span data-stu-id="96fc7-117">They include:</span></span>

-   <span data-ttu-id="96fc7-118">Comandi aggiunti all'elenco di comandi della [barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md) dall'utente.</span><span class="sxs-lookup"><span data-stu-id="96fc7-118">Commands added to the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) Command list by the user.</span></span> <span data-ttu-id="96fc7-119">Specificato da un oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) tramite la chiave della proprietà [ \_ \_ ItemsSource pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-itemssource.md) .</span><span class="sxs-lookup"><span data-stu-id="96fc7-119">Specified by an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key.</span></span>

    <span data-ttu-id="96fc7-120">Lo screenshot seguente mostra il comando del menu **di scelta rapida Aggiungi a barra di accesso rapido** .</span><span class="sxs-lookup"><span data-stu-id="96fc7-120">The following screen shot shows the **Add to Quick Access Toolbar** context menu Command.</span></span>

    ![screenshot del menu di scelta rapida del comando sulla barra multifunzione di Microsoft Paint.](images/controls/qat-contextmenu-add.png)

-   <span data-ttu-id="96fc7-122">Stato di ancoraggio della [barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md) preferito.</span><span class="sxs-lookup"><span data-stu-id="96fc7-122">The preferred [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) docking state.</span></span> <span data-ttu-id="96fc7-123">Specificata dal valore [**\_ CONTROLDOCK dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) utente della chiave della proprietà [ \_ \_ QuickAccessToolbarDock pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) .</span><span class="sxs-lookup"><span data-stu-id="96fc7-123">Specified by the [**UI\_CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) value of the [UI\_PKEY\_QuickAccessToolbarDock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) property key.</span></span>

    <span data-ttu-id="96fc7-124">Questa schermata mostra la barra di [accesso rapido](windowsribbon-controls-quickaccesstoolbar.md) nella posizione predefinita della barra del titolo dell'applicazione e la **barra di accesso rapido Visualizza sotto il comando del menu di scelta rapida della barra multifunzione** .</span><span class="sxs-lookup"><span data-stu-id="96fc7-124">This screen shot shows the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) in its default application title bar location and the **Show Quick Access Toolbar below the Ribbon** context menu Command.</span></span>

    ![screenshot del menu di scelta rapida del comando sulla barra multifunzione di Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    <span data-ttu-id="96fc7-126">Questo screenshot mostra la [barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md) sotto la barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="96fc7-126">This screen shot shows the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) below the ribbon.</span></span>

    ![screenshot della barra di accesso rapido ancorata sotto la barra multifunzione.](images/controls/qat-dockbottom.png)

-   <span data-ttu-id="96fc7-128">Stato ridotto a icona della barra multifunzione come specificato dal valore booleano della chiave della proprietà [ \_ ridotta a \_ icona dell'interfaccia utente pkey](windowsribbon-reference-properties-uipkey-minimized.md) .</span><span class="sxs-lookup"><span data-stu-id="96fc7-128">The ribbon minimized state as specified by the boolean value of the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property key.</span></span>

    > [!Note]  
    > <span data-ttu-id="96fc7-129">Lo stato ridotto a icona della barra multifunzione non è equivalente allo stato compresso della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="96fc7-129">The ribbon minimized state is not equivalent to the ribbon collapsed state.</span></span> <span data-ttu-id="96fc7-130">Quando lo stato è compresso, la barra multifunzione è completamente nascosta e non può essere interagito con.</span><span class="sxs-lookup"><span data-stu-id="96fc7-130">When in collapsed state, the ribbon is completely hidden and cannot be interacted with.</span></span> <span data-ttu-id="96fc7-131">Il Framework richiama questo stato automaticamente se la dimensione della finestra dell'applicazione è ridotta, orizzontalmente o verticalmente, al punto in cui la barra multifunzione nasconde l'area di lavoro dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="96fc7-131">The framework invokes this state automatically if the application window is reduced in size, either horizontally or vertically, to the point that the ribbon obscures the application workspace.</span></span> <span data-ttu-id="96fc7-132">Il Framework ripristina la barra multifunzione quando vengono aumentate le dimensioni della finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="96fc7-132">The framework restores the ribbon when the size of the application window is increased.</span></span>

     

    <span data-ttu-id="96fc7-133">Questa schermata mostra il comando del menu di scelta rapida **della barra multifunzione** .</span><span class="sxs-lookup"><span data-stu-id="96fc7-133">This screen shot shows the **Minimize the Ribbon** context menu Command.</span></span>

    ![screenshot del menu di scelta rapida del comando sulla barra multifunzione di Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    <span data-ttu-id="96fc7-135">Questo screenshot mostra una barra multifunzione ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="96fc7-135">This screen shot shows a minimized ribbon.</span></span>

    ![screenshot della barra multifunzione di Microsoft Paint ridotta a icona.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a><span data-ttu-id="96fc7-137">Salva le impostazioni della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="96fc7-137">Save Ribbon Settings</span></span>

<span data-ttu-id="96fc7-138">Il metodo [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) scrive una rappresentazione binaria dello stato della barra multifunzione persistente, descritta nella sezione precedente, in un oggetto [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="96fc7-138">The [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method writes a binary representation of the persistent ribbon state (outlined in the previous section) to an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object.</span></span> <span data-ttu-id="96fc7-139">L'applicazione salva quindi il contenuto dell'oggetto IStream in un file o nel registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="96fc7-139">The application then saves the content of the IStream object to a file or the Windows registry.</span></span>

<span data-ttu-id="96fc7-140">Nell'esempio seguente viene illustrato il codice di base necessario per scrivere lo stato della barra multifunzione in un oggetto [IStream](/windows/win32/api/objidl/nn-objidl-istream) usando il metodo [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .</span><span class="sxs-lookup"><span data-stu-id="96fc7-140">The following example demonstrates the basic code required to write the ribbon state to an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object using the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method.</span></span>


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



## <a name="load-ribbon-settings"></a><span data-ttu-id="96fc7-141">Caricare le impostazioni della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="96fc7-141">Load Ribbon Settings</span></span>

<span data-ttu-id="96fc7-142">Il metodo [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) viene usato per recuperare le informazioni sullo stato della barra multifunzione permanenti archiviate come oggetto [IStream](/windows/win32/api/objidl/nn-objidl-istream) dal metodo [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .</span><span class="sxs-lookup"><span data-stu-id="96fc7-142">The [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method is used to retrieve the persistent ribbon state information stored as an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object by the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method.</span></span> <span data-ttu-id="96fc7-143">Le informazioni nell'oggetto IStream vengono applicate all'interfaccia utente della barra multifunzione quando l'applicazione viene inizializzata.</span><span class="sxs-lookup"><span data-stu-id="96fc7-143">The information in the IStream object is applied to the ribbon UI when the application initializes.</span></span>

<span data-ttu-id="96fc7-144">Nell'esempio seguente viene illustrato il codice di base necessario per caricare lo stato della barra multifunzione da un oggetto [IStream](/windows/win32/api/objidl/nn-objidl-istream) con il metodo [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="96fc7-144">The following example demonstrates the basic code required to load the ribbon state from an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object with the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method.</span></span>


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



<span data-ttu-id="96fc7-145">Per ottenere prestazioni ottimali, è necessario chiamare il metodo [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) dalla funzione di callback [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) durante la fase di inizializzazione del Framework, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="96fc7-145">For optimal performance, the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method should be called from the [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) callback function during the framework initialization phase, as shown in the following example.</span></span>


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



<span data-ttu-id="96fc7-146">Più istanze della stessa applicazione del Framework della barra multifunzione possono gestire ogni stato della barra multifunzione indipendentemente da oggetti [IStream](/windows/win32/api/objidl/nn-objidl-istream) separati o come gruppo tramite un singolo oggetto IStream.</span><span class="sxs-lookup"><span data-stu-id="96fc7-146">Multiple instances of the same Ribbon framework application can manage each ribbon state independently as separate [IStream](/windows/win32/api/objidl/nn-objidl-istream) objects or as a group through a single IStream object.</span></span>

<span data-ttu-id="96fc7-147">Quando si sincronizza lo stato della barra multifunzione in un gruppo di istanze dell'applicazione, ogni finestra di primo livello deve restare in attesa di una notifica di [ \_ attivazione WM](../inputdev/wm-activate.md) .</span><span class="sxs-lookup"><span data-stu-id="96fc7-147">When synchronizing ribbon state across a group of application instances, each top-level window must listen for a [WM\_ACTIVATE](../inputdev/wm-activate.md) notification.</span></span> <span data-ttu-id="96fc7-148">La finestra di primo livello da disattivare Salva lo stato della barra multifunzione usando il metodo [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) e la finestra di primo livello attivata carica lo stato della barra multifunzione usando il metodo [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="96fc7-148">The top-level window being deactivated saves its ribbon state using the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method, and the top-level window being activated loads its ribbon state using the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96fc7-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="96fc7-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96fc7-150">Barra di accesso rapido</span><span class="sxs-lookup"><span data-stu-id="96fc7-150">Quick Access Toolbar</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 