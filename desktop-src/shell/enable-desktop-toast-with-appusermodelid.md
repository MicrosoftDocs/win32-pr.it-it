---
description: Questo argomento illustra come creare un collegamento per l'app, assegnargli un AppUserModelID e installarlo nella schermata Start.
title: Come abilitare le notifiche di tipo avviso popup sul desktop tramite un AppUserModelID
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BB32CD0A-99E6-47dc-A913-39A7B3027314
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: bd02a0ec6512aa7637f0d6b2b281e1b862e61d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978855"
---
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a><span data-ttu-id="7cffb-103">Come abilitare le notifiche di tipo avviso popup sul desktop tramite un AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="7cffb-103">How to enable desktop toast notifications through an AppUserModelID</span></span>

<span data-ttu-id="7cffb-104">Questo argomento illustra come creare un collegamento per l'app, assegnargli un [AppUserModelID](appids.md)e installarlo nella schermata Start.</span><span class="sxs-lookup"><span data-stu-id="7cffb-104">This topic shows you how to create a shortcut for your app, assign it an [AppUserModelID](appids.md), and install it in the Start screen.</span></span> <span data-ttu-id="7cffb-105">Si consiglia vivamente di eseguire questa operazione nell'Windows Installer piuttosto che nel codice dell'app.</span><span class="sxs-lookup"><span data-stu-id="7cffb-105">We strongly recommend that you do this in the Windows Installer rather than in your app's code.</span></span> <span data-ttu-id="7cffb-106">Senza un collegamento valido installato nella schermata Start o in **tutti i programmi**, non è possibile generare una notifica di tipo avviso popup da un'applicazione desktop.</span><span class="sxs-lookup"><span data-stu-id="7cffb-106">Without a valid shortcut installed in the Start screen or in **All Programs**, you cannot raise a toast notification from a desktop app.</span></span>

> [!Note]  
> <span data-ttu-id="7cffb-107">I metodi di esempio usati in questo argomento sono tratti dall' [esempio di toast sul desktop](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).</span><span class="sxs-lookup"><span data-stu-id="7cffb-107">The example methods used in this topic are taken from the [Desktop toast sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="7cffb-108">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="7cffb-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7cffb-109">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="7cffb-109">Technologies</span></span>

-   <span data-ttu-id="7cffb-110">COM</span><span class="sxs-lookup"><span data-stu-id="7cffb-110">COM</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7cffb-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="7cffb-111">Prerequisites</span></span>

-   <span data-ttu-id="7cffb-112">Librerie</span><span class="sxs-lookup"><span data-stu-id="7cffb-112">Libraries</span></span>
    -   <span data-ttu-id="7cffb-113">C++: Runtime. Object. lib</span><span class="sxs-lookup"><span data-stu-id="7cffb-113">C++: Runtime.object.lib</span></span>
    -   <span data-ttu-id="7cffb-114">C \# : Windows. winmd</span><span class="sxs-lookup"><span data-stu-id="7cffb-114">C\#: Windows.Winmd</span></span>
-   <span data-ttu-id="7cffb-115">C \# : Windows API Code Pack per Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="7cffb-115">C\#: Windows API Code Pack for Microsoft .NET Framework</span></span>
-   <span data-ttu-id="7cffb-116">Una versione di Microsoft Visual Studio che supporta almeno Windows 8</span><span class="sxs-lookup"><span data-stu-id="7cffb-116">A version of Microsoft Visual Studio that supports at least Windows 8</span></span>

## <a name="instructions"></a><span data-ttu-id="7cffb-117">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="7cffb-117">Instructions</span></span>

### <a name="step-1-prepare-the-shortcut-to-be-created"></a><span data-ttu-id="7cffb-118">Passaggio 1: preparare il collegamento da creare</span><span class="sxs-lookup"><span data-stu-id="7cffb-118">Step 1: Prepare the shortcut to be created</span></span>

<span data-ttu-id="7cffb-119">Questo esempio determina innanzitutto il percorso della cartella di dati dell'app dell'utente tramite la funzione [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) .</span><span class="sxs-lookup"><span data-stu-id="7cffb-119">This example first determines the path of the user's app data folder through the [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) function.</span></span> <span data-ttu-id="7cffb-120">Quindi compone il percorso completo del collegamento, determina che un collegamento con tale nome non esiste già in quel percorso e passa tali informazioni a un altro metodo che crea e installa il collegamento.</span><span class="sxs-lookup"><span data-stu-id="7cffb-120">It then composes the full path to the shortcut, determines that a shortcut of that name does not already exist at that location, and passes that information to another method which creates and installs the shortcut.</span></span>

