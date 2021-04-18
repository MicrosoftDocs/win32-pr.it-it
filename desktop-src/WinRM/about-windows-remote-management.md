---
title: Informazioni su Gestione remota Windows
description: Gestione remota Windows è un componente delle funzionalità di gestione hardware di Windows che gestiscono l'hardware del server in locale e in remoto.
ms.assetid: f58add53-0746-4423-9ab8-02ba05f82fa7
ms.tgt_platform: multiple
keywords:
- Informazioni su Gestione remota Windows
- Gestione remota Windows, informazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9221676d3a9864e4fc88fc57c5bb6691512c220a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300381"
---
# <a name="about-windows-remote-management"></a>Informazioni su Gestione remota Windows

Gestione remota Windows è un componente delle funzionalità di [gestione hardware di Windows](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) che gestiscono l'hardware del server in locale e in remoto. Queste funzionalità includono un servizio che implementa il protocollo [*WS-Management*](windows-remote-management-glossary.md) , la diagnosi e il controllo dell'hardware tramite i controller di gestione di [*BMC*](windows-remote-management-glossary.md)e un'API com e [oggetti di scripting](winrm-scripting-api.md) che consentono di scrivere applicazioni che comunicano in modalità remota tramite il protocollo WS-Management. Per ulteriori informazioni sulla specifica pubblica per il protocollo WS-Management, vedere [Web Services for Management (WS-Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).

## <a name="components-of-winrm-and-hardware-management"></a>Componenti di gestione remota Windows e hardware

Di seguito è riportato un elenco di componenti e funzionalità forniti da WinRM e dal monitoraggio hardware:

-   [API di scripting WinRM](winrm-scripting-api.md)

    Questa API di scripting consente di ottenere dati da computer remoti tramite script che eseguono operazioni di WS-Management protocollo.

-   **WinRM. cmd**

    Questo strumento da riga di comando per la gestione del sistema viene implementato in un file Visual Basic Scripting Edition (Winrm.vbs) scritto utilizzando l'API di scripting WinRM. Questo strumento consente a un amministratore di configurare WinRM e di ottenere dati o gestire le risorse. Per ulteriori informazioni, vedere la guida online fornita dalla riga di comando **WinRM** **/?**.

-   **Winrs.exe**

    Questo strumento da riga di comando consente agli amministratori di eseguire in modalità remota la maggior parte dei Cmd.exe comandi utilizzando il protocollo di WS-Management. Per ulteriori informazioni, vedere la guida online fornita dalla riga di comando **winrs** **/?**.

-   Driver IPMI (Intelligent Platform Management Interface) e provider WMI

    La gestione dell'hardware tramite il provider e il driver [*IPMI (Intelligent Platform Management Interface)*](windows-remote-management-glossary.md) consente di controllare e diagnosticare l'hardware del server remoto tramite BMC quando il sistema operativo non è in esecuzione o distribuito.

    Per ulteriori informazioni, vedere il [provider IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

-   Servizio WMI

    Il servizio WMI continua a essere eseguito side-by-side con WinRM e fornisce i dati o il controllo richiesti tramite il [*plug-in WMI*](windows-remote-management-glossary.md). È possibile continuare a ottenere i dati dalle classi WMI standard, ad esempio il [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process), oltre ai dati forniti da IPMI. Per ulteriori informazioni sulla configurazione e l'installazione necessarie per WinRM, vedere [Introduzione alla gestione dell'hardware](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)).

-   Protocollo WS-Management

    WS-Management protocollo, un protocollo intuitivo e basato su SOAP, è stato progettato per i sistemi per individuare e scambiare le informazioni di gestione. Lo scopo della specifica del protocollo WS-Management è garantire l'interoperabilità e la coerenza per i sistemi aziendali con computer in esecuzione in un'ampia gamma di sistemi operativi di fornitori diversi.

    Il protocollo WS-Management si basa sulle specifiche del servizio Web standard seguenti: HTTPS, SOAP su HTTP (WS-I profile), SOAP 1,2, WS-Addressing, WS-Transfer, WS-Enumeration e WS-Eventing. Per ulteriori informazioni sulla bozza corrente della specifica, vedere la pagina relativa all' [Indice delle specifiche di gestione](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

## <a name="working-with-winrm"></a>Utilizzo di WinRM

Per ulteriori informazioni sulla scrittura di script WinRM, vedere [utilizzo di gestione remota Windows](using-windows-remote-management.md).

Nella tabella seguente sono elencati gli argomenti che forniscono informazioni sul protocollo WS-Management, WinRM e WMI, su come specificare le risorse di gestione, ad esempio le unità disco o i processi.



| Argomento                                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Installazione e configurazione per Gestione remota Windows](installation-and-configuration-for-windows-remote-management.md) | Il [*listener*](windows-remote-management-glossary.md) WinRM richiede la configurazione nei computer client e server.                                                                                                                                                                                                                               |
| [Architettura Gestione remota Windows](windows-remote-management-architecture.md)                                             | Diagramma che illustra i componenti di WinRM e quali componenti si trovano nei computer client e server.                                                                                                                                                                                                                                                               |
| [Protocollo WS-Management](ws-management-protocol.md)                                                                             | Descrizione del protocollo WS-Management standard pubblico per l'invio e la ricezione di dati di gestione in modalità remota a qualsiasi dispositivo del computer che implementi il protocollo.                                                                                                                                                                                                             |
| [Creazione di script in Gestione remota Windows](scripting-in-windows-remote-management.md)                                             | L'API di scripting WinRM è simile alle azioni del protocollo WS-Management. I dati recuperati dagli script sono formattati in XML, non in oggetti.                                                                                                                                                                                                                                  |
| [Autenticazione per le connessioni remote](authentication-for-remote-connections.md)                                               | WS-Management protocollo mantiene la sicurezza per il trasferimento dei dati tra computer, supportando diversi metodi standard di autenticazione e crittografia dei messaggi.                                                                                                                                                                                                                |
| [Gestione remota Windows e WMI](windows-remote-management-and-wmi.md)                                                       | Poiché WinRM è integrato con [Strumentazione gestione Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page), è possibile ottenere dati WMI con script o applicazioni che utilizzano l' [API di scripting WinRM](winrm-scripting-api.md) o tramite lo strumento da riga di comando WinRM.                                                                                                                     |
| [URI risorse](resource-uris.md)                                                                                               | Un [*URI di risorsa*](windows-remote-management-glossary.md) è un identificatore per un'operazione di gestione o un valore. Ad esempio, le unità disco rappresentano un tipo di risorsa.                                                                                                                                                                              |
| [Gestione hardware remota](remote-hardware-management.md)                                                                     | Il [provider IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) fornisce le [classi](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) e i dati che descrivono il dominio di gestione hardware Baseboard Management Controller (BMC), i sistemi di computer BMC nel dominio e i sensori BMC. Altri oggetti rappresentano il registro eventi di sistema BMC (SEL) e i messaggi nel log. |
| [Eventi](events.md)                                                                                                             | Non è possibile ottenere gli eventi tramite lo script WinRM, ma è possibile usare lo strumento da riga di comando Wevtutil.exe per visualizzare gli eventi dell' [agente di raccolta eventi](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) .                                                                                                                                                                                        |



 

 

 