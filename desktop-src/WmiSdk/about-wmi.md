---
description: Strumentazione gestione Windows (WMI) è l'implementazione di Microsoft di Web-Based Enterprise Management (WBEM), un'iniziativa di settore per lo sviluppo di una tecnologia standard per l'accesso alle informazioni di gestione in un ambiente aziendale.
ms.assetid: d745cf25-a139-439d-9ac5-e7720b640516
ms.tgt_platform: multiple
title: Informazioni su WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cf42ead6c3ae1b364ab8f83c83a744afa28734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348416"
---
# <a name="about-wmi"></a>Informazioni su WMI

Strumentazione gestione Windows (WMI) è l'implementazione di Microsoft di Web-Based Enterprise Management (WBEM), un'iniziativa di settore per lo sviluppo di una tecnologia standard per l'accesso alle informazioni di gestione in un ambiente aziendale. WMI utilizza lo standard di settore Common Information Model (CIM) per rappresentare sistemi, applicazioni, reti, dispositivi e altri componenti gestiti. CIM viene sviluppato e gestito da Distributed Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)).

> [!Note]  
> La nuova generazione di WMI, nota come Windows Management Infrastructure (MI), è attualmente disponibile. MI è completamente compatibile con le versioni precedenti di WMI e offre una serie di funzionalità e vantaggi che semplificano la progettazione e lo sviluppo di provider e client. Molti provider più recenti, ad esempio, vengono scritti usando il Framework MI, ma è possibile accedervi tramite script e applicazioni WMI. Per altre informazioni sulle differenze tra le due tecnologie, vedere [perché usare mi?](/previous-versions/windows/desktop/wmi_v2/why-use-mi-)

 

## <a name="managing-remote-computer-systems-with-wmi"></a>Gestione dei sistemi di computer remoti con WMI

WMI risulta utile perché consente di recuperare dati di gestione da computer remoti. Le connessioni remote WMI vengono stabilite tramite DCOM. In alternativa, è possibile utilizzare Gestione remota Windows ([WinRM](/windows/desktop/WinRM/portal)), che consente di ottenere dati di gestione WMI remoti utilizzando il protocollo WS-Management basato su SOAP.

## <a name="programming-with-wmi"></a>Programmazione con WMI

Le applicazioni o gli script di gestione possono recuperare dati o eseguire operazioni tramite WMI in un'ampia gamma di linguaggi. Per ulteriori informazioni, vedere la sezione destinatari per sviluppatori all' [Strumentazione gestione Windows](wmi-start-page.md).

Molte funzionalità di Windows dispongono di provider WMI associati, ad esempio il [provider di dati configurazione di avvio (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) o il [provider del volume di archiviazione](/previous-versions/windows/desktop/vdswmi/storage-volume-provider). I provider WMI implementano la funzionalità descritta dai metodi e dalle proprietà delle classi WMI per gestire le funzionalità di Windows associate. Per ulteriori informazioni, vedere [provider WMI](wmi-providers.md) e [classi WMI](wmi-classes.md).

Per ulteriori informazioni su come scrivere un provider per fornire dati da nuovi componenti hardware o applicazioni, vedere la pagina relativa [alla fornitura di dati a WMI](providing-data-to-wmi.md).

Per ulteriori informazioni sull'implementazione di questa tecnologia, vedere [utilizzo di WMI](using-wmi.md).

Nella tabella seguente sono elencati gli argomenti inclusi in questa sezione.



| Sezione                                                                                                | Descrizione                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novità di WMI](what-s-new-in-wmi.md)                                                             | Nuove funzionalità di WMI.                                                                                                                                                                                                                              |
| [Disponibilità del sistema operativo dei componenti WMI](operating-system-availability-of-wmi-components.md) | Alcuni componenti non sono più disponibili o sono disponibili come installazione facoltativa.                                                                                                                                                             |
| [Architettura WMI](wmi-architecture.md)                                                               | Un'applicazione di gestione comunica con WMI utilizzando un'ampia gamma di interfacce, ad esempio Visual Basic, C++, ODBC e ActiveX. Tutte le interfacce WMI sono basate sulla Component Object Model (COM).                                              |
| [Common Information Model](common-information-model.md)                                               | Un modello di programmazione indipendente dal linguaggio che usa tecniche orientate a oggetti per descrivere un'azienda.                                                                                                                                          |
| [MOF (Managed Object Format)](managed-object-format--mof-.md)                                               | Formato che consente di creare codice leggibile, che può essere convertito dal sistema operativo in un set di classi CIM. È possibile utilizzare le nuove classi per modellare e controllare le nuove tecnologie per un'organizzazione.                                 |
| [Controllo dell'account utente e WMI](user-account-control-and-wmi.md)                                       | Il controllo dell'account utente influiscono sui dati WMI restituiti, sull'accesso remoto e sul modo in cui è necessario eseguire gli script. Per ulteriori informazioni, vedere [Introduzione con controllo dell'account utente in Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista). |
| [Accesso a oggetti a protezione diretta WMI](access-to-wmi-securable-objects.md)                                 | WMI utilizza gli oggetti e le procedure standard di sicurezza di Windows per controllare e proteggere l'accesso a oggetti a protezione diretta come spazi dei nomi WMI, stampanti, servizi e applicazioni DCOM.                                                                      |
| [Librerie di prestazioni e WMI](performance-libraries-and-wmi.md)                                     | I dati dei contatori delle prestazioni di sistema sono disponibili nelle classi WMI.                                                                                                                                                                            |
| [Supporto di IPv6 e IPv4 in WMI](ipv6-and-ipv4-support-in-wmi.md)                                       | Il [provider di route IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI e le classi di rete forniscono i dati per gli indirizzi IPv4. A partire da Windows Vista, WMI fornisce anche il supporto limitato per le funzionalità di rete IPv6.                                       |
| [Formato di data e ora](date-and-time-format.md)                                                       | WMI usa i formati di data e ora definiti dalla specifica di Distributed Management Task Force CIM. Per ulteriori informazioni, vedere [DMTF](https://www.dmtf.org/).                                                          |
| [Creazione di script per l'accesso a WMI](scripting-access-to-wmi.md)                                                 | Scrivere script WMI per eseguire attività di gestione.                                                                                                                                                                                                    |
| [Risoluzione dei problemi WMI](wmi-troubleshooting.md)                                                         | Quando si accede a dati locali o remoti WMI in un'applicazione o in uno script, è possibile che si verifichino errori da classi mancanti a accesso negato. Ai provider sono inoltre disponibili opzioni di debug e classi di risoluzione dei problemi.                           |
| [Altre informazioni](further-information.md)                                                         | Siti Web, libri e articoli relativi a WMI.                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di WMI](using-wmi.md)
</dt> <dt>

[Informazioni di riferimento su WMI](wmi-reference.md)
</dt> </dl>

 

 
