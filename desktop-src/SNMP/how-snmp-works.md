---
title: Funzionamento di SNMP
description: Il modo in cui un'applicazione console di gestione SNMP di terze parti restituisce informazioni dal servizio SNMP.
ms.assetid: 2edbf9ff-b9e3-4103-affc-a5c0f22b80a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d58943f0765b60f9c235094642d3fa759402db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955329"
---
# <a name="how-snmp-works"></a>Funzionamento di SNMP

Nei passaggi seguenti viene illustrato il modo in cui un'applicazione console di gestione SNMP di terze parti restituisce informazioni dal servizio SNMP:

1.  L'applicazione console di gestione SNMP formula un messaggio SNMP basato sull'input dell'utente. Il messaggio include un'unità dati di protocollo (PDU) e le informazioni di autenticazione. L'applicazione console di gestione può utilizzare la libreria API di gestione SNMP Microsoft (MGMTAPI.DLL) o la libreria [API Microsoft WinSNMP](winsnmp-api.md) (WSNMP32.DLL) per eseguire questo passaggio.
2.  L'applicazione console di gestione SNMP Invia il messaggio SNMP al servizio SNMP utilizzando le librerie del servizio SNMP.
3.  Il servizio SNMP riceve la richiesta. Verifica le informazioni di autenticazione e l'indirizzo IP di origine.
4.  Il servizio SNMP seleziona l'agente di estensione appropriato e richiede che l'agente recuperi le informazioni richieste.
5.  Il servizio SNMP Invia la risposta all'applicazione console di gestione SNMP.

 

 




