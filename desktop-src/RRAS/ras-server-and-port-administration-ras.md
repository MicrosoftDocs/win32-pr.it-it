---
title: Amministrazione di server e porte RAS
description: Le funzioni di amministrazione del server RAS consentono di ottenere informazioni su un server RAS specificato e sulle relative porte. Queste funzioni consentono inoltre di terminare una connessione su una porta del server RAS specificata.
ms.assetid: 783b0ded-7c0e-49eb-8040-563d5dd675f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af21dfeda38a1c1147bf864a1fa1959092ac946
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044987"
---
# <a name="ras-server-and-port-administration"></a>Amministrazione di server e porte RAS

Le funzioni di amministrazione del server RAS consentono di ottenere informazioni su un server RAS specificato e sulle relative porte. Queste funzioni consentono inoltre di terminare una connessione su una porta del server RAS specificata.

La funzione [**RasAdminServerGetInfo**](rasadminservergetinfo.md) restituisce una [**struttura \_ server RAS \_ 0**](ras-server-0-str.md) che contiene informazioni sulla configurazione di un server RAS. Le informazioni restituite includono il numero di porte attualmente disponibili per la connessione, il numero di porte attualmente in uso e il numero di versione del server.

La funzione [**RasAdminPortEnum**](rasadminportenum.md) recupera una matrice di strutture di [**\_ porta RAS \_ 0**](ras-port-0-str.md) che contiene informazioni per ognuna delle porte configurate in un server RAS. Le informazioni per ogni porta includono:

-   Nome della porta
-   Informazioni sul dispositivo collegato alla porta
-   Indica se il server RAS associato alla porta è un server Windows NT/Windows 2000
-   Indica se la porta è attualmente in uso e, in caso contrario, informazioni sulla connessione

È possibile chiamare la funzione [**RasAdminPortGetInfo**](rasadminportgetinfo.md) per ottenere informazioni aggiuntive su una porta specificata in un server RAS. Questa funzione restituisce una struttura di [**\_ porta RAS \_ 1**](ras-port-1-str.md) che contiene una struttura di [**\_ porta RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) e informazioni aggiuntive sullo stato corrente della porta. La funzione **RasAdminPortGetInfo** restituisce inoltre una matrice di strutture di [**\_ parametri RAS**](ras-parameters-str.md) che descrivono i valori di tutte le chiavi specifiche del supporto associate alla porta. Una struttura di **\_ parametri RAS** usa un valore dell'enumerazione del [**\_ \_ formato params RAS**](ras-params-format-str.md) per indicare il formato del valore per ogni chiave specifica del supporto.

La funzione [**RasAdminPortGetInfo**](rasadminportgetinfo.md) restituisce inoltre una struttura di [**\_ \_ statistiche della porta RAS**](ras-port-statistics-str.md) che contiene vari contatori statistici per la connessione corrente, se presente, sulla porta. Per una porta che fa parte di una connessione a più collegamenti, **RasAdminPortGetInfo** restituisce le statistiche per la singola porta e le statistiche cumulative per tutte le porte incluse nella connessione. Per reimpostare i contatori delle statistiche per la porta, è possibile usare la funzione [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) . La funzione [**RasAdminPortDisconnect**](rasadminportdisconnect.md) disconnette una porta in uso.

Utilizzare la funzione [**RasAdminFreeBuffer**](rasadminfreebuffer.md) per liberare la memoria allocata dalle funzioni [**RasAdminPortEnum**](rasadminportenum.md) e [**RasAdminPortGetInfo**](rasadminportgetinfo.md) . Utilizzare la funzione [**RasAdminGetErrorString**](rasadmingeterrorstring.md) per ottenere una stringa che descrive un codice di errore RAS restituito da una delle funzioni di amministrazione del server RAS (RASADMIN).

 

 




