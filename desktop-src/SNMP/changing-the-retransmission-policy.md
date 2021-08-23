---
title: Modifica dei criteri di ritrasmissione
description: L'implementazione Microsoft WinSNMP fornisce il supporto dei criteri di ritrasmissione archiviando un valore di timeout e un numero di tentativi per l'applicazione WinSNMP in un database.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed160de40b300d1b2430304b7a487f4544fee9a13db6049d1d837958276da8e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009769"
---
# <a name="changing-the-retransmission-policy"></a>Modifica dei criteri di ritrasmissione

L'implementazione Microsoft WinSNMP fornisce il supporto dei criteri di ritrasmissione archiviando un valore di timeout e un numero di tentativi per l'applicazione WinSNMP in un database. L'implementazione archivia i valori per le singole entità di destinazione. L'implementazione fornisce inizialmente valori predefiniti per questi elementi, ma un'applicazione può aggiungere o modificare valori per singole entità.

Una chiamata alle [**funzioni SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) e [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) restituisce i valori di timeout e numero di tentativi per un'entità di destinazione specifica. Per modificare il valore di timeout, un'applicazione WinSNMP deve chiamare la [**funzione SnmpSetTimeout.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) Per modificare il valore del numero di tentativi, l'applicazione deve chiamare la [**funzione SnmpSetRetry.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) Le impostazioni aggiornate influiscono sulle nuove richieste di messaggi SNMP all'entità di destinazione.

 

 




