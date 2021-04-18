---
description: I provider di eventi SNMP ricevono pacchetti di eventi SNMP dallo stack WINSNMP e convertono le informazioni incluse nei pacchetti in eventi WMI.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Scelta tra i provider di eventi SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dabd8f6d432025406a5faecc3ace423cd6671e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315738"
---
# <a name="choosing-between-snmp-event-providers"></a>Scelta tra i provider di eventi SNMP

I provider di eventi SNMP ricevono pacchetti di eventi SNMP dallo stack WINSNMP e convertono le informazioni incluse nei pacchetti in eventi WMI.

WMI include i due provider di eventi SNMP seguenti:

-   Provider di eventi incapsulato SNMP (Filtra)

    Il provisioning incapsulato indica che l'istanza dell'evento dispone di proprietà semplici che descrivono le informazioni mappate direttamente dal trap SNMP.

-   Provider di eventi SNMP referente (SREP)

    Il provisioning referente astrae le informazioni presenti all'interno del trap SNMP in modo che le proprietà che condividono la stessa classe e l'istanza vengano presentate come oggetti incorporati. Questo consente di recuperare l'istanza univoca, a cui è associata la trap, dopo la ricezione dell'evento usando il \_ \_ RelPath SNMP.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Indipendentemente dal fatto che l'evento SNMP sia un trap SNMPv1 o una notifica SNMPv2C, lo stack lo segnala come notifica SNMPv2. Pertanto, i provider di eventi elaborano tutti gli eventi SNMP come notifiche di SNMPv2.

Per descrivere gli eventi SNMP ai consumer WMI, ogni provider di eventi supporta una gerarchia di classi che deriva dalla classe di sistema [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) . La classe [SNMPNotification](snmpnotification.md) è la classe padre per la gerarchia di infiltrazione. la classe [SNMPExtendedNotification](snmpextendednotification.md) è la classe padre per la gerarchia di SREP.

 

 



