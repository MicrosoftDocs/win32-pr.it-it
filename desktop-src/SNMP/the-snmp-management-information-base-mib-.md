---
title: MIB (Management Information Base) SNMP
description: Un set di oggetti gestiti viene descritto da un MIB (Management Information Base). Un'applicazione console di gestione SNMP può modificare gli oggetti in un computer specifico se il servizio SNMP dispone di una DLL dell'agente di estensione che supporta il MIB.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba4612c026aa5a3a1a1574556f58207bad08e06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708827"
---
# <a name="the-snmp-management-information-base-mib"></a>MIB (Management Information Base) SNMP

Un set di oggetti gestiti viene descritto da un MIB (Management Information Base). Un'applicazione console di gestione SNMP può modificare gli oggetti in un computer specifico se il servizio SNMP dispone di una DLL dell'agente di estensione che supporta il MIB.

Ogni oggetto gestito in un MIB ha un identificatore univoco. L'identificatore include il tipo di oggetto (ad esempio Counter, String, gauge o Address), il livello di accesso dell'oggetto, ad esempio di lettura o di lettura/scrittura, le restrizioni di dimensione e le informazioni sull'intervallo.

La tabella seguente contiene un elenco parziale dei MIB forniti con il sistema. Vengono installati con il servizio SNMP nella directory% SystemRoot% \\ system32. Per un elenco completo di MIB, vedere il Resource Kit di Windows.



| MIB         | Descrizione                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCP. MIB    | MIB definito da Microsoft che contiene i tipi di oggetto per il monitoraggio del traffico di rete tra host remoti e server DHCP                        |
| HOSTMIB. MIB | Contiene i tipi di oggetto per il monitoraggio e la gestione delle risorse host                                                                                 |
| Lmmib2. MIB  | Copre i servizi workstation e server                                                                                                           |
| MIB \_ II. MIB | Contiene il Management Information Base (MIB-II), che fornisce un'architettura semplice e praticabile per la gestione di Internet basati su TCP/IP. |
| WINS. MIB    | MIB definito da Microsoft per Windows Internet Name Service (WINS)                                                                               |



 

**Windows NT:** In genere, è possibile copiare un MIB dall'agente di estensione SNMP che supporta il MIB specifico. Con il Resource Kit di Windows NT 4,0 sono disponibili MIB aggiuntive.

Le DLL dell'agente di estensione per MIB-II, LAN Manager MIB-II e le risorse host MIB vengono installate con il servizio SNMP. Le DLL dell'agente di estensione per gli altri MIB vengono installate quando vengono installati i rispettivi servizi. Al momento dell'avvio del servizio, il servizio SNMP carica tutte le DLL dell'agente di estensione elencate nel registro di sistema.

Gli utenti possono aggiungere altre DLL dell'agente di estensione che implementano MIB aggiuntive. A tale scopo, è necessario aggiungere una voce del registro di sistema per la nuova DLL nel servizio SNMP. Devono inoltre registrare il nuovo MIB con l'applicazione console di gestione SNMP. Per ulteriori informazioni, vedere la documentazione inclusa nell'applicazione console di gestione.

Per ulteriori informazioni, vedere la pagina relativa all' [albero dei nomi MIB](mib-name-tree.md).

 

 




