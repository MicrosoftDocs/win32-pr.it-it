---
description: Roadmap per l'uso di WMI per ottenere dati per script client e applicazioni o per fornire dati a WMI da un'applicazione.
ms.assetid: d9a3741c-313f-4b63-8588-696a10d370f5
ms.tgt_platform: multiple
title: Uso di WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d1556d321441c7e6a3191bf95e85db356e7ba9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475317"
---
# <a name="using-wmi"></a>Uso di WMI

È possibile usare WMI da applicazioni client e script. Fornisce un'infrastruttura che semplifica l'individuazione e l'esecuzione di attività di gestione. È anche possibile aggiungere al set di possibili attività di gestione creando provider WMI personalizzati.

> [!Note]  
> La versione di nuova generazione di WMI per la scrittura di applicazioni e script è disponibile tramite Windows Management Infrastructure (MI). Per altre informazioni, vedere [Provider e client MI](/previous-versions/windows/desktop/wmi_v2/mi-providers-and-clients-node-page).

 

In questa sezione vengono trattati gli argomenti seguenti:

-   [Recupero di dati da WMI](#obtaining-data-from-wmi)
-   [Fornire dati a WMI](#providing-data-to-wmi)
-   [Attività importanti per WMI](#important-tasks-for-wmi)

## <a name="obtaining-data-from-wmi"></a>Recupero di dati da WMI

La procedura seguente descrive come ottenere dati da WMI scrivendo uno script o un'applicazione.

**Per ottenere dati da WMI scrivendo uno script o un'applicazione**

1.  Decidere quale lingua usare. Per altre informazioni sullo scripting, vedere [Creazione di uno script WMI.](creating-a-wmi-script.md) Per altre informazioni su C++, vedere [Creazione di un'applicazione WMI tramite C++.](creating-a-wmi-application-using-c-.md) Per altre informazioni su C# o WMI .NET, vedere [Panoramica di WMI .NET.](/previous-versions/)

    È possibile visualizzare o modificare i dati WMI in molti linguaggi. Nella tabella seguente sono elencati gli argomenti che descrivono come usare i linguaggi di scripting e delle applicazioni per ottenere i dati.

    

    
| Lingua dell'applicazione | Argomento | 
|----------------------|-------|
| Script scritti in Microsoft ActiveX hosting di script, tra cui Visual Basic Scripting Edition (VBScript) e Perl<br /> | <a href="scripting-api-for-wmi.md">API di scripting per WMI</a>.<br /> Iniziare con <a href="creating-a-wmi-script.md">Creazione di uno script WMI</a>.<br /> Per esempi di codice di script, vedere <a href="wmi-tasks-for-scripts-and-applications.md">Attività WMI per script e applicazioni e</a> il repository di script di TechNet <a href="https://www.microsoft.com/technet/scriptcenter">ScriptCenter.</a><br /> | 
| Windows PowerShell<br /> | <a href="/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7">Attività iniziali con Windows PowerShell</a><br /> Cmdlet di PowerShell WMI, ad esempio <a href="/previous-versions//dd315295(v=technet.10)">Get-WmiObject</a>.<br /> | 
| Visual Basic applicazioni<br /> | <a href="scripting-api-for-wmi.md">API di scripting per WMI</a>.<br /> | 
| Active Server Pages<br /> | <a href="scripting-api-for-wmi.md">API di scripting per WMI</a>.<br /> Iniziare con <a href="creating-active-server-pages-for-wmi.md">Creazione di Active Server pagine per WMI.</a><br /> | 
| applicazioni C++<br /> | <a href="com-api-for-wmi.md">API COM per WMI</a>.<br /> Iniziare con <a href="creating-a-wmi-application-using-c-.md">Creazione di un'applicazione WMI con esempi di applicazioni C++</a> e WMI <a href="wmi-c---application-examples.md">C++</a> (contiene esempi).<br /> | 
| .NET Framework applicazioni scritte in C#, Visual Basic .NET o J #<br /> | Classi nello spazio <a href="/previous-versions//hh872326(v=vs.85)"><strong>dei nomi Microsoft.Management.Infrastructure.</strong></a><br /><blockquote>    [!Note]<br /><strong>System.Management è</strong> lo spazio dei nomi originale che ha trattato il codice gestito per WMI. Tuttavia, la tecnologia sottostante per <strong>System.Management</strong> è in genere più lenta e non viene ridimensionata come <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft.Management.Infrastructure</strong></a>. Di conseguenza, non è consigliabile usare <strong>System.Management</strong> per i nuovi progetti. Per altre informazioni su <strong>System.Management,</strong>vedere <a href="/previous-versions/bb404655(v=vs.90)">Panoramica di WMI .NET.</a>    </blockquote><br /> | 


    

     

2.  Assicurarsi che le connessioni ai computer remoti funzionino.

    Per altre informazioni, vedere [Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

3.  La connessione a WMI nei computer remoti richiede le impostazioni di sicurezza corrette, come illustrato in [Gestione della sicurezza WMI](maintaining-wmi-security.md). Nella tabella seguente sono elencati gli argomenti che descrivono come configurare le impostazioni di sicurezza con i linguaggi di scripting e delle applicazioni.

    

    | Linguaggio                                                      | Argomento                                                                                                                                                                                                                                                 |
    |---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Script in qualsiasi linguaggio, Visual Basic applicazioni<br/> | [Impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md)<br/>                                                                                                                 |
    | Active Server Pages<br/>                                | [Configurazione di IIS 5 e versioni successive per lo scripting ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md)<br/>                                                                                                                                           |
    | C++<br/>                                                | Impostazione del livello di sicurezza del processo [predefinito con C++](setting-the-default-process-security-level-using-c-.md) e impostazione della sicurezza in [IWbemServices e altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md)<br/> |

    

     

4.  Dopo la connessione a WMI, è possibile ottenere dati tramite query ed enumerazioni.

    Per altre informazioni, vedere [Modifica delle informazioni su classi e istanze](manipulating-class-and-instance-information.md) ed Esecuzione di query con [WQL.](querying-with-wql.md)

5.  I dati del Registro di sistema sono disponibili tramite WMI ed è possibile creare nuove chiavi e valori o modificare quelli esistenti.

    Per altre informazioni, vedere [Modifica del Registro di sistema](modifying-the-system-registry.md).

6.  È possibile sottoscrivere le notifiche degli eventi tramite WMI, temporaneamente tra un riavvio del sistema e l'altro in modo permanente.

    Per altre informazioni, vedere [Monitoraggio degli eventi](monitoring-events.md) e Ricezione di un evento [WMI](receiving-a-wmi-event.md).

7.  I dati dei contatori delle prestazioni per un sistema sono disponibili tramite WMI.

    I contatori della libreria delle prestazioni di sistema vengono convertiti in classi WMI. Per altre informazioni, vedere [Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md).

8.  [Attività WMI per script e applicazioni](wmi-tasks-for-scripts-and-applications.md) descrive come eseguire molte attività amministrative con WMI.

## <a name="providing-data-to-wmi"></a>Fornire dati a WMI

La procedura seguente descrive come fornire dati a WMI scrivendo un provider.

**Per fornire dati a WMI scrivendo un provider**

-   Decidere il tipo di provider da scrivere.

    Non è possibile scrivere un provider WMI in VBScript. È tuttavia possibile adottare diversi altri approcci per scrivere un provider COM WMI:

    -   Uso della procedura guidata ATL WMI in Visual Studio.

        Questo approccio crea un provider COM non gestito. Per altre informazioni, vedere [Aggiunta di un provider di istanze WMI](./writing-an-instance-provider.md) e Aggiunta di un provider di eventi [WMI](./writing-an-event-provider.md).

    -   Uso di COM direttamente in qualsiasi ambiente di sviluppo integrato.

        Questo approccio crea un provider COM non gestito.

    -   Uso di WMI nel .NET Framework per creare un provider di codice gestito.

        Questo approccio crea un provider di codice gestito. I provider di codice gestito possono essere scritti in qualsiasi linguaggio .NET Framework, sono più semplici da scrivere rispetto ai provider COM WMI e possono ottenere dati dalle classi WMI basate su [*CIM,*](gloss-c.md)ad esempio le classi [Win32](/windows/desktop/CIMWin32Prov/win32-provider). Tuttavia, il .NET Framework WMI ha alcune limitazioni. Per altre informazioni, vedere [Gestione di applicazioni tramite WMI.](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))

    -   Non è [consigliabile usare le classi del framework](wmi-c-classes.md) del provider.

        Il framework del provider è stato sostituito dalle procedure guidate ATL WMI, usando direttamente COM o .NET Framework provider. Non è più consigliabile creare un provider COM WMI con le classi del framework del provider. Nella tabella seguente sono elencati gli argomenti che descrivono come usare i provider com o .NET Framework client.

    

    | Provider                                                      | Argomento                                                                                                   |
    |---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
    | Provider COM nello stesso processo di WMI<br/>            | [Fornire dati a WMI](providing-data-to-wmi.md)<br/>                                           |
    | Provider com disaccoccolato<br/>                             | [Incorporamento di un provider in un'applicazione](incorporating-a-provider-in-an-application.md)<br/> |
    | .NET Framework provider in C# o Visual Basic.NET<br/> | [Gestione di applicazioni tramite WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))<br/>            |

    

     

## <a name="important-tasks-for-wmi"></a>Attività importanti per WMI

Negli argomenti seguenti vengono fornite informazioni sull'uso di WMI per monitorare e controllare i componenti aziendali.



| Argomento                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Attività WMI per script e applicazioni](wmi-tasks-for-scripts-and-applications.md)<br/>                                                 | Descrive come trovare la classe WMI corretta e le procedure da usare negli script e nelle applicazioni che eseguono attività comuni di amministrazione di computer e di rete, ad esempio l'aggiunta di una nuova connessione stampante per un computer remoto o la ricerca di tutti gli hotfix installati in un computer.<br/>                                                                            |
| [Creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md)<br/>                                                     | Qualsiasi linguaggio di scripting, ad esempio VBScript o Perl, che funziona con ActiveX possono accedere ai dati WMI. Le applicazioni possono accedere a WMI in C++, usando [l'API COM](com-api-for-wmi.md) per WMI o in Visual Basic, usando la libreria dei tipi Wbemdisp.tlb e l'API scripting per [WMI.](scripting-api-for-wmi.md)[](using-the-wmi-scripting-type-library.md)<br/> |
| [Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)<br/>                                                 | Descrive in che modo script, applicazioni e provider possono stabilire connessioni a WMI nei computer remoti per ottenere dati o controllare hardware e software.<br/>                                                                                                                                                                                                   |
| [Connessione a WMI in un computer remoto tramite Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)<br/> | Viene descritto come usare Windows PowerShell per stabilire connessioni a WMI nei computer remoti per ottenere dati o per controllare hardware e software.<br/>                                                                                                                                                                                                            |
| [Monitoraggio degli eventi](monitoring-events.md)<br/>                                                                                           | Viene descritto come ottenere notifiche degli eventi creando consumer di eventi WMI temporanei o permanenti.<br/>                                                                                                                                                                                                                                                           |
| [Fornire dati a WMI](providing-data-to-wmi.md)<br/>                                                                                   | WMI fornisce dati a gestione dinamica alle applicazioni e agli script client ottenendoli dai provider.<br/>                                                                                                                                                                                                                                                    |
| [Recupero e fornitura di dati in un computer a 64 bit](getting-and-providing-data-on-a-64-bit-computer.md)<br/>                               | Descrive come accedere a provider non predefiniti e considerazioni per i writer di provider nei sistemi a 64 bit.<br/>                                                                                                                                                                                                                                                    |



