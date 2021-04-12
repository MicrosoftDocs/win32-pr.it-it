---
title: Stampa guidata online
description: La procedura guidata di stampa online di Windows Vista consente agli utenti di ordinare stampe di foto da rivenditori di stampa online.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Stampa guidata online
- icone, stampa guidata online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8536eea7a51eddb2dbb46d10c9291a60edfdc74e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337422"
---
# <a name="online-printing-wizard"></a><span data-ttu-id="c4bd8-105">Stampa guidata online</span><span class="sxs-lookup"><span data-stu-id="c4bd8-105">Online Printing Wizard</span></span>

<span data-ttu-id="c4bd8-106">La procedura guidata di stampa online di Windows Vista consente agli utenti di ordinare stampe di foto da rivenditori di stampa online.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-106">The Windows Vista Online Printing Wizard helps users order prints of photos from participating online printing retailers.</span></span> <span data-ttu-id="c4bd8-107">Questa procedura guidata è progettata in modo da poter essere richiamata a livello di codice da qualsiasi applicazione che desideri offrire agli utenti la possibilità di ordinare stampe di foto.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-107">This wizard is designed so that it can be invoked programmatically by any application that wants to offer users the ability to order prints of photos.</span></span> <span data-ttu-id="c4bd8-108">La stampa guidata foto è disponibile in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-108">The Photo Printing Wizard is available on Windows Vista.</span></span> <span data-ttu-id="c4bd8-109">PIX per Windows</span><span class="sxs-lookup"><span data-stu-id="c4bd8-109">PIX for Windows</span></span>

