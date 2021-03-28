---
description: L'interfaccia IHWEventHandler può essere registrata nella tabella degli oggetti in esecuzione (ROT), in modo che le applicazioni in esecuzione abbiano accesso agli eventi AutoPlay.
ms.assetid: 6FEFFB5D-DD8B-4FEA-B273-D32FC30CAFEA
title: Come usare gli eventi AutoPlay nelle applicazioni in esecuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51795a3992bdb40dde833bb3e352905efaa2be63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967438"
---
# <a name="how-to-use-autoplay-events-in-running-applications"></a><span data-ttu-id="58f79-103">Come usare gli eventi AutoPlay nelle applicazioni in esecuzione</span><span class="sxs-lookup"><span data-stu-id="58f79-103">How to Use AutoPlay Events in Running Applications</span></span>

<span data-ttu-id="58f79-104">L'interfaccia [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) può essere registrata nella tabella degli oggetti in esecuzione (ROT), in modo che le applicazioni in esecuzione abbiano accesso agli eventi AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="58f79-104">The [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface can be registered in the running object table (ROT) so that running applications have access to AutoPlay events.</span></span>

<span data-ttu-id="58f79-105">Nelle istruzioni seguenti viene descritto come utilizzare gli eventi AutoPlay nelle applicazioni in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="58f79-105">The following instructions describe how to use AutoPlay events in running applications.</span></span>

## <a name="instructions"></a><span data-ttu-id="58f79-106">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="58f79-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="58f79-107">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="58f79-107">Step 1:</span></span>

<span data-ttu-id="58f79-108">Creare un nuovo componente che implementi l'interfaccia [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .</span><span class="sxs-lookup"><span data-stu-id="58f79-108">Create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span>

### <a name="step-2"></a><span data-ttu-id="58f79-109">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="58f79-109">Step 2:</span></span>

<span data-ttu-id="58f79-110">Inizializzare il nuovo componente con il valore InitCmdLine dalla voce specifica del gestore sotto la chiave dei **gestori** .</span><span class="sxs-lookup"><span data-stu-id="58f79-110">Initialize the new component with the InitCmdLine value from the particular handler's entry under the **Handlers** key.</span></span>

<span data-ttu-id="58f79-111">Questo passaggio è necessario perché AutoPlay non chiama il metodo Initialize.</span><span class="sxs-lookup"><span data-stu-id="58f79-111">This step is required because Autoplay does not call the Initialize method.</span></span>

### <a name="step-3"></a><span data-ttu-id="58f79-112">Passaggio 3:</span><span class="sxs-lookup"><span data-stu-id="58f79-112">Step 3:</span></span>

<span data-ttu-id="58f79-113">Chiamare la funzione [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) per ottenere un moniker che rappresenta il componente e il gestore eventi che si desidera chiamare.</span><span class="sxs-lookup"><span data-stu-id="58f79-113">Call the [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) function to get a moniker that represents your component and the event handler that you want to call.</span></span>

### <a name="step-4"></a><span data-ttu-id="58f79-114">Passaggio 4:</span><span class="sxs-lookup"><span data-stu-id="58f79-114">Step 4:</span></span>

<span data-ttu-id="58f79-115">Usare il parametro *ppmoniker* per registrare il componente nella tabella ROT.</span><span class="sxs-lookup"><span data-stu-id="58f79-115">Use the *ppmoniker* parameter to register your component in the ROT.</span></span>

## <a name="remarks"></a><span data-ttu-id="58f79-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="58f79-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="58f79-117">[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) può rappresentare rischi per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="58f79-117">[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) can pose security risks.</span></span> <span data-ttu-id="58f79-118">Per informazioni su come caricare correttamente le dll con versioni diverse di Windows, vedere la documentazione di **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="58f79-118">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

```cpp
typedef HRESULT (*CREATEHARDWAREEVENTMONIKER)(REFCLSID clsid, LPCWSTR pszEventHandler, IMoniker **ppmoniker);

HRESULT RegisterComponent(IUnknown* punk, DWORD* dpwToken)
{
    HRESULT hr = E_FAIL;
    HINSTANCE hinstShSvcs = LoadLibrary(TEXT("shsvcs.dll"));
    
    if (hinstShSvcs)
    {   
        CREATEHARDWAREEVENTMONIKER fct = (CREATEHARDWAREEVENTMONIKER)GetProcAddress(hinstShSvcs, "CreateHardwareEventMoniker");
        if (fct)
        {
            IMoniker* pmoniker;
            
            hr = fct(CLSID_App, TEXT("VideoCameraArrival"), &pmoniker);

            if (SUCCEEDED(hr))
            {
                IRunningObjectTable *prot;
                    
                if (SUCCEEDED(GetRunningObjectTable(0, &prot)))
                {
                    hr = prot->Register(ROTFLAGS_ALLOWANYCLIENT | ROTFLAGS_REGISTRATIONKEEPSALIVE, punk, pmoniker, &_dwRegisterROT);
                    prot->Release();
                }
                pmoniker->Release();
            }
            CoRegisterClassObject(CLSID_App, static_cast<IClassFactory *>(this), CLSCTX_LOCAL_SERVER, REGCLS_MULTIPLEUSE, &_dwRegisterClass;
        }
        FreeLibrary(hinstShSvcs);
    }
    return hr;
}
```

<span data-ttu-id="58f79-119">Per la chiamata a [**IRunningObjectTable:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) è necessario che il componente includa le seguenti informazioni **AppID** nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="58f79-119">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that the component have the following **AppID** information in the registry.</span></span>

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="related-topics"></a><span data-ttu-id="58f79-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58f79-120">Related topics</span></span>

[<span data-ttu-id="58f79-121">**IHWEventHandler**</span><span class="sxs-lookup"><span data-stu-id="58f79-121">**IHWEventHandler**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[<span data-ttu-id="58f79-122">**CreateHardwareEventMoniker**</span><span class="sxs-lookup"><span data-stu-id="58f79-122">**CreateHardwareEventMoniker**</span></span>](createhardwareeventmoniker.md)
