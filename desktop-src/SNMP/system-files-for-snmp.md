---
title: File di sistema per SNMP
description: Nella tabella seguente vengono descritti i file principali correlati al servizio SNMP.
ms.assetid: 513d7c75-2f68-4d7d-897f-493089f045cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 139b83a2d2117af693bcd7ae624ff18d7a18ab5618c9a9597c1e142f62aba07d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886051"
---
# <a name="system-files-for-snmp"></a>File di sistema per SNMP

Nella tabella seguente vengono descritti i file principali correlati al servizio SNMP.



| Nome file     | Descrizione                                                                                                                                                                                                                         |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCPMIB.DLL  | DLL dell'agente di estensione che implementa l'MIB DHCP definito da Microsoft. Installato solo nei server DHCP.                                                                                                                                 |
| EVNTAGNT.DLL | DLL SNMP che converte i log eventi in trap SNMP; noto anche come convertitore di eventi SNMP.                                                                                                                                       |
| HOSTMIB.DLL  | DLL dell'agente di estensione che implementa il MIB delle risorse host.                                                                                                                                                                         |
| LMMIB2.DLL   | DLL dell'agente di estensione che implementa MIB-II di LAN Manager.                                                                                                                                                                             |
| MGMTAPI.DLL  | Libreria di API Gestione Microsoft SNMP. Questa API consente alle applicazioni di gestione SNMP di "restare in ascolto" delle richieste di gestione SNMP e di inviare richieste e ricevere risposte dagli agenti SNMP.                                                |
| Mib. Bin      | Informazioni MIB compilate usate MGMTAPI.DLL.                                                                                                                                                                                       |
| SNMP.EXE     | Servizio SNMP. Si tratta dell'agente master che riceve le richieste SNMP e le recapita alla DLL dell'agente di estensione appropriata.                                                                                                        |
| SNMPAPI.DLL  | DLL delle utilità SNMP usata dalle DLL dell'agente di estensione SNMP e dalle applicazioni di gestione. Questa DLL contiene un framework per lo sviluppo di DLL dell'agente di estensione.                                                                                   |
| SNMPSNAP.DLL | Applicazione di configurazione SNMP che è un Microsoft Management Console snap-in MMC (Microsoft Management Console). Lo snap-in aggiunge diverse pagine alla finestra Proprietà servizio SNMP. Per altre informazioni, vedere la Guida online per il servizio SNMP. |
| SNMPTRAP.EXE | Servizio trap SNMP. Riceve trap SNMP e le inoltra alle applicazioni di gestione SNMP.                                                                                                                                              |
| WINSMIB.DLL  | DLL dell'agente di estensione che implementa il MIB WINS definito da Microsoft. Installato solo nei server WINS.                                                                                                                                 |
| WSNMP32.DLL  | Libreria [api Microsoft WinSNMP.](winsnmp-api.md) Questa API consente alle applicazioni di gestione SNMP di "restare in ascolto" delle richieste di gestione SNMP e di inviare richieste e ricevere risposte dagli agenti SNMP.                                     |



 

Per altre informazioni, vedere [The SNMP Management Information Base (MIB).](the-snmp-management-information-base-mib-.md) È anche possibile fare riferimento al resource kit Windows 2000.

 

 




