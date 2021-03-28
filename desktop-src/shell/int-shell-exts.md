---
description: Gran parte dell'implementazione di un oggetto gestore dell'estensione della shell è determinata dal tipo. Esistono, tuttavia, alcuni elementi comuni. Questo argomento descrive gli aspetti dell'implementazione condivisi da tutti i gestori di estensioni della shell.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Inizializzazione di gestori estensioni della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a27b6273c5e342dc4caf545fb3593cdad66261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980778"
---
# <a name="initializing-shell-extension-handlers"></a><span data-ttu-id="493c3-105">Inizializzazione di gestori estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="493c3-105">Initializing Shell Extension Handlers</span></span>

<span data-ttu-id="493c3-106">Gran parte dell'implementazione di un oggetto gestore dell'estensione della shell è determinata dal tipo.</span><span class="sxs-lookup"><span data-stu-id="493c3-106">Much of the implementation of a Shell extension handler object is dictated by its type.</span></span> <span data-ttu-id="493c3-107">Esistono, tuttavia, alcuni elementi comuni.</span><span class="sxs-lookup"><span data-stu-id="493c3-107">There are, however, some common elements.</span></span> <span data-ttu-id="493c3-108">Questo argomento descrive gli aspetti dell'implementazione condivisi da tutti i gestori di estensioni della shell.</span><span class="sxs-lookup"><span data-stu-id="493c3-108">This topic discusses those aspects of implementation that are shared by all Shell extension handlers.</span></span>

