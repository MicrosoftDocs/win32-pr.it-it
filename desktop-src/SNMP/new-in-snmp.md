---
title: Novità in SNMP
description: SNMP supporta l'utilizzo di IPv6 a partire da Windows Vista.
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729783"
---
# <a name="new-in-snmp"></a>Novità in SNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

SNMP supporta l'utilizzo di IPv6 a partire da Windows Vista. Tuttavia, SNMP supporta solo IPv6 per le reti che eseguono Windows Server 2008 e Windows Vista. Questo perché SNMP richiede che lo stack di protocolli aggiornato sia disponibile in questi sistemi operativi per il supporto IPv6.

A meno che la rete non sia solo una rete Windows Server 2008, le comunicazioni IPv6 avranno esito negativo, anche se uno stack di protocolli IPv6 è installato separatamente nei computer che eseguono versioni precedenti di Windows. Ad esempio, gli agenti SNMP eseguiti in Windows Server 2003 o Windows XP o Windows 2000 rispondono solo alle query eseguite sui rispettivi indirizzi IPv4.

 

 