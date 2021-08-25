---
title: Informazioni Windows gestione remota
description: Windows Gestione remota è un componente delle funzionalità Windows gestione hardware che gestiscono l'hardware del server in locale e in remoto.
ms.assetid: f58add53-0746-4423-9ab8-02ba05f82fa7
ms.tgt_platform: multiple
keywords:
- Informazioni Windows gestione remota
- Windows Gestione remota, informazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a83df38de4af354f826b9bbba59ddab76e1b656c72e1c3dc74301da883f875cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858911"
---
# <a name="about-windows-remote-management"></a>Informazioni Windows gestione remota

Windows Gestione remota è un componente delle funzionalità Windows [gestione hardware](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) che gestiscono l'hardware del server in locale e in remoto. Queste funzionalità includono un servizio che implementa il protocollo [*WS-Management,*](windows-remote-management-glossary.md) la diagnosi e il controllo dell'hardware tramite i controller di gestione della baseboard ([*BBMC)*](windows-remote-management-glossary.md)e un'API COM e oggetti [di scripting](winrm-scripting-api.md) che consentono di scrivere applicazioni che comunicano in remoto tramite il protocollo WS-Management. Per altre informazioni sulla specifica pubblica per il protocollo WS-Management, vedere Servizi Web per [la gestione (WS-Management).](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf)

## <a name="components-of-winrm-and-hardware-management"></a>Componenti di Gestione remota Windows e Gestione hardware

Di seguito è riportato un elenco di componenti e funzionalità forniti da WinRM e dal monitoraggio hardware:

-   [WinRM Scripting API](winrm-scripting-api.md)

    Questa API di scripting consente di ottenere dati da computer remoti usando script che eseguono WS-Management operazioni del protocollo.

-   **Winrm.cmd**

    Questo strumento da riga di comando per la gestione del sistema viene implementato in un file Visual Basic Scripting Edition (Winrm.vbs) scritto usando l'API di scripting WinRM. Questo strumento consente a un amministratore di configurare WinRM e di ottenere dati o gestire le risorse. Per altre informazioni, vedere la Guida online fornita dalla riga di comando **Winrm** **/?**.

-   **Winrs.exe**

    Questo strumento della riga di comando consente agli amministratori di eseguire in remoto la maggior parte Cmd.exe comandi usando il WS-Management remoto. Per altre informazioni, vedere la Guida online fornita dalla riga di comando **Winrs** **/?**.

-   Driver IPMI (Intelligent Platform Management Interface) e provider WMI

    La gestione dell'hardware tramite il provider e il driver [*IPMI (Intelligent Platform Management Interface)*](windows-remote-management-glossary.md) consente di controllare e diagnosticare l'hardware del server remoto tramite bMC quando il sistema operativo non è in esecuzione o distribuito.

    Per altre informazioni, vedere Provider [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

-   Servizio WMI

    Il servizio WMI continua a essere eseguito side-by-side con WinRM e fornisce i dati richiesti o il controllo tramite il [*plug-in WMI*](windows-remote-management-glossary.md). È possibile continuare a ottenere dati dalle classi WMI standard, ad esempio il processo [**Win32, \_**](/windows/desktop/CIMWin32Prov/win32-process)nonché dai dati forniti da IPMI. Per altre informazioni sulla configurazione e l'installazione necessarie per WinRM, vedere [Introduzione alla gestione hardware](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)).

-   WS-Management protocollo

    WS-Management, un protocollo basato su SOAP e basato su firewall, è stato progettato per i sistemi per individuare e scambiare informazioni di gestione. Lo scopo della specifica WS-Management protocollo è fornire interoperabilità e coerenza per i sistemi aziendali con computer in esecuzione in un'ampia gamma di sistemi operativi di fornitori diversi.

    WS-Management è basato sulle specifiche del servizio Web standard seguenti: HTTPS, SOAP su HTTP (profilo WS-I), SOAP 1.2, WS-Addressing, WS-Transfer, WS-Enumeration e WS-Eventing. Per altre informazioni sulla bozza corrente della specifica, vedere la [pagina dell'indice delle specifiche di gestione](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

## <a name="working-with-winrm"></a>Uso di WinRM

Per altre informazioni sulla scrittura di script WinRM, vedere [Using Windows Remote Management](using-windows-remote-management.md).

Nella tabella seguente sono elencati gli argomenti che forniscono informazioni sul protocollo WS-Management, WinRM e WMI, su come specificare le risorse di gestione, ad esempio unità disco o processi.



| Argomento                                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Installazione e configurazione per la Windows remota](installation-and-configuration-for-windows-remote-management.md) | Il [*listener*](windows-remote-management-glossary.md) di Gestione remota Windows richiede la configurazione nei computer client e server.                                                                                                                                                                                                                               |
| [Windows Architettura di gestione remota](windows-remote-management-architecture.md)                                             | Diagramma che illustra i componenti di WinRM e i componenti disponibili nei computer client e server.                                                                                                                                                                                                                                                               |
| [Protocollo WS-Management](ws-management-protocol.md)                                                                             | Descrizione del protocollo WS-Management standard pubblico per l'invio e la ricezione remota dei dati di gestione a qualsiasi dispositivo computer che implementa il protocollo.                                                                                                                                                                                                             |
| [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md)                                             | L'API di scripting winrm è simile alle azioni del protocollo WS-Management winrm. I dati recuperati dagli script vengono formattati in XML, non in oggetti.                                                                                                                                                                                                                                  |
| [Autenticazione per le connessioni remote](authentication-for-remote-connections.md)                                               | WS-Management protocollo mantiene la sicurezza per il trasferimento dei dati tra computer supportando diversi metodi standard di autenticazione e crittografia dei messaggi.                                                                                                                                                                                                                |
| [Windows Gestione remota e WMI](windows-remote-management-and-wmi.md)                                                       | Poiché WinRM è integrato [Windows Management Instrumentation (WMI),](/windows/desktop/WmiSdk/wmi-start-page)è possibile ottenere dati WMI con script o applicazioni che usano l'API scripting [WinRM](winrm-scripting-api.md) o tramite lo strumento da riga di comando Winrm.                                                                                                                     |
| [URI risorse](resource-uris.md)                                                                                               | Un [*URI di risorsa*](windows-remote-management-glossary.md) è un identificatore per un'operazione di gestione o un valore. Ad esempio, le unità disco rappresentano un tipo di risorsa.                                                                                                                                                                              |
| [Gestione hardware remota](remote-hardware-management.md)                                                                     | Il provider [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) fornisce classi e dati che descrivono il dominio di gestione hardware del controller di gestione di base (BMC), i sistemi computer BMC nel dominio e i sensori BMC. [](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) Altri oggetti rappresentano il registro eventi di sistema BMC (SEL) e i messaggi nel log. |
| [Eventi](events.md)                                                                                                             | Non è possibile ottenere eventi tramite script WinRM, ma è possibile usare lo Wevtutil.exe da riga di comando per visualizzare [gli eventi dell'agente di raccolta](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) eventi.                                                                                                                                                                                        |



 

 

 