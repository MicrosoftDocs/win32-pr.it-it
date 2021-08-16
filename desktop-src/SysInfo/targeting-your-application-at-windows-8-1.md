---
description: In Windows 8.1 e Windows 10, le funzioni GetVersion e GetVersionEx sono state deprecate.
ms.assetid: E7A1A16A-95B3-4B45-81AD-A19E33F15AE4
title: Destinazione dell'applicazione per Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e045dff2f46501c4715e2ffebe484dfeadb3aa9f276d79c7e7c1afdbec6ba7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763112"
---
# <a name="targeting-your-application-for-windows"></a>Destinazione dell'applicazione per Windows

In Windows 8.1 e Windows 10, le [**funzioni GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) e [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) sono state deprecate. In Windows 10, anche la [**funzione VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) è stata deprecata. Anche se è comunque possibile chiamare le funzioni deprecate, se l'applicazione non ha specificamente come destinazione Windows 8.1 o Windows 10, le funzioni restituiranno la versione Windows 8 (6.2).

> [!Note]  
> [**Le funzioni GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion), [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa), [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)e [Version Helper](version-helper-apis.md) sono solo per le app desktop. Le app Windows universali possono usare la [**proprietà AnalyticsInfo.VersionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) per i log di telemetria e di diagnostica.

Per fare in modo che l'app sia Windows 8.1 o Windows 10, è necessario includere un manifesto [dell'app (eseguibile)](/windows/compatibility/application-executable-manifest) per il file eseguibile dell'app. Nella sezione [ **&lt; &gt;** di](../SbsCs/application-manifests.md#compatibility) compatibilità del manifesto sarà quindi necessario aggiungere un elemento **&lt; supportedOS &gt;** per ogni versione Windows che si vuole dichiarare supportata dall'app.

L'esempio seguente mostra un file manifesto dell'app per un'app che supporta tutte le versioni di Windows da Windows Vista a Windows 10:

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

La dichiarazione del supporto per Windows 8.1 o Windows 10 nel manifesto dell'app non avrà alcun effetto quando si esegue l'app nei sistemi operativi precedenti.

Il manifesto dell'app precedente include anche una sezione [ **&lt; trustInfo &gt;**](/previous-versions/bb756929(v=msdn.10)), che specifica in che modo il sistema deve trattarlo rispetto al controllo [dell'account utente .](/windows/security/identity-protection/user-account-control/how-user-account-control-works) **L'aggiunta di trustInfo** non è essenziale, ma è consigliabile, anche quando l'app non richiede un comportamento specifico correlato al controllo dell'account utente. In particolare, se non si aggiunge **trustInfo,** le versioni x86 a 32 bit dell'app saranno soggette alla virtualizzazione dei [file](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization)del controllo dell'account utente, che consente di eseguire operazioni di scrittura in cartelle con privilegi di amministratore come le cartelle di sistema Windows quando altrimenti non riescono, ma le reindirizza a una cartella "VirtualStore" specifica dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Recupero della versione del sistema](getting-the-system-version.md)
</dt> <dt>

[Funzioni dell'helper versione](version-helper-apis.md)
</dt> <dt>

[OSVERSIONINFO](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[OSVERSIONINFOEX](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
