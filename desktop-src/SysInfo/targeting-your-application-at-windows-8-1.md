---
description: In Windows 8.1 e Windows 10 le funzioni GetVersion e GetVersionEx sono state deprecate.
ms.assetid: E7A1A16A-95B3-4B45-81AD-A19E33F15AE4
title: Destinazione dell'applicazione per Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0bd280451e5a1dd6a5162dd7b9ccb34495d22be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348456"
---
# <a name="targeting-your-application-for-windows"></a><span data-ttu-id="eb4bf-103">Destinazione dell'applicazione per Windows</span><span class="sxs-lookup"><span data-stu-id="eb4bf-103">Targeting your application for Windows</span></span>

<span data-ttu-id="eb4bf-104">In Windows 8.1 e Windows 10 le funzioni [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) e [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) sono state deprecate.</span><span class="sxs-lookup"><span data-stu-id="eb4bf-104">In Windows 8.1 and Windows 10, the [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) and [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) functions have been deprecated.</span></span> <span data-ttu-id="eb4bf-105">In Windows 10, anche la funzione [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="eb4bf-105">In Windows 10, the [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) function has also been deprecated.</span></span> <span data-ttu-id="eb4bf-106">Sebbene sia comunque possibile chiamare le funzioni deprecate, se l'applicazione non specifica come destinazione Windows 8.1 o Windows 10, le funzioni restituiranno la versione di Windows 8 (6,2).</span><span class="sxs-lookup"><span data-stu-id="eb4bf-106">While you can still call the deprecated functions, if your application does not specifically target Windows 8.1 or Windows 10, the functions will return the Windows 8 version (6.2).</span></span>

> [!Note]  
> <span data-ttu-id="eb4bf-107">[**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion), [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa), [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)e le [funzioni helper Version](version-helper-apis.md) sono solo per le applicazioni desktop.</span><span class="sxs-lookup"><span data-stu-id="eb4bf-107">[**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion), [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa), [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa), and the [Version Helper functions](version-helper-apis.md) are for desktop apps only.</span></span> <span data-ttu-id="eb4bf-108">Le app di Windows universale possono usare la proprietà [**AnalyticsInfo. VERSIONINFO**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) per i log di diagnostica e di telemetria.</span><span class="sxs-lookup"><span data-stu-id="eb4bf-108">Universal Windows apps can use the [**AnalyticsInfo.VersionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) property for telemetry and diagnostic logs.</span></span>

<span data-ttu-id="eb4bf-109">Per fare in modo che l'app abbia come destinazione Windows 8.1 o Windows 10, è necessario includere un [manifesto dell'app (eseguibile)](/windows/compatibility/application-executable-manifest) per l'eseguibile dell'app.</span><span class="sxs-lookup"><span data-stu-id="eb4bf-109">In order for your app to target Windows 8.1 or Windows 10, you'll need to include an [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="eb4bf-110">Quindi, nella sezione [ **&lt; compatibilità &gt;**](../SbsCs/application-manifests.md#compatibility) del manifesto è necessario aggiungere un elemento **&lt; &gt; supportos** per ogni versione di Windows che si vuole dichiarare supportata dall'app.</span><span class="sxs-lookup"><span data-stu-id="eb4bf-110">Then, in the [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest, you'll need to add a **&lt;supportedOS&gt;** element for each Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="eb4bf-111">Nell'esempio seguente viene illustrato un file manifesto dell'applicazione per un'applicazione che supporta tutte le versioni di Windows da Windows Vista a Windows 10:</span><span class="sxs-lookup"><span data-stu-id="eb4bf-111">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 10:</span></span>

```XML
<!-- example.exe.manifest -->
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
    <assemblyIdentity
        type="win32"
        name="Contoso.ExampleApplication.ExampleBinary"
        version="1.2.3.4"
        processorArchitecture="x86"
    />
    <description>Contoso Example Application</description>
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!-- Windows 10 -->
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/>
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
        <security>
            <requestedPrivileges>
                <!--
                  UAC settings:
                  - app should run at same integrity level as calling process
                  - app does not need to manipulate windows belonging to
                    higher-integrity-level processes
                  -->
                <requestedExecutionLevel
                    level="asInvoker"
                    uiAccess="false"
                />   
            </requestedPrivileges>
        </security>
    </trustInfo>
</assembly>
```

<span data-ttu-id="eb4bf-112">La dichiarazione del supporto per Windows 8.1 o Windows 10 nel manifesto dell'app non avrà alcun effetto quando si esegue l'app nei sistemi operativi precedenti.</span><span class="sxs-lookup"><span data-stu-id="eb4bf-112">Declaring support for Windows 8.1 or Windows 10 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

<span data-ttu-id="eb4bf-113">Il manifesto dell'applicazione precedente include anche una [sezione **&lt; trustInfo &gt;**](/previous-versions/bb756929(v=msdn.10)), che specifica il modo in cui il sistema deve considerarlo rispetto al [controllo dell'account utente (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works).</span><span class="sxs-lookup"><span data-stu-id="eb4bf-113">The above app manifest also includes a [**&lt;trustInfo&gt;** section](/previous-versions/bb756929(v=msdn.10)), which specifies how the system should treat it with respect to [User Account Control (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works).</span></span> <span data-ttu-id="eb4bf-114">L'aggiunta di **trustInfo** non è essenziale, ma è consigliabile anche quando l'app non necessita di alcun comportamento correlato a UAC specifico.</span><span class="sxs-lookup"><span data-stu-id="eb4bf-114">Adding **trustInfo** isn't essential, but it is highly recommended, even when your app doesn't need any particular UAC-related behavior.</span></span> <span data-ttu-id="eb4bf-115">In particolare, se non si aggiunge **trustInfo** , le versioni x86 a 32 bit dell'app saranno soggette alla [virtualizzazione dei file UAC](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), che consente alle scritture delle cartelle con privilegi di amministratore, ad esempio le cartelle di sistema di Windows, di avere esito positivo in caso contrario, ma le reindirizza a una cartella "VirtualStore" specifica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="eb4bf-115">In particular, if you don't add **trustInfo** at all, then 32-bit x86 versions of your app will be subject to [UAC file virtualization](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), which allows writes to administrator-privileged folders like the Windows system folders to succeed when they would otherwise fail, but redirects them to a user-specific "VirtualStore" folder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb4bf-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb4bf-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb4bf-117">Recupero della versione del sistema</span><span class="sxs-lookup"><span data-stu-id="eb4bf-117">Getting the system version</span></span>](getting-the-system-version.md)
</dt> <dt>

[<span data-ttu-id="eb4bf-118">Funzioni helper versione</span><span class="sxs-lookup"><span data-stu-id="eb4bf-118">Version Helper functions</span></span>](version-helper-apis.md)
</dt> <dt>

[<span data-ttu-id="eb4bf-119">OSVERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="eb4bf-119">OSVERSIONINFO</span></span>](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[<span data-ttu-id="eb4bf-120">OSVERSIONINFOEX</span><span class="sxs-lookup"><span data-stu-id="eb4bf-120">OSVERSIONINFOEX</span></span>](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