<span data-ttu-id="7cffb-121">Si noti che il collegamento può essere distribuito per utente o per app.</span><span class="sxs-lookup"><span data-stu-id="7cffb-121">Note that the shortcut can be deployed per-user or per-app.</span></span>


```C++
HRESULT DesktopToastsApp::TryCreateShortcut()
{
    wchar_t shortcutPath[MAX_PATH];
    DWORD charWritten = GetEnvironmentVariable(L"APPDATA", shortcutPath, MAX_PATH);
    HRESULT hr = charWritten > 0 ? S_OK : E_INVALIDARG;

    if (SUCCEEDED(hr))
    {
        errno_t concatError = wcscat_s(shortcutPath, ARRAYSIZE(shortcutPath), L"\\Microsoft\\Windows\\Start Menu\\Programs\\Desktop Toasts App.lnk");
 
        hr = concatError == 0 ? S_OK : E_INVALIDARG;
        if (SUCCEEDED(hr))
        {
            DWORD attributes = GetFileAttributes(shortcutPath);
            bool fileExists = attributes < 0xFFFFFFF;

            if (!fileExists)
            {
                hr = InstallShortcut(shortcutPath);  // See step 2.
            }
            else
            {
                hr = S_FALSE;
            }
        }
    }
    return hr;
}
```



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a><span data-ttu-id="7cffb-122">Passaggio 2: creare il collegamento e installarlo nella schermata Start</span><span class="sxs-lookup"><span data-stu-id="7cffb-122">Step 2: Create the shortcut and install it in the Start screen</span></span>