<span data-ttu-id="493c3-109">Tutti i gestori di estensioni della shell sono oggetti Component Object Model (COM) in-process.</span><span class="sxs-lookup"><span data-stu-id="493c3-109">All Shell extension handlers are in-process Component Object Model (COM) objects.</span></span> <span data-ttu-id="493c3-110">È necessario assegnare un GUID e registrarlo come descritto in [Registering Shell Extension Handler](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="493c3-110">They must be assigned a GUID and registered as described in [Registering Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="493c3-111">Vengono implementate come dll ed è necessario esportare le funzioni standard seguenti:</span><span class="sxs-lookup"><span data-stu-id="493c3-111">They are implemented as DLLs and must export the following standard functions:</span></span>

-   <span data-ttu-id="493c3-112">[**DllMain**](../dlls/dllmain.md).</span><span class="sxs-lookup"><span data-stu-id="493c3-112">[**DllMain**](../dlls/dllmain.md).</span></span> <span data-ttu-id="493c3-113">Il punto di ingresso standard della DLL.</span><span class="sxs-lookup"><span data-stu-id="493c3-113">The standard entry point to the DLL.</span></span>
-   <span data-ttu-id="493c3-114">[**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject).</span><span class="sxs-lookup"><span data-stu-id="493c3-114">[**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject).</span></span> <span data-ttu-id="493c3-115">Espone la class factory dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="493c3-115">Exposes the object's class factory.</span></span>
-   <span data-ttu-id="493c3-116">[**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow).</span><span class="sxs-lookup"><span data-stu-id="493c3-116">[**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow).</span></span> <span data-ttu-id="493c3-117">COM chiama questa funzione per determinare se l'oggetto serve qualsiasi client.</span><span class="sxs-lookup"><span data-stu-id="493c3-117">COM calls this function to determine whether the object is serving any clients.</span></span> <span data-ttu-id="493c3-118">In caso contrario, il sistema può scaricare la DLL e liberare la memoria associata.</span><span class="sxs-lookup"><span data-stu-id="493c3-118">If not, the system can unload the DLL and free the associated memory.</span></span>

<span data-ttu-id="493c3-119">Come tutti gli oggetti COM, i gestori di estensioni della shell devono implementare un'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e un [class factory](../com/implementing-iclassfactory.md).</span><span class="sxs-lookup"><span data-stu-id="493c3-119">Like all COM objects, Shell extension handlers must implement an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface and a [class factory](../com/implementing-iclassfactory.md).</span></span> <span data-ttu-id="493c3-120">La maggior parte deve implementare anche un'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) o [**ISHELLEXTINIT**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) in Windows XP o versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="493c3-120">Most must also implement either an [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) or [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface in Windows XP or earlier.</span></span> <span data-ttu-id="493c3-121">Questi sono stati sostituiti da [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) e [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="493c3-121">These were replaced by [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) and [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista.</span></span> <span data-ttu-id="493c3-122">La shell usa queste interfacce per inizializzare il gestore.</span><span class="sxs-lookup"><span data-stu-id="493c3-122">The Shell uses these interfaces to initialize the handler.</span></span>

<span data-ttu-id="493c3-123">L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) deve essere implementata dai seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="493c3-123">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface must be implemented by the following:</span></span>

-   <span data-ttu-id="493c3-124">Gestori di icone</span><span class="sxs-lookup"><span data-stu-id="493c3-124">Icon handlers</span></span>
-   <span data-ttu-id="493c3-125">Gestori di dati</span><span class="sxs-lookup"><span data-stu-id="493c3-125">Data handlers</span></span>
-   <span data-ttu-id="493c3-126">Gestori di rilascio</span><span class="sxs-lookup"><span data-stu-id="493c3-126">Drop handlers</span></span>

<span data-ttu-id="493c3-127">L'interfaccia [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) deve essere implementata dai seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="493c3-127">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface must be implemented by the following:</span></span>

-   <span data-ttu-id="493c3-128">Gestori dei menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="493c3-128">Shortcut menu handlers</span></span>
-   <span data-ttu-id="493c3-129">Gestori di trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="493c3-129">Drag-and-drop handlers</span></span>
-   <span data-ttu-id="493c3-130">Gestori della finestra delle proprietà</span><span class="sxs-lookup"><span data-stu-id="493c3-130">Property sheet handlers</span></span>

<span data-ttu-id="493c3-131">Gli argomenti seguenti sono descritti nella parte restante di questo argomento:</span><span class="sxs-lookup"><span data-stu-id="493c3-131">The following subjects are discussed in the remainder of this topic:</span></span>

-   [<span data-ttu-id="493c3-132">Implementazione di IPersistFile</span><span class="sxs-lookup"><span data-stu-id="493c3-132">Implementing IPersistFile</span></span>](#implementing-ipersistfile)
-   [<span data-ttu-id="493c3-133">Implementazione di IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="493c3-133">Implementing IShellExtInit</span></span>](#implementing-ishellextinit)
-   [<span data-ttu-id="493c3-134">Personalizzazione di infotip</span><span class="sxs-lookup"><span data-stu-id="493c3-134">Infotip Customization</span></span>](#infotip-customization)
-   [<span data-ttu-id="493c3-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="493c3-135">Related topics</span></span>](#related-topics)

## <a name="implementing-ipersistfile"></a><span data-ttu-id="493c3-136">Implementazione di IPersistFile</span><span class="sxs-lookup"><span data-stu-id="493c3-136">Implementing IPersistFile</span></span>

<span data-ttu-id="493c3-137">L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è progettata per consentire il caricamento o il salvataggio di un oggetto in un file su disco.</span><span class="sxs-lookup"><span data-stu-id="493c3-137">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is designed to permit an object to be loaded from or saved to a disk file.</span></span> <span data-ttu-id="493c3-138">Sono disponibili sei metodi, oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), cinque dei propri e il metodo [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) che eredita da [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist).</span><span class="sxs-lookup"><span data-stu-id="493c3-138">It has six methods in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), five of its own, and the [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) method that it inherits from [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist).</span></span> <span data-ttu-id="493c3-139">Con le estensioni della shell, **IPersist** viene usato solo per inizializzare un oggetto gestore dell'estensione della shell.</span><span class="sxs-lookup"><span data-stu-id="493c3-139">With Shell extensions, **IPersist** is used only to initialize a Shell extension handler object.</span></span> <span data-ttu-id="493c3-140">Poiché in genere non è necessario leggere o scrivere sul disco, solo i metodi **GetClassID** e [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) richiedono un'implementazione non token.</span><span class="sxs-lookup"><span data-stu-id="493c3-140">Because there is typically no need to read from or write to the disk, only the **GetClassID** and [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) methods require a nontoken implementation.</span></span>

<span data-ttu-id="493c3-141">La shell chiama prima [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) e la funzione restituisce l'identificatore di classe (CLSID) dell'oggetto gestore di estensione.</span><span class="sxs-lookup"><span data-stu-id="493c3-141">The Shell calls [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) first, and the function returns the class identifier (CLSID) of the extension handler object.</span></span> <span data-ttu-id="493c3-142">La shell chiama quindi [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) e passa due valori.</span><span class="sxs-lookup"><span data-stu-id="493c3-142">The Shell then calls [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) and passes in two values.</span></span> <span data-ttu-id="493c3-143">Il primo, *pszFile*, è una stringa Unicode con il nome del file o della cartella su cui la Shell sta per operare.</span><span class="sxs-lookup"><span data-stu-id="493c3-143">The first, *pszFile*, is a Unicode string with the name of the file or folder that Shell is about to operate on.</span></span> <span data-ttu-id="493c3-144">Il secondo è *dwMode*, che indica la modalità di accesso ai file.</span><span class="sxs-lookup"><span data-stu-id="493c3-144">The second is *dwMode*, which indicates the file access mode.</span></span> <span data-ttu-id="493c3-145">Poiché in genere non è necessario accedere ai file, *dwMode* è in genere pari a zero.</span><span class="sxs-lookup"><span data-stu-id="493c3-145">Because there is normally no need to access files, *dwMode* is typically zero.</span></span> <span data-ttu-id="493c3-146">Il metodo archivia questi valori in base alle esigenze per un riferimento successivo.</span><span class="sxs-lookup"><span data-stu-id="493c3-146">The method stores these values as needed for later reference.</span></span>

<span data-ttu-id="493c3-147">Nel frammento di codice seguente viene illustrato il modo in cui un tipico gestore dell'estensione della shell implementa i metodi [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) e [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) .</span><span class="sxs-lookup"><span data-stu-id="493c3-147">The following code fragment illustrates how a typical Shell extension handler implements the [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) and [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) methods.</span></span> <span data-ttu-id="493c3-148">È progettato per gestire ANSI o Unicode.</span><span class="sxs-lookup"><span data-stu-id="493c3-148">It is designed to handle either ANSI or Unicode.</span></span> <span data-ttu-id="493c3-149">CLSID \_ SampleExtHandler è il GUID dell'oggetto gestore dell'estensione e CSampleShellExtension è il nome della classe utilizzata per implementare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="493c3-149">CLSID\_SampleExtHandler is the extension handler object's GUID, and CSampleShellExtension is the name of the class used to implement the interface.</span></span> <span data-ttu-id="493c3-150">Le variabili **m \_ szFileName** e **m \_ dwMode** sono variabili private utilizzate per archiviare i flag di accesso e il nome del file.</span><span class="sxs-lookup"><span data-stu-id="493c3-150">The **m\_szFileName** and **m\_dwMode** variables are private variables that are used to store the file's name and access flags.</span></span>


```C++
class CSampleShellExtension : public IPersistFile
{
    // Method declarations not included

    private:
    WCHAR m_szFileName[MAX_PATH];    // The file name
    DWORD m_dwMode;                  // The file access mode
}

IFACEMETHODIMP CSampleShellExtension::GetClassID(__out CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

IFACEMETHODIMP CSampleShellExtension::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(m_szFileName, ARRAYSIZE(m_szFileName), pszFile); 
}

// The implementation sample is continued in the next section.
```



## <a name="implementing-ishellextinit"></a><span data-ttu-id="493c3-151">Implementazione di IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="493c3-151">Implementing IShellExtInit</span></span>

<span data-ttu-id="493c3-152">L'interfaccia [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) ha un solo metodo, [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="493c3-152">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface has only one method, [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="493c3-153">Il metodo dispone di tre parametri che la shell può usare per passare vari tipi di informazioni.</span><span class="sxs-lookup"><span data-stu-id="493c3-153">The method has three parameters that the Shell can use to pass in various types of information.</span></span> <span data-ttu-id="493c3-154">I valori passati dipendono dal tipo di gestore e altri possono essere impostati su **null**.</span><span class="sxs-lookup"><span data-stu-id="493c3-154">The values passed in depend on the type of handler, and some can be set to **NULL**.</span></span>

-   <span data-ttu-id="493c3-155">*pidlFolder* include il puntatore di una cartella a un elenco di identificatori di elemento (PIDL).</span><span class="sxs-lookup"><span data-stu-id="493c3-155">*pidlFolder* holds a folder's pointer to an item identifier list (PIDL).</span></span> <span data-ttu-id="493c3-156">Si tratta di un PIDL assoluto.</span><span class="sxs-lookup"><span data-stu-id="493c3-156">This is an absolute PIDL.</span></span> <span data-ttu-id="493c3-157">Per le estensioni della finestra delle proprietà, questo valore è **null**.</span><span class="sxs-lookup"><span data-stu-id="493c3-157">For property sheet extensions, this value is **NULL**.</span></span> <span data-ttu-id="493c3-158">Per le estensioni del menu di scelta rapida, è il PIDL della cartella che contiene l'elemento di cui viene visualizzato il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="493c3-158">For shortcut menu extensions, it is the PIDL of the folder that contains the item whose shortcut menu is being displayed.</span></span> <span data-ttu-id="493c3-159">Per i gestori di trascinamento della selezione non predefiniti, è il PIDL della cartella di destinazione.</span><span class="sxs-lookup"><span data-stu-id="493c3-159">For nondefault drag-and-drop handlers, it is the PIDL of the target folder.</span></span>
-   <span data-ttu-id="493c3-160">*pDataObject* include un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) di un oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="493c3-160">*pDataObject* holds a pointer to a data object's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="493c3-161">L'oggetto dati include uno o più nomi di file nel formato [CF \_ HDROP](dragdrop.md) .</span><span class="sxs-lookup"><span data-stu-id="493c3-161">The data object holds one or more file names in [CF\_HDROP](dragdrop.md) format.</span></span>
-   <span data-ttu-id="493c3-162">*hRegKey* include una chiave del registro di sistema per l'oggetto file o il tipo di cartella.</span><span class="sxs-lookup"><span data-stu-id="493c3-162">*hRegKey* holds a registry key for the file object or folder type.</span></span>

<span data-ttu-id="493c3-163">Il metodo [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) archivia il nome file, il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) e la chiave del registro di sistema in base alle esigenze per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="493c3-163">The [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method stores the file name, [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer, and registry key as needed for later use.</span></span> <span data-ttu-id="493c3-164">Nel frammento di codice seguente viene illustrata un'implementazione di **IShellExtInit:: Initialize**.</span><span class="sxs-lookup"><span data-stu-id="493c3-164">The following code fragment illustrates an implementation of **IShellExtInit::Initialize**.</span></span> <span data-ttu-id="493c3-165">Per semplicità, in questo esempio si presuppone che l'oggetto dati contenga un solo file.</span><span class="sxs-lookup"><span data-stu-id="493c3-165">For simplicity, this example assumes that the data object contains only a single file.</span></span> <span data-ttu-id="493c3-166">In generale, l'oggetto dati potrebbe contenere più file, ognuno dei quali dovrà essere estratto.</span><span class="sxs-lookup"><span data-stu-id="493c3-166">In general, the data object might contain multiple files, each of which will need to be extracted.</span></span>


```C++
// This code continues the CSampleShellExtension sample shown in the
// "Implementing IPersistFile" section above.

class CSampleShellExtension : public IShellExtInit
{
    // Method declarations not included
    
    private:
    // IDList of the folder for extensions invoked on the folder, such as 
    // background context menu handlers or nondefault drag-and-drop handlers. 
    PIDLIST_ABSOLUTE m_pidlFolder;
    
    // The data object contains an expression of the items that the handler is 
    // being initialized for. Use SHCreateShellItemArrayFromDataObject to 
    // convert this object to an array of items. Use SHGetItemFromObject if you
    // are only interested in a single Shell item. If you need a file system
    // path, use IShellItem::GetDisplayName(SIGDN_FILESYSPATH, ...).
    IDataObject *m_pdtobj;
    
    // For context menu handlers, the registry key provides access to verb 
    // instance data that might be stored there. This is a rare feature to use 
    // so most extensions do not need this variable.
    HKEY m_hRegKey;             
}
    
// This method must be very efficient. Do not do any unnecessary work here.
// Use Initialize to acquire resources that will be used later.

IFACEMETHODIMP CSampleShellExtension::Initialize(__in_opt PCIDLIST_ABSOLUTE pidlFolder,
                                                 __in_opt IDataObject *pDataObject, 
                                                 __in_opt HKEY hRegKey) 
{ 
    // In some cases, handlers are initialized multiple times. Therefore, 
    // clear any previous state here.
    CoTaskMemFree(m_pidlFolder);
    m_pidlFolder = NULL;
    
    if (m_pdtobj)
    { 
        m_pdtobj->Release(); 
    }
    
    if (m_hRegKey)
    {
        RegCloseKey(m_hRegKey);
        m_hRegKey = NULL;
    }
    
    // Capture the inputs for use later.
    HRESULT hr = S_OK;
    
    if (pidlFolder)
    {
        m_pidlFolder = ILClone(pidlFolder);   // Make a copy to use later.
        hr = m_pidlFolder ? S_OK : E_OUTOFMEMORY;
    }
    
    if (SUCCEEDED(hr))
    {
        // If a data object pointer was passed into the method, save it and
        // extract the file name. 
        if (pDataObject) 
        { 
            m_pdtobj = pDataObject; 
            m_pdtobj->AddRef(); 
        }
    
        // It is uncommon to use the registry handle, but if you need it,
        // duplicate it now.
        if (hRegKey)
        {
            LSTATUS const result = RegOpenKeyEx(hRegKey, NULL, 0, KEY_READ, &m_hRegKey); 
            hr = HRESULT_FROM_WIN32(result);
        }
    }
    
    return hr;
}
```



## <a name="infotip-customization"></a><span data-ttu-id="493c3-167">Personalizzazione di infotip</span><span class="sxs-lookup"><span data-stu-id="493c3-167">Infotip Customization</span></span>

<span data-ttu-id="493c3-168">Esistono due modi per personalizzare infotip.</span><span class="sxs-lookup"><span data-stu-id="493c3-168">There are two ways to customize infotips.</span></span> <span data-ttu-id="493c3-169">Un modo consiste nell'implementare un oggetto che supporta [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) e quindi registrare l'oggetto sotto la sottochiave corretta nel registro di sistema (vedere di seguito).</span><span class="sxs-lookup"><span data-stu-id="493c3-169">One way is to implement an object that supports [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) and then register the object under the proper subkey in the registry (see below).</span></span> <span data-ttu-id="493c3-170">In alternativa, è possibile specificare una stringa fissa o un elenco di determinate proprietà di file da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="493c3-170">Alternatively, you can specify either a fixed string or a list of certain file properties to be displayed.</span></span>

<span data-ttu-id="493c3-171">Per visualizzare una stringa fissa per un'estensione dello spazio dei nomi, creare una sottochiave denominata **infotip** sotto la chiave CLSID dell'estensione dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="493c3-171">To display a fixed string for a namespace extension, create a subkey called **InfoTip** beneath the CLSID key of your namespace extension.</span></span> <span data-ttu-id="493c3-172">Impostare i dati della sottochiave in modo che siano la stringa che si desidera visualizzare.</span><span class="sxs-lookup"><span data-stu-id="493c3-172">Set the data of that subkey to be the string you want to be displayed.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

<span data-ttu-id="493c3-173">Per visualizzare una stringa fissa per un tipo di file, creare una sottochiave denominata **infotip** sotto la chiave **ProgID** del tipo di file per cui si vuole specificare infotip.</span><span class="sxs-lookup"><span data-stu-id="493c3-173">To display a fixed string for a file type, create a subkey called **InfoTip** beneath the **ProgID** key of the file type for which you want to supply infotips.</span></span> <span data-ttu-id="493c3-174">Impostare i dati della sottochiave in modo che siano la stringa che si desidera visualizzare.</span><span class="sxs-lookup"><span data-stu-id="493c3-174">Set the data of that subkey to be the string you want to be displayed.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

<span data-ttu-id="493c3-175">Se si vuole che la shell mostri determinate proprietà del file in infotip per un tipo di file specifico, creare una sottochiave denominata **infotip** sotto la chiave **ProgID** del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="493c3-175">If you want the Shell to show certain file properties in the infotip for a specific file type, create a subkey called **InfoTip** beneath the **ProgID** key of that file type.</span></span> <span data-ttu-id="493c3-176">Impostare i dati di tale sottochiave come un elenco delimitato da punti e virgola di nomi di proprietà canonici o {fmtid}, coppie PID dove *propName* è un nome di proprietà canonico e *{fmtid}, PID* è una [**coppia fmtid/PID**](./objects.md).</span><span class="sxs-lookup"><span data-stu-id="493c3-176">Set the data of that subkey to be a semicolon-delineated list of canonical property names or {fmtid}, pid pairs where *propname* is a canonical property name and *{fmtid},pid* is a [**FMTID/PID pair**](./objects.md).</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

<span data-ttu-id="493c3-177">È possibile utilizzare i nomi di proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="493c3-177">The following property names can be used.</span></span>



| <span data-ttu-id="493c3-178">Nome proprietà</span><span class="sxs-lookup"><span data-stu-id="493c3-178">Property Name</span></span>    | <span data-ttu-id="493c3-179">Descrizione</span><span class="sxs-lookup"><span data-stu-id="493c3-179">Description</span></span>                   | <span data-ttu-id="493c3-180">Recuperato da</span><span class="sxs-lookup"><span data-stu-id="493c3-180">Retrieved From</span></span>                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="493c3-181">Autore</span><span class="sxs-lookup"><span data-stu-id="493c3-181">Author</span></span>           | <span data-ttu-id="493c3-182">Autore del documento</span><span class="sxs-lookup"><span data-stu-id="493c3-182">Author of the document</span></span>        | [<span data-ttu-id="493c3-183">**autore di PIDSI \_**</span><span class="sxs-lookup"><span data-stu-id="493c3-183">**PIDSI\_AUTHOR**</span></span>](../stg/the-summary-information-property-set.md)                             |
| <span data-ttu-id="493c3-184">Titolo</span><span class="sxs-lookup"><span data-stu-id="493c3-184">Title</span></span>            | <span data-ttu-id="493c3-185">Titolo del documento</span><span class="sxs-lookup"><span data-stu-id="493c3-185">Title of the document</span></span>         | [<span data-ttu-id="493c3-186">**\_titolo PIDSI**</span><span class="sxs-lookup"><span data-stu-id="493c3-186">**PIDSI\_TITLE**</span></span>](../stg/the-summary-information-property-set.md)                              |
| <span data-ttu-id="493c3-187">Oggetto</span><span class="sxs-lookup"><span data-stu-id="493c3-187">Subject</span></span>          | <span data-ttu-id="493c3-188">Riepilogo oggetto</span><span class="sxs-lookup"><span data-stu-id="493c3-188">Subject summary</span></span>               | [<span data-ttu-id="493c3-189">**\_oggetto PIDSI**</span><span class="sxs-lookup"><span data-stu-id="493c3-189">**PIDSI\_SUBJECT**</span></span>](../stg/the-summary-information-property-set.md)                            |
| <span data-ttu-id="493c3-190">Commento</span><span class="sxs-lookup"><span data-stu-id="493c3-190">Comment</span></span>          | <span data-ttu-id="493c3-191">Commenti del documento</span><span class="sxs-lookup"><span data-stu-id="493c3-191">Document comments</span></span>             | <span data-ttu-id="493c3-192">[**PIDSI \_ Proprietà commento**](../stg/the-summary-information-property-set.md) o cartella/unità</span><span class="sxs-lookup"><span data-stu-id="493c3-192">[**PIDSI\_COMMENT**](../stg/the-summary-information-property-set.md) or folder/drive properties</span></span> |
| <span data-ttu-id="493c3-193">PageCount</span><span class="sxs-lookup"><span data-stu-id="493c3-193">PageCount</span></span>        | <span data-ttu-id="493c3-194">Numero di pagine</span><span class="sxs-lookup"><span data-stu-id="493c3-194">Number of pages</span></span>               | [<span data-ttu-id="493c3-195">**\_PageCount PIDSI**</span><span class="sxs-lookup"><span data-stu-id="493c3-195">**PIDSI\_PAGECOUNT**</span></span>](../stg/the-summary-information-property-set.md)                          |
| <span data-ttu-id="493c3-196">Nome</span><span class="sxs-lookup"><span data-stu-id="493c3-196">Name</span></span>             | <span data-ttu-id="493c3-197">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="493c3-197">Friendly name</span></span>                 | <span data-ttu-id="493c3-198">Visualizzazione cartelle standard</span><span class="sxs-lookup"><span data-stu-id="493c3-198">Standard folder view</span></span>                                                                      |
| <span data-ttu-id="493c3-199">OriginalLocation</span><span class="sxs-lookup"><span data-stu-id="493c3-199">OriginalLocation</span></span> | <span data-ttu-id="493c3-200">Percorso del file originale</span><span class="sxs-lookup"><span data-stu-id="493c3-200">Location of original file</span></span>     | <span data-ttu-id="493c3-201">Cartella valigetta e cartella Cestino</span><span class="sxs-lookup"><span data-stu-id="493c3-201">Briefcase folder and Recycle Bin folder</span></span>                                                   |
| <span data-ttu-id="493c3-202">DateDeleted</span><span class="sxs-lookup"><span data-stu-id="493c3-202">DateDeleted</span></span>      | <span data-ttu-id="493c3-203">Il file di data è stato eliminato</span><span class="sxs-lookup"><span data-stu-id="493c3-203">Date file was deleted</span></span>         | <span data-ttu-id="493c3-204">Cartella Cestino</span><span class="sxs-lookup"><span data-stu-id="493c3-204">Recycle Bin folder</span></span>                                                                        |
| <span data-ttu-id="493c3-205">Tipo</span><span class="sxs-lookup"><span data-stu-id="493c3-205">Type</span></span>             | <span data-ttu-id="493c3-206">Tipo di file</span><span class="sxs-lookup"><span data-stu-id="493c3-206">Type of file</span></span>                  | <span data-ttu-id="493c3-207">Visualizzazione Dettagli cartella standard</span><span class="sxs-lookup"><span data-stu-id="493c3-207">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="493c3-208">Dimensione</span><span class="sxs-lookup"><span data-stu-id="493c3-208">Size</span></span>             | <span data-ttu-id="493c3-209">Dimensioni del file</span><span class="sxs-lookup"><span data-stu-id="493c3-209">Size of file</span></span>                  | <span data-ttu-id="493c3-210">Visualizzazione Dettagli cartella standard</span><span class="sxs-lookup"><span data-stu-id="493c3-210">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="493c3-211">SyncCopyIn</span><span class="sxs-lookup"><span data-stu-id="493c3-211">SyncCopyIn</span></span>       | <span data-ttu-id="493c3-212">Uguale a OriginalLocation</span><span class="sxs-lookup"><span data-stu-id="493c3-212">Same as OriginalLocation</span></span>      | <span data-ttu-id="493c3-213">Uguale a OriginalLocation</span><span class="sxs-lookup"><span data-stu-id="493c3-213">Same as OriginalLocation</span></span>                                                                  |
| <span data-ttu-id="493c3-214">Ultima modifica</span><span class="sxs-lookup"><span data-stu-id="493c3-214">Modified</span></span>         | <span data-ttu-id="493c3-215">Data ultima modifica</span><span class="sxs-lookup"><span data-stu-id="493c3-215">Date last modified</span></span>            | <span data-ttu-id="493c3-216">Visualizzazione Dettagli cartella standard</span><span class="sxs-lookup"><span data-stu-id="493c3-216">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="493c3-217">Data di creazione</span><span class="sxs-lookup"><span data-stu-id="493c3-217">Created</span></span>          | <span data-ttu-id="493c3-218">Data creazione</span><span class="sxs-lookup"><span data-stu-id="493c3-218">Date created</span></span>                  | <span data-ttu-id="493c3-219">Visualizzazione Dettagli cartella standard</span><span class="sxs-lookup"><span data-stu-id="493c3-219">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="493c3-220">Accedere</span><span class="sxs-lookup"><span data-stu-id="493c3-220">Accessed</span></span>         | <span data-ttu-id="493c3-221">Data ultimo accesso</span><span class="sxs-lookup"><span data-stu-id="493c3-221">Date last accessed</span></span>            | <span data-ttu-id="493c3-222">Visualizzazione Dettagli cartella standard</span><span class="sxs-lookup"><span data-stu-id="493c3-222">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="493c3-223">InCartella</span><span class="sxs-lookup"><span data-stu-id="493c3-223">InFolder</span></span>         | <span data-ttu-id="493c3-224">Directory che contiene il file</span><span class="sxs-lookup"><span data-stu-id="493c3-224">Directory containing the file</span></span> | <span data-ttu-id="493c3-225">Risultati della ricerca nei documenti</span><span class="sxs-lookup"><span data-stu-id="493c3-225">Document search results</span></span>                                                                   |
| <span data-ttu-id="493c3-226">Classifica</span><span class="sxs-lookup"><span data-stu-id="493c3-226">Rank</span></span>             | <span data-ttu-id="493c3-227">Qualità della corrispondenza di ricerca</span><span class="sxs-lookup"><span data-stu-id="493c3-227">Quality of search match</span></span>       | <span data-ttu-id="493c3-228">Risultati della ricerca nei documenti</span><span class="sxs-lookup"><span data-stu-id="493c3-228">Document search results</span></span>                                                                   |
| <span data-ttu-id="493c3-229">FreeSpace</span><span class="sxs-lookup"><span data-stu-id="493c3-229">FreeSpace</span></span>        | <span data-ttu-id="493c3-230">Spazio di archiviazione disponibile</span><span class="sxs-lookup"><span data-stu-id="493c3-230">Available storage space</span></span>       | <span data-ttu-id="493c3-231">Unità disco</span><span class="sxs-lookup"><span data-stu-id="493c3-231">Disk drives</span></span>                                                                               |
| <span data-ttu-id="493c3-232">NumberOfVisits</span><span class="sxs-lookup"><span data-stu-id="493c3-232">NumberOfVisits</span></span>   | <span data-ttu-id="493c3-233">Numero di visite</span><span class="sxs-lookup"><span data-stu-id="493c3-233">Number of visits</span></span>              | <span data-ttu-id="493c3-234">Cartella Preferiti</span><span class="sxs-lookup"><span data-stu-id="493c3-234">Favorites folder</span></span>                                                                          |
| <span data-ttu-id="493c3-235">Attributi</span><span class="sxs-lookup"><span data-stu-id="493c3-235">Attributes</span></span>       | <span data-ttu-id="493c3-236">Attributi file</span><span class="sxs-lookup"><span data-stu-id="493c3-236">File Attributes</span></span>               | <span data-ttu-id="493c3-237">Visualizzazione Dettagli cartella standard</span><span class="sxs-lookup"><span data-stu-id="493c3-237">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="493c3-238">Company</span><span class="sxs-lookup"><span data-stu-id="493c3-238">Company</span></span>          | <span data-ttu-id="493c3-239">Nome azienda</span><span class="sxs-lookup"><span data-stu-id="493c3-239">Company name</span></span>                  | [<span data-ttu-id="493c3-240">**\_società PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="493c3-240">**PIDDSI\_COMPANY**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| <span data-ttu-id="493c3-241">Category</span><span class="sxs-lookup"><span data-stu-id="493c3-241">Category</span></span>         | <span data-ttu-id="493c3-242">Categoria documento</span><span class="sxs-lookup"><span data-stu-id="493c3-242">Document category</span></span>             | [<span data-ttu-id="493c3-243">**\_categoria PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="493c3-243">**PIDDSI\_CATEGORY**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| <span data-ttu-id="493c3-244">Copyright</span><span class="sxs-lookup"><span data-stu-id="493c3-244">Copyright</span></span>        | <span data-ttu-id="493c3-245">Copyright del supporto</span><span class="sxs-lookup"><span data-stu-id="493c3-245">Media copyright</span></span>               | [<span data-ttu-id="493c3-246">**\_Copyright PIDMSI**</span><span class="sxs-lookup"><span data-stu-id="493c3-246">**PIDMSI\_COPYRIGHT**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| <span data-ttu-id="493c3-247">HTMLInfoTipFile</span><span class="sxs-lookup"><span data-stu-id="493c3-247">HTMLInfoTipFile</span></span>  | <span data-ttu-id="493c3-248">File InfoTip HTML</span><span class="sxs-lookup"><span data-stu-id="493c3-248">HTML InfoTip file</span></span>             | <span data-ttu-id="493c3-249">File Desktop.ini per la cartella</span><span class="sxs-lookup"><span data-stu-id="493c3-249">Desktop.ini file for folder</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="493c3-250">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="493c3-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="493c3-251">Registrazione di gestori estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="493c3-251">Registering Shell Extension Handlers</span></span>](reg-shell-exts.md)
</dt> </dl>

 

 
