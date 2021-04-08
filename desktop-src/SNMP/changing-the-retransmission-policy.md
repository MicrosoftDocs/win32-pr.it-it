---
title: Modifica dei criteri di ritrasmissione
description: L'implementazione di Microsoft WinSNMP fornisce supporto per i criteri di ritrasmissione archiviando un valore di timeout e un numero di tentativi per l'applicazione WinSNMP in un database.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f21fc479517b8844e9c1db75834b5b1c02edc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856189"
---
# <a name="changing-the-retransmission-policy"></a>Modifica dei criteri di ritrasmissione

L'implementazione di Microsoft WinSNMP fornisce supporto per i criteri di ritrasmissione archiviando un valore di timeout e un numero di tentativi per l'applicazione WinSNMP in un database. L'implementazione archivia i valori per le singole entità di destinazione. L'implementazione fornisce inizialmente i valori predefiniti per questi elementi, ma un'applicazione può aggiungere o modificare i valori per le singole entità.

Una chiamata alle funzioni [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) e [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) restituisce i valori di timeout e di ripetizione dei tentativi per un'entità di destinazione specifica. Per modificare il valore di timeout, un'applicazione WinSNMP deve chiamare la funzione [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) . Per modificare il valore del numero di tentativi, l'applicazione deve chiamare la funzione [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) . Le impostazioni aggiornate influiscono sulle nuove richieste di messaggi SNMP all'entità di destinazione.

 

 




