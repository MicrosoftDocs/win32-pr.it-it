---
title: Modifiche della versione del sistema operativo in Windows 8.1 e Windows Server 2012 R2
description: Modifiche della versione del sistema operativo in Windows 8.1 e Windows Server 2012 R2
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0078ba918c675bbc8b9b9bbaf76660388f05bda9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399644"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a>Modifiche della versione del sistema operativo in Windows 8.1 e Windows Server 2012 R2

## <a name="platforms"></a>Piattaforme

**Client-** Windows 8.1

**Server-** Windows Server 2012 R2

## <a name="description"></a>Descrizione

Sono state apportate alcune modifiche significative al funzionamento delle API GetVersion (ex) in Windows 8.1 a causa di comportamenti indesiderati dei clienti che derivano dal modo in cui le API GetVersion (ex) sono state usate in passato.

Nelle versioni precedenti di Windows, la chiamata delle API GetVersion (ex) restituisce la versione effettiva del sistema operativo, a meno che il processo non sia stato mitigato da uno shim di compatibilità dell'app per assegnargli una versione diversa. Questa operazione è stata eseguita su base provvisoria ed era relativamente incompleta in termini di numero di processi che Microsoft poteva ragionevolmente shim in una versione. Molte applicazioni attraversano le crepe perché non ricevono sottoposto a shim a causa di verifiche della versione progettate in modo non corretto.

Il numero uno dei motivi per eseguire un controllo della versione consiste nel segnalare all'utente che l'applicazione deve essere eseguita in una versione più recente del sistema operativo. Tuttavia, a causa dei controlli di scarsa qualità, le app spesso avvisano erroneamente che erano necessarie per l'esecuzione in Windows XP o versioni successive, ovviamente il sistema operativo più recente è. Spesso, il sistema operativo più recente eseguirebbe l'applicazione senza problemi se non per questi controlli.

## <a name="manifestation"></a>Manifestazione

In Windows 8.1, le API GetVersion (ex) sono state deprecate. Ciò significa che, sebbene sia comunque possibile chiamare queste funzioni API, se l'app non è destinata in modo specifico Windows 8.1, le funzioni restituiranno la versione di Windows 8 (6,2).

## <a name="solution"></a>Soluzione

### <a name="adding-an-app-manifest"></a>Aggiunta di un manifesto dell'applicazione

Per fare in modo che l'app abbia come destinazione Windows 8.1, è necessario includere un [manifesto dell'app (eseguibile)](/windows/compatibility/application-executable-manifest) per l'eseguibile dell'app. Quindi, nella sezione [ **&lt; compatibilità &gt;**](../SbsCs/application-manifests.md#compatibility) del manifesto è necessario aggiungere un elemento **&lt; &gt; supportos** per ogni versione di Windows che si vuole dichiarare supportata dall'app.

Nell'esempio seguente viene illustrato un file manifesto dell'applicazione per un'applicazione che supporta tutte le versioni di Windows da Windows Vista a Windows 8.1:

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
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
</assembly>
```

La riga sopra contrassegnata `* ADD THIS LINE *` Mostra come indirizzare l'applicazione in modo accurato per Windows 8.1.

La dichiarazione del supporto per Windows 8.1 nel manifesto dell'app non avrà alcun effetto quando si esegue l'app nei sistemi operativi precedenti.

### <a name="using-versionhelpers-instead-of-getversionex"></a>Utilizzo di VersionHelpers anziché GetVersion (es)

Windows 8.1 introduce nuove funzioni API sostitutive per GetVersion (ex), noto come VersionHelpers. Sono estremamente facili da usare. è sufficiente `#include <VersionHelpers.h>` . Le funzioni inline disponibili nel file di intestazione VersionHelpers. h consentono al codice di richiedere se il sistema operativo è una versione specifica di Windows o versioni successive.

**Esempio** Se, ad esempio, l'applicazione richiede Windows 8 o versione successiva, usare il test seguente:

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

Le funzioni API VersionHelper disponibili sono:

```c
#define VERSIONHELPERAPI FORCEINLINE BOOL
VERSIONHELPERAPI IsWindowsXPOrGreater();
VERSIONHELPERAPI IsWindowsXPSP1OrGreater();
VERSIONHELPERAPI IsWindowsXPSP2OrGreater();
VERSIONHELPERAPI IsWindowsXPSP3OrGreater();
VERSIONHELPERAPI IsWindowsVistaOrGreater();
VERSIONHELPERAPI IsWindowsVistaSP1OrGreater();
VERSIONHELPERAPI IsWindowsVistaSP2OrGreater();
VERSIONHELPERAPI IsWindows7OrGreater();
VERSIONHELPERAPI IsWindows7SP1OrGreater();
VERSIONHELPERAPI IsWindows8OrGreater();
VERSIONHELPERAPI IsWindows8Point1OrGreater();
VERSIONHELPERAPI IsWindowsServer();
```

Verranno restituiti TRUE o FALSE a seconda della domanda richiesta ed è sufficiente definire il sistema operativo di livello minimo supportato.

## <a name="resources"></a>Risorse

-   [Download di Application Compatibility Toolkit](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   [Correzioni di compatibilità note, modalità di compatibilità e messaggi AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [API VersionHelpers](../sysinfo/version-helper-apis.md)