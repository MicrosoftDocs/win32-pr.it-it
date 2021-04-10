---
title: Gestione remota Windows
description: Gestione remota Windows (Gestione remota Windows) è l'implementazione Microsoft del protocollo WS-Management, un protocollo standard basato su SOAP, che consente l'interoperabilità di hardware e sistemi operativi di fornitori diversi.
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows (WinRM), pagina iniziale
- WS-Management
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27311699fe0321eddc1d3117b17acf3e49e9d518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963114"
---
# <a name="windows-remote-management"></a>Gestione remota Windows

## <a name="purpose"></a>Scopo

Gestione remota Windows (WinRM) è l'implementazione di Microsoft del [protocollo WS-Management](ws-management-protocol.md), un protocollo standard basato su SOAP (Simple Object Access Protocol) adatto al firewall che consente l'interoperabilità di hardware e sistemi operativi di fornitori diversi.

La specifica del protocollo WS-Management consente ai sistemi di accedere alle informazioni di gestione e scambiarle attraverso un'infrastruttura IT in modo comune. WinRM e [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md), insieme all' [agente di raccolta eventi](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) sono componenti delle funzionalità di [gestione hardware di Windows](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) .

## <a name="where-applicable"></a>Se applicabile

È possibile utilizzare gli oggetti di scripting WinRM, lo strumento da riga di comando WinRM o lo strumento da riga di comando Windows Remote Shell WinRS per ottenere i dati di gestione da computer locali e remoti che possono disporre di [*controller di gestione battiscopa (BMC)*](windows-remote-management-glossary.md). Se il computer esegue una versione del sistema operativo basata su Windows che include WinRM, i dati di gestione vengono forniti da [Strumentazione gestione Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page).

È inoltre possibile recuperare dati di sistema e hardware dalle implementazioni del protocollo WS-Management in esecuzione nella propria azienda su sistemi operativi diversi da Windows. A differenza di WMI, WinRM stabilisce una sessione con un computer remoto tramite il protocollo WS-Management basato su SOAP anziché una connessione mediante DCOM. I dati restituiti al protocollo WS-Management sono formattati in XML anziché in oggetti.

Il provider WMI di [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) è un provider WMI standard con classi che ottengono dati del sensore BMC da computer con hardware appropriato. È possibile accedere ai dati IPMI usando l'API di scripting WinRM, lo [Scripting](/windows/desktop/WmiSdk/scripting-api-for-wmi)WMI o le API [com](/windows/desktop/WmiSdk/com-api-for-wmi) .

## <a name="developer-audience"></a>Sviluppatori

I destinatari degli sviluppatori sono i professionisti IT che scrivono gli script per automatizzare la gestione dei server o degli sviluppatori ISV che ottengono dati per le applicazioni di gestione.

## <a name="run-time-requirements"></a>Requisiti di runtime

WinRM fa parte del sistema operativo. Tuttavia, per ottenere i dati da computer remoti, è necessario configurare un [*listener*](windows-remote-management-glossary.md#l)WinRM. Per ulteriori informazioni, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md). Se viene rilevato un BMC all'avvio del sistema, il provider IPMI viene caricato; in caso contrario, gli oggetti di scripting WinRM e lo strumento da riga di comando WinRM sono ancora disponibili.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> <dd>

Collegamento alla specifica del protocollo public WS-Management, all'architettura WinRM, alla relazione con WMI, alla gestione dell'hardware con il provider IPMI, alla configurazione e all'installazione.

</dd> <dt>

[Utilizzo di Gestione remota Windows](using-windows-remote-management.md)
</dt> <dd>

Introduzione all'uso dell'API di scripting WinRM e della gestione dell'hardware.

</dd> <dt>

[Riferimento Gestione remota Windows](windows-remote-management-reference.md)
</dt> <dd>

Elenco di interfacce di scripting definite dall'automazione di Microsoft Web Services for Management (WS-Management) e dalle definizioni delle classi WMI create dal provider IPMI e dalle classi che comunicano con il driver IPMI per ottenere i dati [Baseboard Management Controller (BMC)](windows-remote-management-glossary.md) .

</dd> </dl>

 

 