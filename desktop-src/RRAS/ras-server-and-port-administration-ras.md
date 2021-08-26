---
title: Amministrazione di server e porte RAS
description: Le funzioni di amministrazione del server RAS consentono di ottenere informazioni su un server RAS specificato e sulle relative porte. Queste funzioni consentono anche di terminare una connessione su una porta del server RAS specificata.
ms.assetid: 783b0ded-7c0e-49eb-8040-563d5dd675f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d09d683bf0850b5f51a5d9c1ac1aa21b25f2968ddedbed2d383d28dad7785f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028801"
---
# <a name="ras-server-and-port-administration"></a>Amministrazione di server e porte RAS

Le funzioni di amministrazione del server RAS consentono di ottenere informazioni su un server RAS specificato e sulle relative porte. Queste funzioni consentono anche di terminare una connessione su una porta del server RAS specificata.

La [**funzione RasAdminServerGetInfo**](rasadminservergetinfo.md) restituisce una [**struttura RAS SERVER \_ \_ 0**](ras-server-0-str.md) che contiene informazioni sulla configurazione di un server RAS. Le informazioni restituite includono il numero di porte attualmente disponibili per la connessione, il numero di porte attualmente in uso e il numero di versione del server.

La [**funzione RasAdminPortEnum**](rasadminportenum.md) recupera una matrice di strutture [**RAS PORT \_ \_ 0**](ras-port-0-str.md) che contiene informazioni per ognuna delle porte configurate in un server RAS. Le informazioni per ogni porta includono:

-   Nome della porta
-   Informazioni sul dispositivo collegato alla porta
-   Indica se il server RAS associato alla porta è Windows NT/Windows 2000 Server
-   Indica se la porta è attualmente in uso e, in caso contrario, informazioni sulla connessione

È possibile chiamare la [**funzione RasAdminPortGetInfo**](rasadminportgetinfo.md) per ottenere informazioni aggiuntive su una porta specificata in un server RAS. Questa funzione restituisce una [**struttura RAS \_ PORT \_ 1**](ras-port-1-str.md) che contiene una [**struttura RAS PORT \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) e informazioni aggiuntive sullo stato corrente della porta. La **funzione RasAdminPortGetInfo** restituisce anche una matrice di [**strutture \_ PARAMETERS RAS**](ras-parameters-str.md) che descrivono i valori di qualsiasi chiave specifica del supporto associata alla porta. Una **struttura \_ PARAMETERS RAS** usa un valore dell'enumerazione RAS [**\_ PARAMS \_ FORMAT**](ras-params-format-str.md) per indicare il formato del valore per ogni chiave specifica del supporto.

La [**funzione RasAdminPortGetInfo**](rasadminportgetinfo.md) restituisce anche una struttura [**RAS PORT \_ \_ STATISTICS**](ras-port-statistics-str.md) che contiene vari contatori delle statistiche per la connessione corrente, se presenti, sulla porta. Per una porta che fa parte di una connessione multilink, **RasAdminPortGetInfo** restituisce statistiche per la singola porta e statistiche cumulative per tutte le porte coinvolte nella connessione. È possibile usare la [**funzione RasAdminPortClearStatistics**](rasadminportclearstatistics.md) per reimpostare i contatori delle statistiche per la porta. La [**funzione RasAdminPortDisconnect**](rasadminportdisconnect.md) disconnette una porta in uso.

Usare la [**funzione RasAdminFreeBuffer**](rasadminfreebuffer.md) per liberare la memoria allocata dalle [**funzioni RasAdminPortEnum**](rasadminportenum.md) e [**RasAdminPortGetInfo.**](rasadminportgetinfo.md) Usare la [**funzione RasAdminGetErrorString**](rasadmingeterrorstring.md) per ottenere una stringa che descrive un codice di errore RAS restituito da una delle funzioni di amministrazione del server RAS (RasAdmin).

 

 




