---
title: SNMP Management Information Base (MIB)
description: Un mib (Management Information Base) descrive un set di oggetti gestiti. Un'applicazione console di gestione SNMP può modificare gli oggetti in un computer specifico se il servizio SNMP dispone di una DLL dell'agente di estensione che supporta MIB.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf3fac2e24b79da3ea7277010da5a3f96e3664416809bc440097f4ec0b1384e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127601"
---
# <a name="the-snmp-management-information-base-mib"></a>SNMP Management Information Base (MIB)

Un mib (Management Information Base) descrive un set di oggetti gestiti. Un'applicazione console di gestione SNMP può modificare gli oggetti in un computer specifico se il servizio SNMP dispone di una DLL dell'agente di estensione che supporta MIB.

Ogni oggetto gestito in un MIB ha un identificatore univoco. L'identificatore include il tipo dell'oggetto (ad esempio contatore, stringa, misuratore o indirizzo), il livello di accesso dell'oggetto (ad esempio lettura o lettura/scrittura), le restrizioni relative alle dimensioni e le informazioni sull'intervallo.

La tabella seguente contiene un elenco parziale dei MIB forniti con il sistema. Vengono installati con il servizio SNMP nella directory %systemroot% \\ system32. Per un elenco completo di MIB, fare riferimento Windows Resource Kit.



| MIB         | Descrizione                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Dhcp. Mib    | MIB definito da Microsoft che contiene i tipi di oggetto per il monitoraggio del traffico di rete tra host remoti e server DHCP                        |
| HOSTMIB. Mib | Contiene i tipi di oggetto per il monitoraggio e la gestione delle risorse host                                                                                 |
| LMMIB2. Mib  | Vengono illustrati i servizi workstation e server                                                                                                           |
| MIB \_ II.MIB | Contiene Management Information Base (MIB-II), che fornisce un'architettura e un sistema semplici e utilizzabili per la gestione di Internet basate su TCP/IP |
| Vince. Mib    | MIB definito da Microsoft per Windows Internet Name Service (WINS)                                                                               |



 

**Windows NT:** In genere, è possibile copiare un MIB dall'agente di estensione SNMP che supporta il miB specifico. Alcuni MIB aggiuntivi sono disponibili con il Resource Kit Windows NT 4.0.

Le DLL dell'agente di estensione per MIB-II, LAN Manager MIB-II e LE RISORSE HOST MIB vengono installate con il servizio SNMP. Le DLL dell'agente di estensione per gli altri MIB vengono installate quando vengono installati i rispettivi servizi. Al momento dell'avvio del servizio, il servizio SNMP carica tutte le DLL dell'agente di estensione elencate nel Registro di sistema.

Gli utenti possono aggiungere altre DLL dell'agente di estensione che implementano MIB aggiuntivi. A tale scopo, è necessario aggiungere una voce del Registro di sistema per la nuova DLL nel servizio SNMP. Devono anche registrare il nuovo MIB con l'applicazione console di gestione SNMP. Per altre informazioni, vedere la documentazione inclusa nell'applicazione console di gestione.

Per altre informazioni, vedere [Albero dei nomi MIB.](mib-name-tree.md)

 

 




