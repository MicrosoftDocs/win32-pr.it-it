---
description: Guida di orientamento all'utilizzo di WMI per ottenere i dati per le applicazioni e gli script client o per fornire dati a WMI da un'applicazione.
ms.assetid: d9a3741c-313f-4b63-8588-696a10d370f5
ms.tgt_platform: multiple
title: Utilizzo di WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31878b41de0f44a70c31c2134f0a611a9309a321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131971"
---
# <a name="using-wmi"></a>Utilizzo di WMI

È possibile utilizzare WMI da applicazioni e script client. Fornisce un'infrastruttura che semplifica l'individuazione e l'esecuzione di attività di gestione. Inoltre, è possibile aggiungere al set di possibili attività di gestione creando provider WMI personalizzati.

> [!Note]  
> La versione di nuova generazione di WMI per la scrittura di applicazioni e script è disponibile tramite Windows Management Infrastructure (MI). Per altre informazioni, vedere [i provider e i client mi](/previous-versions/windows/desktop/wmi_v2/mi-providers-and-clients-node-page).

 

In questa sezione vengono trattati gli argomenti seguenti:

-   [Recupero di dati da WMI](#obtaining-data-from-wmi)
-   [Invio di dati a WMI](#providing-data-to-wmi)
-   [Attività importanti per WMI](#important-tasks-for-wmi)

## <a name="obtaining-data-from-wmi"></a>Recupero di dati da WMI

Nella procedura seguente viene descritto come ottenere dati da WMI scrivendo uno script o un'applicazione.

**Per ottenere dati da WMI scrivendo uno script o un'applicazione**

1.  Decidere quale lingua usare. Per ulteriori informazioni sullo scripting, vedere [creazione di uno script WMI](creating-a-wmi-script.md). Per ulteriori informazioni su C++, vedere [creazione di un'applicazione WMI con c++](creating-a-wmi-application-using-c-.md). Per ulteriori informazioni su C# o WMI .NET, vedere [Panoramica di WMI .NET](/previous-versions/).

    È possibile visualizzare o modificare i dati WMI in molte lingue. Nella tabella seguente sono elencati gli argomenti in cui viene descritto come utilizzare lo scripting e i linguaggi delle applicazioni per ottenere i dati.

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Lingua dell'applicazione</th>
    <th>Argomento</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Script scritti nell'hosting di script Microsoft ActiveX, tra cui Visual Basic Scripting Edition (VBScript) e Perl<br/></td>
    <td><a href="scripting-api-for-wmi.md">API di scripting per WMI</a>.<br/> Iniziare con <a href="creating-a-wmi-script.md">la creazione di uno script WMI</a>.<br/> Per esempi di codice di script, vedere <a href="wmi-tasks-for-scripts-and-applications.md">attività WMI per gli script e le applicazioni</a> e il repository di script TechNet <a href="https://www.microsoft.com/technet/scriptcenter">ScriptCenter</a> .<br/></td>
    </tr>
    <tr class="even">
    <td>Windows PowerShell<br/></td>
    <td><a href="/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7">Introduzione con Windows PowerShell</a><br/> Cmdlet di PowerShell per WMI, ad esempio <a href="/previous-versions//dd315295(v=technet.10)">Get-WmiObject</a>.<br/></td>
    </tr>
    <tr class="odd">
    <td>Applicazioni Visual Basic<br/></td>
    <td><a href="scripting-api-for-wmi.md">API di scripting per WMI</a>.<br/></td>
    </tr>
    <tr class="even">
    <td>Active Server Pages<br/></td>
    <td><a href="scripting-api-for-wmi.md">API di scripting per WMI</a>.<br/> Iniziare con la <a href="creating-active-server-pages-for-wmi.md">creazione di Active Server pagine per WMI</a>.<br/></td>
    </tr>
    <tr class="odd">
    <td>applicazioni C++<br/></td>
    <td><a href="com-api-for-wmi.md">API com per WMI</a>.<br/> Iniziare con <a href="creating-a-wmi-application-using-c-.md">la creazione di un'applicazione WMI utilizzando</a> gli esempi di applicazioni C++ e <a href="wmi-c---application-examples.md">WMI c++</a> (contiene esempi).<br/></td>
    </tr>
    <tr class="even">
    <td>.NET Framework applicazioni scritte in C#, Visual Basic .NET o J #<br/></td>
    <td>Classi nello spazio dei nomi <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft. Management. Infrastructure</strong></a> .<br/>
    <blockquote>
    [!Note]<br />
    <strong>System. Management</strong> era lo spazio dei nomi originale che analizzava il codice gestito per WMI. Tuttavia, la tecnologia sottostante per <strong>System. Management</strong> è in genere più lenta di e non viene ridimensionata, oltre a <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft. Management. Infrastructure</strong></a>. Di conseguenza, non è consigliabile usare <strong>System. Management</strong> per i nuovi progetti. Per ulteriori informazioni su <strong>System. Management</strong>, vedere <a href="/previous-versions/bb404655(v=vs.90)">Panoramica di WMI .NET</a>. </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Verificare che le connessioni ai computer remoti funzionino.

    Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

3.  Per la connessione a WMI in computer remoti sono necessarie le impostazioni di sicurezza corrette, come illustrato in [gestione della sicurezza di WMI](maintaining-wmi-security.md). Nella tabella seguente sono elencati gli argomenti che descrivono come configurare le impostazioni di sicurezza con gli script e i linguaggi delle applicazioni.

    

    | Linguaggio                                                      | Argomento                                                                                                                                                                                                                                                 |
    |---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Script in qualsiasi linguaggio, applicazioni Visual Basic<br/> | [Impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md)<br/>                                                                                                                 |
    | Active Server Pages<br/>                                | [Configurazione di IIS 5 e versioni successive per lo scripting ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md)<br/>                                                                                                                                           |
    | C++<br/>                                                | [Impostazione del livello di sicurezza del processo predefinito mediante C++](setting-the-default-process-security-level-using-c-.md) e [impostazione della sicurezza in IWbemServices e in altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md)<br/> |

    

     

4.  Dopo la connessione a WMI, è possibile ottenere dati tramite query ed enumerazioni.

    Per ulteriori informazioni, vedere [modifica delle informazioni relative a classi e istanze](manipulating-class-and-instance-information.md) ed [esecuzione di query con WQL](querying-with-wql.md).

5.  I dati del registro di sistema sono disponibili tramite WMI ed è possibile creare nuove chiavi e valori o modificare quelli esistenti.

    Per ulteriori informazioni, vedere [modifica del registro di sistema](modifying-the-system-registry.md).

6.  È possibile sottoscrivere le notifiche degli eventi tramite WMI, temporaneamente tra i riavvii del sistema o in modo permanente.

    Per ulteriori informazioni, vedere [monitoraggio di eventi](monitoring-events.md) e [ricezione di un evento WMI](receiving-a-wmi-event.md).

7.  I dati dei contatori delle prestazioni per un sistema sono disponibili tramite WMI.

    I contatori delle prestazioni di sistema vengono convertiti in classi WMI. Per ulteriori informazioni, vedere [monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md).

8.  [Nelle attività WMI per script e applicazioni](wmi-tasks-for-scripts-and-applications.md) viene descritto come eseguire numerose attività amministrative con WMI.

## <a name="providing-data-to-wmi"></a>Invio di dati a WMI

Nella procedura riportata di seguito viene descritto come fornire dati a WMI scrivendo un provider.

**Per fornire i dati a WMI scrivendo un provider**

-   Decidere il tipo di provider da scrivere.

    Non è possibile scrivere un provider WMI in VBScript. Tuttavia, è possibile adottare diversi altri approcci alla scrittura di un provider COM WMI:

    -   Utilizzo della procedura guidata WMI ATL in Visual Studio.

        Questo approccio crea un provider COM non gestito. Per ulteriori informazioni, vedere [aggiunta di un provider di istanze WMI](./writing-an-instance-provider.md) e [aggiunta di un provider di eventi WMI](./writing-an-event-provider.md).

    -   Utilizzo di COM direttamente in qualsiasi Integrated Development Environment.

        Questo approccio crea un provider COM non gestito.

    -   Utilizzare WMI nel .NET Framework per creare un provider di codice gestito.

        Questo approccio consente di creare un provider di codice gestito. I provider di codice gestito possono essere scritti in qualsiasi linguaggio di .NET Framework, sono più semplici da scrivere rispetto ai provider COM WMI e possono ottenere dati dalle classi basate su [*CIM*](gloss-c.md)WMI, ad esempio [le classi Win32](/windows/desktop/CIMWin32Prov/win32-provider). Tuttavia, il provider WMI .NET Framework presenta alcune limitazioni. Per ulteriori informazioni, vedere [gestione di applicazioni tramite WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

    -   Non è consigliabile usare le [classi del Framework del provider](wmi-c-classes.md) .

        Il Framework del provider è stato sostituito dalle procedure guidate di WMI ATL, usando direttamente i provider COM o .NET Framework. La creazione di un provider COM WMI con le classi del Framework del provider non è più consigliata. Nella tabella seguente sono elencati gli argomenti che descrivono come utilizzare i provider COM o .NET Framework.

    

    | Provider                                                      | Argomento                                                                                                   |
    |---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
    | Provider COM nello stesso processo di WMI<br/>            | [Invio di dati a WMI](providing-data-to-wmi.md)<br/>                                           |
    | Provider COM disaccoppiato<br/>                             | [Incorporamento di un provider in un'applicazione](incorporating-a-provider-in-an-application.md)<br/> |
    | Provider .NET Framework in C# o Visual Basic.NET<br/> | [Gestione di applicazioni tramite WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))<br/>            |

    

     

## <a name="important-tasks-for-wmi"></a>Attività importanti per WMI

Negli argomenti seguenti vengono fornite informazioni sull'utilizzo di WMI per monitorare e controllare i componenti aziendali.



| Argomento                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Attività WMI per script e applicazioni](wmi-tasks-for-scripts-and-applications.md)<br/>                                                 | Viene descritto come trovare la classe e le procedure WMI corrette da utilizzare negli script e nelle applicazioni che eseguono attività comuni di amministrazione di computer e reti, ad esempio l'aggiunta di una nuova connessione alla stampante per un computer remoto o la ricerca di tutti gli hotfix installati in un computer.<br/>                                                                            |
| [Creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md)<br/>                                                     | Qualsiasi linguaggio di scripting, ad esempio VBScript o Perl, che funziona con gli oggetti ActiveX, può accedere ai dati WMI. Le applicazioni possono accedere a WMI in C++, usando l' [API com per WMI](com-api-for-wmi.md) o in Visual Basic, usando la[libreria dei tipi](using-the-wmi-scripting-type-library.md) wbemdisp. tlb e l' [API di scripting per WMI](scripting-api-for-wmi.md).<br/> |
| [Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)<br/>                                                 | Viene descritto in che modo gli script, le applicazioni e i provider possono stabilire connessioni a WMI in computer remoti per ottenere dati o controllare hardware e software.<br/>                                                                                                                                                                                                   |
| [Connessione a WMI in un computer remoto tramite Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)<br/> | Viene descritto come utilizzare Windows PowerShell per stabilire connessioni a WMI su computer remoti per ottenere i dati o per controllare l'hardware e il software.<br/>                                                                                                                                                                                                            |
| [Monitoraggio degli eventi](monitoring-events.md)<br/>                                                                                           | Viene descritto come ottenere le notifiche degli eventi tramite la creazione di consumer di eventi WMI temporanei o permanenti.<br/>                                                                                                                                                                                                                                                           |
| [Invio di dati a WMI](providing-data-to-wmi.md)<br/>                                                                                   | WMI fornisce dati di gestione dinamici agli script e alle applicazioni client ottenendoli dai provider.<br/>                                                                                                                                                                                                                                                    |
| [Ottenere e fornire dati in un computer a 64 bit](getting-and-providing-data-on-a-64-bit-computer.md)<br/>                               | Viene descritto come accedere a provider e considerazioni non predefiniti per writer del provider in sistemi a 64 bit.<br/>                                                                                                                                                                                                                                                    |



