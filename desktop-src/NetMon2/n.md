---
description: Glossario dei termini Network Monitor che iniziano con la lettera N.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: a9b0e907-45c0-4301-9e83-398dd1c1c39a
title: N (Network Monitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54404640b13bff3b098b9d223e656e8f1905c055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883662"
---
# <a name="n-network-monitor"></a>N (Network Monitor)

<dl> <dt>

<span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**NDIS**
</dt> <dd>

Vedere Specifica dell'interfaccia del driver di rete.

</dd> <dt>

<span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**specifiche di Network Driver Interface (NDIS)**
</dt> <dd>

Specifica per l'interfaccia tra i driver di dispositivo e una rete. Tutti i trasporti chiamano l'interfaccia NDIS per accedere alle schede di interfaccia di rete e utilizzarle.

</dd> <dt>

<span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Agente di Network Monitor**
</dt> <dd>

Componente Network Monitor. L'agente consente a un computer remoto di acquisire i dati dalla rete. Quando un'installazione di Network Monitor si connette in remoto all'agente di Network Monitor e avvia un'acquisizione, le statistiche dall'acquisizione vengono trasferite attraverso la rete al computer di gestione. Il trasferimento procede a intervalli specificati quando viene steffettuata la connessione.

</dd> <dt>

<span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**provider di pacchetti di rete (NPP)**
</dt> <dd>

Il componente Network Monitor che raccoglie il traffico di rete nei frame, quindi passa i frame a un'applicazione Expert e NPP. Un NPP usa il driver di sistema Network Monitor (Nmnt.sys) per ottenere i frame raccolti dalla rete e offre diverse interfacce COM che passano i frame a un'applicazione Expert, monitor e Network Packet Provider (NPP) in cui possono essere visualizzati e analizzati.

</dd> <dt>

<span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**NPP**
</dt> <dd>

Vedere provider di pacchetti di rete.

</dd> <dt>

<span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**Applicazione NPP**
</dt> <dd>

Applicazione che ignora sia l'interfaccia utente di Network Monitor che lo strumento di controllo del monitoraggio e si connette direttamente al provider di pacchetti di rete (NPP). Un'applicazione NPP può connettersi al componente NPP con una delle cinque interfacce COM di NPP.

</dd> <dt>

<span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**Ricerca NPP**
</dt> <dd>

Componente Network Monitor che comunica con centrali.

</dd> </dl>

 

 