<span data-ttu-id="7cffb-123">In questo esempio viene recuperato anche l'archivio delle proprietà del collegamento e viene impostata la proprietà [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) richiesta da una variabile definita in precedenza, `AppID` .</span><span class="sxs-lookup"><span data-stu-id="7cffb-123">This example also retrieves the shortcut's property store and sets the required [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property from a previously defined variable, `AppID`.</span></span>


```C++
HRESULT DesktopToastsApp::InstallShortcut(_In_z_ wchar_t *shortcutPath)
{
    wchar_t exePath[MAX_PATH];
    
    DWORD charWritten = GetModuleFileNameEx(GetCurrentProcess(), nullptr, exePath, ARRAYSIZE(exePath));

    HRESULT hr = charWritten > 0 ? S_OK : E_FAIL;
    
    if (SUCCEEDED(hr))
    {
        ComPtr<IShellLink> shellLink;
        hr = CoCreateInstance(CLSID_ShellLink, nullptr, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&shellLink));

        if (SUCCEEDED(hr))
        {
            hr = shellLink->SetPath(exePath);
            if (SUCCEEDED(hr))
            {
                hr = shellLink->SetArguments(L"");
                if (SUCCEEDED(hr))
                {
                    ComPtr<IPropertyStore> propertyStore;

                    hr = shellLink.As(&propertyStore);
                    if (SUCCEEDED(hr))
                    {
                        PROPVARIANT appIdPropVar;
                        hr = InitPropVariantFromString(AppId, &appIdPropVar);
                        if (SUCCEEDED(hr))
                        {
                            hr = propertyStore->SetValue(PKEY_AppUserModel_ID, appIdPropVar);
                            if (SUCCEEDED(hr))
                            {
                                hr = propertyStore->Commit();
                                if (SUCCEEDED(hr))
                                {
                                    ComPtr<IPersistFile> persistFile;
                                    hr = shellLink.As(&persistFile);
                                    if (SUCCEEDED(hr))
                                    {
                                        hr = persistFile->Save(shortcutPath, TRUE);
                                    }
                                }
                            }
                            PropVariantClear(&appIdPropVar);
                        }
                    }
                }
            }
        }
    }
    return hr;
}
```



## <a name="remarks"></a><span data-ttu-id="7cffb-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="7cffb-124">Remarks</span></span>

<span data-ttu-id="7cffb-125">In alternativa all'approccio illustrato in questo argomento, è possibile usare un Framework come il Windows Installer XML (WiX) per generare il collegamento e distribuirlo come parte del Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7cffb-125">As an alternative to the approach shown in this topic, you can use a framework such as the Windows Installer XML (WiX) to generate the shortcut and deploy it as part of the Windows Installer.</span></span> <span data-ttu-id="7cffb-126">In tal caso, il codice deve essere incluso nel file MSI invece che nel codice dell'app.</span><span class="sxs-lookup"><span data-stu-id="7cffb-126">In that case, this code should be included in the MSI rather than in the app's code.</span></span> <span data-ttu-id="7cffb-127">Per altre informazioni, vedere il file di configurazione di WiX di esempio incluso nell'esempio [invio di notifiche di tipo avviso popup da app desktop](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) .</span><span class="sxs-lookup"><span data-stu-id="7cffb-127">For more information, see the sample WiX configuration file included with the [Sending toast notifications from desktop apps](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cffb-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7cffb-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cffb-129">Guida introduttiva: invio di una notifica di tipo avviso popup dal desktop</span><span class="sxs-lookup"><span data-stu-id="7cffb-129">Quickstart: Sending a toast notification from the desktop</span></span>](quickstart-sending-desktop-toast.md)
</dt> <dt>

<span data-ttu-id="7cffb-130">[Esempio di invio notifiche di tipo avviso popup da app desktop](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="7cffb-130">[Sending toast notifications from desktop apps sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))</span></span>
</dt> <dt>

[<span data-ttu-id="7cffb-131">ID modello utente applicazione (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="7cffb-131">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> <dt>

<span data-ttu-id="7cffb-132">[Procedura: installare gli strumenti di Windows Installer XML (WiX)](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7cffb-132">[How to: Install the Windows Installer XML (WiX) Tools](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="7cffb-133">XML Schema popup</span><span class="sxs-lookup"><span data-stu-id="7cffb-133">Toast XML schema</span></span>](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

<span data-ttu-id="7cffb-134">[Panoramica delle notifiche di tipo avviso popup](/previous-versions/windows/apps/hh779727(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7cffb-134">[Toast notification overview](/previous-versions/windows/apps/hh779727(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7cffb-135">[Guida introduttiva: invio di una notifica di tipo avviso popup](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7cffb-135">[Quickstart: Sending a toast notification](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7cffb-136">[Guida introduttiva: invio di notifiche push di tipo avviso popup](/previous-versions/windows/hh761487(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7cffb-136">[Quickstart: Sending a toast push notification](/previous-versions/windows/hh761487(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="7cffb-137">Linee guida ed elenco di controllo per notifiche di tipo avviso popup</span><span class="sxs-lookup"><span data-stu-id="7cffb-137">Guidelines and checklist for toast notifications</span></span>](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[<span data-ttu-id="7cffb-138">Come aggiungere immagini a un modello di avviso popup</span><span class="sxs-lookup"><span data-stu-id="7cffb-138">How to add images to a toast template</span></span>](/previous-versions/windows/)
</dt> <dt>

[<span data-ttu-id="7cffb-139">Come verificare le impostazioni di notifica di tipo avviso popup</span><span class="sxs-lookup"><span data-stu-id="7cffb-139">How to check toast notification settings</span></span>](/previous-versions/windows/)
</dt> <dt>

<span data-ttu-id="7cffb-140">[Come scegliere e usare un modello di avviso popup](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7cffb-140">[How to choose and use a toast template](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7cffb-141">[Come gestire l'attivazione da una notifica di tipo avviso popup](/previous-versions/windows/apps/hh761468(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7cffb-141">[How to handle activation from a toast notification](/previous-versions/windows/apps/hh761468(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7cffb-142">[Come acconsentire esplicitamente per le notifiche di tipo avviso popup](/previous-versions/windows/apps/hh781238(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7cffb-142">[How to opt in for toast notifications](/previous-versions/windows/apps/hh781238(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7cffb-143">[Scelta di un modello di avviso popup](/previous-versions/windows/apps/hh761494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7cffb-143">[Choosing a toast template](/previous-versions/windows/apps/hh761494(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7cffb-144">[Opzioni audio popup](/previous-versions/windows/apps/hh761492(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7cffb-144">[Toast audio options](/previous-versions/windows/apps/hh761492(v=win.10))</span></span>
</dt> </dl>

 

 