-   [<span data-ttu-id="c4bd8-110">Funzionalità fornite dalla procedura guidata di stampa online</span><span class="sxs-lookup"><span data-stu-id="c4bd8-110">Features Provided by the Online Print Wizard</span></span>](#features-provided-by-the-online-print-wizard)
-   [<span data-ttu-id="c4bd8-111">Formati di file di foto supportati</span><span class="sxs-lookup"><span data-stu-id="c4bd8-111">Supported Photo File Formats</span></span>](#supported-photo-file-formats)
-   [<span data-ttu-id="c4bd8-112">Avvio a livello di codice della procedura guidata di stampa online</span><span class="sxs-lookup"><span data-stu-id="c4bd8-112">Programmatically Launching the Online Print Wizard</span></span>](#programmatically-launching-the-online-print-wizard)
-   [<span data-ttu-id="c4bd8-113">Accesso all'icona della procedura guidata di stampa online</span><span class="sxs-lookup"><span data-stu-id="c4bd8-113">Accessing the Online Print Wizard Icon</span></span>](#accessing-the-online-print-wizard-icon)
-   [<span data-ttu-id="c4bd8-114">Proprietà MRU della procedura guidata di stampa online</span><span class="sxs-lookup"><span data-stu-id="c4bd8-114">Online Print Wizard MRU Properties</span></span>](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a><span data-ttu-id="c4bd8-115">Funzionalità fornite dalla procedura guidata di stampa online</span><span class="sxs-lookup"><span data-stu-id="c4bd8-115">Features Provided by the Online Print Wizard</span></span>

<span data-ttu-id="c4bd8-116">La procedura guidata di stampa online di Windows Vista consente agli utenti di ordinare le stampe da una selezione di rivenditori di stampa online.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-116">The Windows Vista Online Printing Wizard enables users to order prints from a selection of participating online printing retailers.</span></span> <span data-ttu-id="c4bd8-117">Quando viene richiamato, la procedura guidata:</span><span class="sxs-lookup"><span data-stu-id="c4bd8-117">When invoked, the wizard:</span></span>

1.  <span data-ttu-id="c4bd8-118">Accetta un file o un elenco di file per cui è necessario ordinare le stampe.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-118">Accepts a file or list of files for which prints are to be ordered.</span></span>
2.  <span data-ttu-id="c4bd8-119">Recupera automaticamente l'elenco corrente dei rivenditori di stampa online partecipanti e consente all'utente di selezionare il rivenditore da cui acquistare le stampe foto.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-119">Automatically retrieves the current list of participating online printing retailers, and enables the user to select the retailer from which to purchase the photo prints.</span></span>
3.  <span data-ttu-id="c4bd8-120">Guida l'utente attraverso il processo o Ordina le stampe.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-120">Guides the user through the process or ordering prints.</span></span>

<span data-ttu-id="c4bd8-121">Qualsiasi applicazione può trarre vantaggio dalle funzionalità offerte dalla procedura guidata di stampa online di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-121">Any application can benefit from the features offered by the Windows Vista Online Printing Wizard.</span></span> <span data-ttu-id="c4bd8-122">Un'applicazione deve passare solo il file o i file per i quali verranno ordinate le stampe e la procedura guidata guiderà l'utente attraverso il processo di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-122">An application need only pass in the file or files for which prints will be ordered, and the wizard guides the user through the ordering process.</span></span>

<span data-ttu-id="c4bd8-123">Nella figura seguente viene illustrata la procedura guidata di stampa online di Windows Vista che visualizza un elenco di esempio dei rivenditori di stampa online partecipanti.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-123">The following figure shows the Windows Vista Online Printing Wizard displaying an example list of participating online printing retailers.</span></span>

![procedura guidata di stampa online di Windows Vista](images/opw.png)

## <a name="supported-photo-file-formats"></a><span data-ttu-id="c4bd8-125">Formati di file di foto supportati</span><span class="sxs-lookup"><span data-stu-id="c4bd8-125">Supported Photo File Formats</span></span>

<span data-ttu-id="c4bd8-126">La procedura guidata di stampa online di Windows Vista supporta qualsiasi formato di file di immagine per cui è installato un codec di Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="c4bd8-126">The Windows Vista Online Printing Wizard supports any image file format for which a Windows Imaging Component (WIC) codec is installed.</span></span> <span data-ttu-id="c4bd8-127">WIC fornisce diversi codec standard, tra cui:</span><span class="sxs-lookup"><span data-stu-id="c4bd8-127">WIC provides several standard codecs, including:</span></span>

-   <span data-ttu-id="c4bd8-128">Bitmap (BMP)</span><span class="sxs-lookup"><span data-stu-id="c4bd8-128">Bitmap (BMP)</span></span>
-   <span data-ttu-id="c4bd8-129">Graphics Interchange Format (GIF)</span><span class="sxs-lookup"><span data-stu-id="c4bd8-129">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="c4bd8-130">Formato dell'icona (ICO)</span><span class="sxs-lookup"><span data-stu-id="c4bd8-130">Icon Format (ICO)</span></span>
-   <span data-ttu-id="c4bd8-131">Joint Photographic Experts Group (JPEG)</span><span class="sxs-lookup"><span data-stu-id="c4bd8-131">Joint Photographic Experts Group (JPEG)</span></span>
-   <span data-ttu-id="c4bd8-132">Portable Network Graphics (PNG)</span><span class="sxs-lookup"><span data-stu-id="c4bd8-132">Portable Network Graphics (PNG)</span></span>
-   <span data-ttu-id="c4bd8-133">Tagged Image File Format (TIFF)</span><span class="sxs-lookup"><span data-stu-id="c4bd8-133">Tagged Image File Format (TIFF)</span></span>
-   <span data-ttu-id="c4bd8-134">Formato foto Windows Media</span><span class="sxs-lookup"><span data-stu-id="c4bd8-134">Windows Media Photo format</span></span>

<span data-ttu-id="c4bd8-135">Per ulteriori informazioni sui codec WIC e WIC, vedere componente per la [creazione di immagini Windows](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="c4bd8-135">For more information about WIC and WIC codecs, see [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).</span></span>

<span data-ttu-id="c4bd8-136">I formati di file supportati dai rivenditori di stampa online variano a seconda del rivenditore. è possibile che un rivenditore specifico non supporti tutti i formati di file supportati dalla procedura guidata di stampa online di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-136">File formats supported by online printing retailers vary from retailer to retailer; it is possible that a particular retailer may not support all of the file formats supported by the Windows Vista Online Printing Wizard.</span></span> <span data-ttu-id="c4bd8-137">Se l'utente tenta di ordinare le stampe in un formato non supportato dal rivenditore selezionato, la procedura guidata di stampa online di Windows vista informa l'utente che il rivenditore selezionato non supporta il formato di file inviato.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-137">If the user attempts to order prints in a format that is not supported by the selected retailer, the Windows Vista Online Printing Wizard notifies the user that the selected retailer does not support the submitted file format.</span></span>

## <a name="programmatically-launching-the-online-print-wizard"></a><span data-ttu-id="c4bd8-138">Avvio a livello di codice della procedura guidata di stampa online</span><span class="sxs-lookup"><span data-stu-id="c4bd8-138">Programmatically Launching the Online Print Wizard</span></span>

<span data-ttu-id="c4bd8-139">Per richiamare la procedura guidata di stampa online di Windows Vista, chiamare l'interfaccia [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) con l'identificatore di classe seguente (CLSID):</span><span class="sxs-lookup"><span data-stu-id="c4bd8-139">To invoke the Windows Vista Online Printing Wizard, call the [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface with the following class identifier (CLSID):</span></span>


```
CLSID_PublishDropTarget
```



<span data-ttu-id="c4bd8-140">Questo CLSID è definito in ShObjIdl. h e ShObjIdl. idl.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-140">This CLSID is defined in Shobjidl.h and Shobjidl.idl.</span></span> <span data-ttu-id="c4bd8-141">I file che devono essere elaborati dalla stampa guidata di Windows Vista sono specificati in un oggetto [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="c4bd8-141">The files to be processed by the Windows Vista Online Printing Wizard are specified in an [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) object.</span></span>

<span data-ttu-id="c4bd8-142">Nell'esempio di codice riportato di seguito viene illustrato come richiamare la procedura guidata di stampa online di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-142">The following code example demonstrates how to invoke the Windows Vista Online Printing Wizard.</span></span>


```
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PublishDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



## <a name="accessing-the-online-print-wizard-icon"></a><span data-ttu-id="c4bd8-143">Accesso all'icona della procedura guidata di stampa online</span><span class="sxs-lookup"><span data-stu-id="c4bd8-143">Accessing the Online Print Wizard Icon</span></span>

<span data-ttu-id="c4bd8-144">La procedura guidata stampa online di Windows Vista consente di esportare un'icona accessibile e visualizzata dalle applicazioni che lo chiamano.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-144">The Windows Vista Online Printing Wizard exports an icon that can be accessed and displayed by applications which call it.</span></span> <span data-ttu-id="c4bd8-145">Nella figura seguente viene illustrata l'icona della procedura guidata di stampa online di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-145">The following figure shows the Windows Vista Online Printing Wizard icon.</span></span>

![icona della procedura guidata di stampa online di Windows Vista](images/opw-icon.png)

<span data-ttu-id="c4bd8-147">Nell'esempio di codice seguente viene illustrato come recuperare l'indice per l'icona della procedura guidata di stampa online di Windows Vista leggendo la proprietà **OPWIcon** .</span><span class="sxs-lookup"><span data-stu-id="c4bd8-147">The following code example demonstrates how to retrieve the index for the Windows Vista Online Printing Wizard icon by reading the **OPWIcon** property.</span></span>


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;

spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

// Read the icon index from the properties set. 
CComVariant vtIcon;
int nIndex;
hr = spPropsBag->Read(L"OPWIcon", &vtIcon, NULL);

if SUCCEEDED(hr)
{
    nIndex = vtIcon.lVal;
}
```



## <a name="online-print-wizard-mru-properties"></a><span data-ttu-id="c4bd8-148">Proprietà MRU della procedura guidata di stampa online</span><span class="sxs-lookup"><span data-stu-id="c4bd8-148">Online Print Wizard MRU Properties</span></span>

<span data-ttu-id="c4bd8-149">La procedura guidata di stampa online di Windows Vista definisce tre proprietà correlate al rivenditore di stampa online usato più di recente (MRU).</span><span class="sxs-lookup"><span data-stu-id="c4bd8-149">The Windows Vista Online Printing Wizard defines three properties that are related to the most recently used (MRU) online printing retailer.</span></span>



| <span data-ttu-id="c4bd8-150">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="c4bd8-150">Property Name</span></span> | <span data-ttu-id="c4bd8-151">Valore/funzione della proprietà</span><span class="sxs-lookup"><span data-stu-id="c4bd8-151">Property Value/Function</span></span>                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4bd8-152">**MRUIcon**</span><span class="sxs-lookup"><span data-stu-id="c4bd8-152">**MRUIcon**</span></span>   | <span data-ttu-id="c4bd8-153">L'indice dell'icona per il rivenditore di stampa online usato più di recente può essere letto da questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-153">The index of the icon for the most recently used online printing retailer can be read from this property.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="c4bd8-154">**MRUName**</span><span class="sxs-lookup"><span data-stu-id="c4bd8-154">**MRUName**</span></span>   | <span data-ttu-id="c4bd8-155">Il nome del rivenditore di stampa online usato più di recente può essere letto da questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-155">The name of the most recently used online printing retailer can be read from this property.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="c4bd8-156">**UseMRU**</span><span class="sxs-lookup"><span data-stu-id="c4bd8-156">**UseMRU**</span></span>    | <span data-ttu-id="c4bd8-157">Un valore di **variabile** **VT \_ bool** che indica se la procedura guidata deve ignorare la pagina di selezione del rivenditore di stampa online e usare invece il rivenditore di stampa online usato più di recente.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-157">A **VARIANT** **VT\_BOOL** value indicating whether the wizard should skip the online printing retailer selection page, and just use the most recently used online printing retailer instead.</span></span> <span data-ttu-id="c4bd8-158">Impostare questa proprietà su **Variant \_ true** per ignorare la pagina di selezione del rivenditore.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-158">Set this property to **VARIANT\_TRUE** to skip the retailer selection page.</span></span> |



 

<span data-ttu-id="c4bd8-159">Nell'esempio di codice seguente viene illustrato come impostare la proprietà UseMRU in modo che la procedura guidata di stampa online di Windows Vista ignori la pagina di selezione del rivenditore di stampa online e selezioni automaticamente il rivenditore usato più di recente.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-159">The following code example demonstrates how to set the UseMRU property so the Windows Vista Online Printing Wizard bypasses the online printing retailer selection page and automatically selects the most recently used retailer.</span></span>


```
// A data object that contains the list of photos to order prints for.
IDataObject* pDataObject;

// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Set the UserMRU property to true to skip retailer selection and use 
// the MRU retailer instead.    
CComQIPtr<IPropertyBag> spPropsBag(spDropTarget);
if(spPropsBag) 
{
    VARIANT varTrue = {0};
    varTrue.vt = VT_BOOL;
    varTrue.boolVal = VARIANT_TRUE;
    spPropsBag->Write(L"UseMRU", &varTrue);
}

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);
```



<span data-ttu-id="c4bd8-160">Nell'esempio di codice riportato di seguito viene illustrato come leggere le proprietà MRUName e MRUIcon.</span><span class="sxs-lookup"><span data-stu-id="c4bd8-160">The following code example demonstrates how to read the MRUName and MRUIcon properties.</span></span>


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;
spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

CComVariant vtMRUName, vtMRUIconIndex;
CComBSTR bstrMRUName;
int nMRUIconIndex;

// Get the MRU name value.
hr = spPropsBag->Read(L"MRUName", &vtMRUName, NULL);
if SUCCEEDED(hr) 
{
    bstrMRUName = vtMRUName.bstrVal;
}

// Get the MRU icon index value.
hr = spPropsBag->Read(L"MRUIcon", &vtMRUIconIndex, NULL);
if SUCCEEDED(hr)
{
    nMRUIconIndex = vtMRUIconIndex.lVal;
}
```



 

 