---
title: Informazioni sull'amministrazione di server e porte RAS
description: Le funzioni di amministrazione del server RAS ottengono informazioni su un server RAS specificato e sulle relative porte. Queste funzioni vengono utilizzate anche per terminare una connessione su una porta del server RAS specificata.
ms.assetid: eedac23e-d716-451e-b08b-594398656bb5
keywords:
- Amministrazione RAS RRAS, amministrazione server e porta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb9d3cc520efa6bbb492e8d9e967d423548f96a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104472067"
---
# <a name="about-ras-server-and-port-administration"></a>Informazioni sull'amministrazione di server e porte RAS

Le funzioni di amministrazione del server RAS ottengono informazioni su un server RAS specificato e sulle relative porte. Queste funzioni vengono utilizzate anche per terminare una connessione su una porta del server RAS specificata.

La funzione [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) restituisce una struttura del [**\_ Server MPR \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_server_0) che contiene informazioni sulla configurazione di un server RAS. Le informazioni restituite includono il numero di porte attualmente disponibili per le connessioni, il numero di porte attualmente in uso e il numero di versione del server.

La funzione [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) recupera una matrice di strutture di [**\_ porta RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) . Ogni struttura contiene informazioni per una delle porte configurate in un server RAS. Le informazioni per ogni porta includono:

-   Nome della porta
-   Informazioni sul dispositivo collegato alla porta
-   Indica se il server RAS associato alla porta è un server Windows NT/Windows 2000
-   Indica se la porta è attualmente in uso e, in caso contrario, informazioni sulla connessione

Per ottenere le porte utilizzate da una connessione specifica, passare [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) un handle a tale connessione nel parametro *hConnection* . Per ottenere un handle per una connessione, usare la funzione [**MprAdminConnectionEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum) . In alternativa, se è stata implementata una [dll di amministrazione RAS](ras-administration-dll.md), le funzioni [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) e [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) ricevono un handle per ogni nuova connessione nel momento in cui viene stabilita la connessione.

È possibile chiamare la funzione [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) per ottenere informazioni aggiuntive su una porta specificata in un server RAS. Questa funzione restituisce una struttura di [**\_ porta RAS \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) che contiene una struttura di [**\_ porta RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) e informazioni aggiuntive sullo stato corrente della porta. La funzione [**RasAdminPortGetInfo**](rasadminportgetinfo.md) restituisce inoltre una matrice di strutture di [**\_ parametri RAS**](ras-parameters-str.md) che descrivono i valori di tutte le chiavi specifiche del supporto associate alla porta. Una struttura di **\_ parametri RAS** usa un valore dell'enumerazione del [**\_ \_ formato params RAS**](ras-params-format-str.md) per indicare il formato del valore per ogni chiave specifica del supporto.

La funzione [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) restituisce inoltre una struttura di [**\_ \_ statistiche della porta RAS**](ras-port-statistics-str.md) che contiene vari contatori statistici per la connessione corrente, se presente, sulla porta. Per una porta che fa parte di una connessione a più collegamenti, **MprAdminPortGetInfo** restituisce le statistiche per la singola porta e le statistiche cumulative per tutte le porte incluse nella connessione. Per reimpostare i contatori delle statistiche per la porta, è possibile usare la funzione [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) . La funzione [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) disconnette una porta in uso.

Utilizzare la funzione [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) per liberare la memoria allocata dalle funzioni [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) e [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) . Utilizzare la funzione [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) per ottenere una stringa che descrive un codice di errore RAS restituito da una delle funzioni di amministrazione del server RAS (RASADMIN).

 

 




