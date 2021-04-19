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
# <a name="accessing-snmp-devices"></a><span data-ttu-id="a3687-103">Accesso ai dispositivi SNMP</span><span class="sxs-lookup"><span data-stu-id="a3687-103">Accessing SNMP Devices</span></span>

<span data-ttu-id="a3687-104">Il provider Simple Network Management Protocol (SNMP) consente alle applicazioni client di accedere alle informazioni SNMP tramite WMI.</span><span class="sxs-lookup"><span data-stu-id="a3687-104">The Simple Network Management Protocol (SNMP) provider allows client applications to access SNMP information through WMI.</span></span> <span data-ttu-id="a3687-105">Il [provider SNMP](snmp-provider.md) funge da gateway per i sistemi e i dispositivi che utilizzano SNMP per la gestione.</span><span class="sxs-lookup"><span data-stu-id="a3687-105">The [SNMP provider](snmp-provider.md) acts as a gateway to systems and devices that use SNMP for management.</span></span> <span data-ttu-id="a3687-106">Solo il computer di gestione o di monitoraggio deve eseguire WMI perché può leggere da qualsiasi dispositivo abilitato SNMP.</span><span class="sxs-lookup"><span data-stu-id="a3687-106">Only the management or monitoring computer must be running WMI because it can read from any SNMP-enabled device.</span></span>

> [!Note]  
> <span data-ttu-id="a3687-107">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a3687-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="a3687-108">Le variabili oggetto MIB (Management Information Base) SNMP possono essere lette e scritte e i trap SNMP possono essere mappati automaticamente a eventi WMI, che possono essere definiti per qualsiasi operazione di creazione, eliminazione o aggiornamento arbitraria ai dati oltre i trap definiti da MIB.</span><span class="sxs-lookup"><span data-stu-id="a3687-108">SNMP Management Information Base (MIB) object variables can be read from and written to, and SNMP traps can be automatically mapped to WMI events, which can be defined for any arbitrary create, delete, or update operations to data beyond the MIB-defined traps.</span></span> <span data-ttu-id="a3687-109">Questa funzionalità di WMI funge da estensione delle funzionalità SNMP standard.</span><span class="sxs-lookup"><span data-stu-id="a3687-109">This feature of WMI functions as an extension of standard SNMP capabilities.</span></span> <span data-ttu-id="a3687-110">Per ulteriori informazioni, vedere [monitoraggio degli eventi](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="a3687-110">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

<span data-ttu-id="a3687-111">Gli strumenti descritti negli argomenti seguenti sono progettati per l'uso da parte dei programmatori di Windows Scripting e C/C++.</span><span class="sxs-lookup"><span data-stu-id="a3687-111">The tools described in the following topics are designed for use by Windows scripting and C/C++ programmers.</span></span> <span data-ttu-id="a3687-112">Si consiglia di acquisire familiarità con WMI, SNMPv1 e SNMPv2C e una conoscenza approfondita dei concetti relativi alla rete e alla gestione della rete.</span><span class="sxs-lookup"><span data-stu-id="a3687-112">Familiarity with WMI, SNMPv1 and SNMPv2C, and a working knowledge of networking and network management concepts are recommended.</span></span>

<span data-ttu-id="a3687-113">Per ulteriori informazioni sull'utilizzo di WMI con SNMP, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a3687-113">For more information about using WMI with SNMP, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

 



