---
description: Consente alle applicazioni client di accedere alle informazioni SNMP tramite WMI.
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: Accesso ai dispositivi SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a349053f054f3e8ad9dffb7c108d2bee6c6d8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319310"
---
# <a name="accessing-snmp-devices"></a>Accesso ai dispositivi SNMP

Il provider Simple Network Management Protocol (SNMP) consente alle applicazioni client di accedere alle informazioni SNMP tramite WMI. Il [provider SNMP](snmp-provider.md) funge da gateway per i sistemi e i dispositivi che utilizzano SNMP per la gestione. Solo il computer di gestione o di monitoraggio deve eseguire WMI perché può leggere da qualsiasi dispositivo abilitato SNMP.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Le variabili oggetto MIB (Management Information Base) SNMP possono essere lette e scritte e i trap SNMP possono essere mappati automaticamente a eventi WMI, che possono essere definiti per qualsiasi operazione di creazione, eliminazione o aggiornamento arbitraria ai dati oltre i trap definiti da MIB. Questa funzionalità di WMI funge da estensione delle funzionalità SNMP standard. Per ulteriori informazioni, vedere [monitoraggio degli eventi](monitoring-events.md).

Gli strumenti descritti negli argomenti seguenti sono progettati per l'uso da parte dei programmatori di Windows Scripting e C/C++. Si consiglia di acquisire familiarità con WMI, SNMPv1 e SNMPv2C e una conoscenza approfondita dei concetti relativi alla rete e alla gestione della rete.

Per ulteriori informazioni sull'utilizzo di WMI con SNMP, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

 



