---
title: Pubblicazione con il servizio nomi RPC
description: I servizi RPC possono pubblicare gli identificatori in uno spazio dei nomi usando le API RPC Name Service (RpcNs).
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Pubblicazione con RPC Name Service AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd53922bd4ce952c18c58d1b71cb485887bdc0fd020f4113679eb114b32b6f3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025369"
---
# <a name="publishing-with-the-rpc-name-service"></a>Pubblicazione con il servizio nomi RPC

I servizi RPC possono pubblicare gli identificatori in uno spazio dei nomi usando le API RPC Name Service (RpcNs). Le API RpcNs in Windows 2000 pubblicano le voci RPC in Active Directory Domain Services. I servizi creano associazioni RPC e le pubblicano nello spazio dei nomi come voci del server RPC denominate con attributi che includono l'ID univoco dell'interfaccia, un GUID riconosciuto dai client. Un client può quindi cercare i server RPC che offrono l'interfaccia desiderata, importare l'associazione e connettersi al server.

Per altre informazioni sulla pubblicazione di un servizio RPC, vedere [Associazione lato server](/windows/desktop/Rpc/server-side-binding).

 

 