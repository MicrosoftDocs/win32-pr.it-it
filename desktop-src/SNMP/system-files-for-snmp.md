---
title: File di sistema per SNMP
description: Nella tabella seguente vengono descritti i file principali correlati al servizio SNMP.
ms.assetid: 513d7c75-2f68-4d7d-897f-493089f045cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb917276fd807835fea703ec27cc66a0d493766d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471099"
---
# <a name="system-files-for-snmp"></a>File di sistema per SNMP

Nella tabella seguente vengono descritti i file principali correlati al servizio SNMP.



| Nome file     | Descrizione                                                                                                                                                                                                                         |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCPMIB.DLL  | DLL dell'agente di estensione che implementa il MIB DHCP definito da Microsoft. Installato solo nei server DHCP.                                                                                                                                 |
| EVNTAGNT.DLL | DLL SNMP che converte i registri eventi in trap SNMP; noto anche come traduttore di eventi SNMP.                                                                                                                                       |
| HOSTMIB.DLL  | DLL dell'agente di estensione che implementa il MIB delle risorse host.                                                                                                                                                                         |
| LMMIB2.DLL   | DLL dell'agente di estensione che implementa LAN Manager MIB-II.                                                                                                                                                                             |
| MGMTAPI.DLL  | Libreria API di gestione SNMP Microsoft. Questa API consente alle applicazioni di gestione SNMP di restare in ascolto per le richieste di gestione SNMP e inviare richieste e ricevere risposte dagli agenti SNMP.                                                |
| MIB. BIN      | Informazioni MIB compilate utilizzate da MGMTAPI.DLL.                                                                                                                                                                                       |
| SNMP.EXE     | Servizio SNMP. Si tratta dell'agente master che riceve le richieste SNMP e le recapita alla DLL dell'agente di estensione appropriato.                                                                                                        |
| SNMPAPI.DLL  | DLL delle utilità SNMP utilizzate dalle DLL dell'agente di estensione SNMP e dalle applicazioni di gestione. Questa DLL contiene un Framework per lo sviluppo di dll dell'agente di estensione.                                                                                   |
| SNMPSNAP.DLL | Applicazione di configurazione SNMP che è un componente di snap-in di Microsoft Management Console (MMC). Lo snap-in aggiunge diverse pagine alla finestra delle proprietà del servizio SNMP. Per ulteriori informazioni, vedere la Guida in linea per il servizio SNMP. |
| SNMPTRAP.EXE | Servizio trap SNMP. Riceve i trap SNMP e li inoltra alle applicazioni di gestione SNMP.                                                                                                                                              |
| WINSMIB.DLL  | DLL dell'agente di estensione che implementa il MIB WINS definito da Microsoft. Installato solo nei server WINS.                                                                                                                                 |
| WSNMP32.DLL  | Libreria [API Microsoft WinSNMP](winsnmp-api.md) . Questa API consente alle applicazioni di gestione SNMP di restare in ascolto per le richieste di gestione SNMP e inviare richieste e ricevere risposte dagli agenti SNMP.                                     |



 

Per ulteriori informazioni, vedere [SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md). È anche possibile fare riferimento al Resource Kit di Windows 2000.

 

 




