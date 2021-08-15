---
description: Consente alle applicazioni client di accedere alle informazioni SNMP tramite WMI.
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: Accesso ai dispositivi SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3acf8fd67ee9153167cd328b7a50f6aafc5853327a64baf80c3b2e20b663d3ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320303"
---
# <a name="accessing-snmp-devices"></a>Accesso ai dispositivi SNMP

Il provider Simple Network Management Protocol (SNMP) consente alle applicazioni client di accedere alle informazioni SNMP tramite WMI. Il [provider SNMP](snmp-provider.md) funge da gateway per sistemi e dispositivi che usano SNMP per la gestione. Solo il computer di gestione o monitoraggio deve eseguire WMI perché può leggere da qualsiasi dispositivo abilitato per SNMP.

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Configurazione dell'ambiente SNMP WMI.](setting-up-the-wmi-snmp-environment.md)

 

Le variabili oggetto MIB (Management Information Base) SNMP possono essere lette e scritte in e le trap SNMP possono essere mappate automaticamente agli eventi WMI, che possono essere definiti per qualsiasi operazione di creazione, eliminazione o aggiornamento arbitraria sui dati oltre le trap definite da MIB. Questa funzionalità di WMI funziona come estensione delle funzionalità SNMP standard. Per altre informazioni, vedere [Monitoraggio degli eventi](monitoring-events.md).

Gli strumenti descritti negli argomenti seguenti sono progettati per l'uso da Windows di scripting e programmatori C/C++. È consigliabile acquisire familiarità con WMI, SNMPv1 e SNMPv2C e conoscere i concetti di rete e gestione di rete.

Per altre informazioni sull'uso di WMI con SNMP, vedere [Configurazione dell'ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

 



