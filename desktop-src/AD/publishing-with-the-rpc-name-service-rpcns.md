---
title: Pubblicazione con il servizio nome RPC
description: I servizi RPC possono pubblicare i relativi identificatori in uno spazio dei nomi usando le API RpcNs (RPC Name Service).
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Pubblicazione con il nome RPC servizio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b672eec6308d709fe2f4cbc64ad22ecf0d6edd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046496"
---
# <a name="publishing-with-the-rpc-name-service"></a>Pubblicazione con il servizio nome RPC

I servizi RPC possono pubblicare i relativi identificatori in uno spazio dei nomi usando le API RpcNs (RPC Name Service). Le API RpcNs in Windows 2000 pubblicano le voci RPC in Active Directory Domain Services. I servizi creano binding RPC e li pubblicano nello spazio dei nomi come voci del server RPC denominate con attributi che includono l'ID di interfaccia univoco, un GUID riconosciuto dai client. Un client può quindi cercare i server RPC che offrono l'interfaccia desiderata, importare l'associazione e connettersi al server.

Per ulteriori informazioni sulla pubblicazione di un servizio RPC, vedere [Binding lato server](/windows/desktop/Rpc/server-side-binding).

 

 