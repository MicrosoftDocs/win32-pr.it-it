---
description: I provider di eventi SNMP ricevono pacchetti di eventi SNMP dallo stack WINSNMP e converte le informazioni incluse nei pacchetti in eventi WMI.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Scelta tra provider di eventi SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0902c463ee0fc51505e125a329f592ebced6df20ec7f63296ba7248cd8dade98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131874"
---
# <a name="choosing-between-snmp-event-providers"></a>Scelta tra provider di eventi SNMP

I provider di eventi SNMP ricevono pacchetti di eventi SNMP dallo stack WINSNMP e converte le informazioni incluse nei pacchetti in eventi WMI.

WMI include i due provider di eventi SNMP seguenti:

-   Provider di eventi incapsulati SNMP (SEEP)

    Il provisioning incapsulato significa che l'istanza dell'evento dispone di proprietà semplici che descrivono le informazioni mappate direttamente dalla trap SNMP.

-   Provider di eventi di riferimento SNMP (SREP)

    Il provisioning referenziato astrae le informazioni presenti nel trap SNMP in modo che le proprietà che condividono la stessa classe e la stessa istanza siano presentate come oggetti incorporati. In questo modo l'istanza univoca, a cui è associata la trap, può essere recuperata dopo la ricezione dell'evento, usando IL PERCORSO \_ \_ RELPATH SNMP.

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).

 

Indipendentemente dal fatto che l'evento SNMP sia una trap SNMPv1 o una notifica SNMPv2C, lo stack lo segnala come notifica SNMPv2. Di conseguenza, i provider di eventi elaborano tutti gli eventi SNMP come notifiche SNMPv2.

Per descrivere gli eventi SNMP ai consumer WMI, ogni provider di eventi supporta una gerarchia di classi che deriva dalla classe di sistema [**\_ \_ ExtrinsicEvent.**](--extrinsicevent.md) La [classe SNMPNotification](snmpnotification.md) è la classe padre per la gerarchia SEEP. La [classe SNMPExtendedNotification](snmpextendednotification.md) è la classe padre per la gerarchia SREP.

 

 



