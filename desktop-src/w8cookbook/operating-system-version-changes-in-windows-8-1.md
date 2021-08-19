---
title: Modifiche alla versione del sistema operativo in Windows 8.1 e Windows Server 2012 R2
description: Modifiche alla versione del sistema operativo in Windows 8.1 e Windows Server 2012 R2
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e1fe0972a915d0f13ca3c3f8f52e5dd0559ad9c24e1afd2dd005f4a733373c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882691"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a>Modifiche alla versione del sistema operativo in Windows 8.1 e Windows Server 2012 R2

## <a name="platforms"></a>Piattaforme

**Client -** Windows 8.1

**Server -** Windows Server 2012 R2

## <a name="description"></a>Descrizione

Sono state apportate alcune modifiche significative al funzionamento delle API GetVersion(Ex) in Windows 8.1 a causa di comportamenti indesiderati dei clienti derivanti dal modo in cui le API GetVersion(Ex) sono state usate in passato.

Nelle versioni precedenti di Windows, la chiamata delle API GetVersion(Ex) restituiva la versione effettiva del sistema operativo, a meno che il processo non fosse stato mitigato da uno shim di compatibilità dell'app per assegnargli una versione diversa. Questa operazione è stata eseguita in modo provvisorio ed è relativamente incompleta in termini di numero di processi che Microsoft potrebbe ragionevolmente shim in una versione. Molte applicazioni sono state in grado di risolvere i problemi perché non sono state s shimmed a causa di controlli della versione non progettati in modo non corretta.

Il motivo principale per eseguire un controllo della versione è avvisare l'utente che l'applicazione deve essere eseguita in una versione più recente del sistema operativo. Tuttavia, a causa di controlli non corretti, le app spesso avvisano erroneamente che devono essere eseguite in Windows XP o versioni successive, come ovviamente il sistema operativo più recente. Più spesso, il sistema operativo più recente eseguirebbe l'applicazione senza problemi se non fosse per questi controlli.

## <a name="manifestation"></a>Manifestazione

In Windows 8.1, le API GetVersion(Ex) sono state deprecate. Ciò significa che anche se è comunque possibile chiamare queste funzioni API, se l'app non ha come destinazione Windows 8.1, le funzioni restituiranno la versione Windows 8 (6.2).

## <a name="solution"></a>Soluzione

### <a name="adding-an-app-manifest"></a>Aggiunta di un manifesto dell'app

Per fare in modo che l'app Windows 8.1 destinazione, è necessario includere un manifesto [dell'app (eseguibile)](/windows/compatibility/application-executable-manifest) per l'eseguibile dell'app. Quindi, nella sezione [ **&lt; relativa alla &gt;**](../SbsCs/application-manifests.md#compatibility) compatibilità del manifesto, è necessario aggiungere un elemento **&lt; supportedOS &gt;** per ogni versione Windows che si vuole dichiarare che l'app supporta.

L'esempio seguente mostra un file manifesto dell'app per un'app che supporta tutte le versioni di Windows da Windows Vista a Windows 8.1:

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

La riga precedente contrassegnata `* ADD THIS LINE *` mostra come definire in modo accurato come destinazione l'applicazione per Windows 8.1.

La dichiarazione del supporto Windows 8.1 nel manifesto dell'app non avrà alcun effetto quando si esegue l'app nei sistemi operativi precedenti.

### <a name="using-versionhelpers-instead-of-getversionex"></a>Uso di VersionHelpers invece di GetVersion(Ex)

Windows 8.1 introduce nuove funzioni API sostitutive per GetVersion(Ex), note come VersionHelpers. Sono estremamente facili da usare. È necessario solo `#include <VersionHelpers.h>` . Le funzioni inline disponibili nel file di intestazione VersionHelpers.h consentono al codice di chiedere se il sistema operativo è una determinata versione di Windows o versioni successive.

**Esempio** Ad esempio, se l'applicazione richiede Windows 8 versione successiva, usare il test seguente:

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

Le funzioni disponibili dell'API VersionHelper sono:

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

Restituiranno TRUE o FALSE a seconda della domanda che si sta ponendo ed è necessario definire solo il sistema operativo di livello minimo che si supporta.

## <a name="resources"></a>Risorse

-   [Application Compatibility Toolkit Download](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   [Correzioni di compatibilità note, modalità di compatibilità e messaggi AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [API VersionHelpers](../sysinfo/version-helper-apis.md)