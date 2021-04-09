---
title: Suggerimenti sulle prestazioni RPC varie
description: In questa sezione vengono illustrati i suggerimenti sulle prestazioni varie per lo sviluppo di server RPC ad alte prestazioni. In questa sezione vengono forniti numerosi suggerimenti che fanno riferimento al client RPC. Lo sviluppo di un client RPC consente al server RPC di eseguire meno lavoro.
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b0b43f996cc0a165076f1d7aab1b69e6fb9b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044347"
---
# <a name="miscellaneous-rpc-performance-tips"></a>Suggerimenti sulle prestazioni RPC varie

In questa sezione vengono illustrati i suggerimenti sulle prestazioni varie per lo sviluppo di server RPC ad alte prestazioni. In questa sezione vengono forniti numerosi suggerimenti che fanno riferimento al client RPC. Lo sviluppo di un client RPC consente al server RPC di eseguire meno lavoro.

## <a name="use-kerberos"></a>Usa Kerberos

Se si utilizza la sicurezza, utilizzare Kerberos. Sul lato server, Kerberos non richiede l'accesso al KDC. In questo modo, il carico di lavoro viene spostato dal server al client, che fornisce server con prestazioni migliori.

## <a name="use-static-identity-tracking"></a>USA rilevamento identità statico

Se si usa la sicurezza, provare a usare il rilevamento statico delle identità. Il rilevamento statico delle identità è più economico in termini di utilizzo delle risorse rispetto al rilevamento dinamico delle identità. Se l'identità del client viene modificata e il server non è in grado di riconoscere la modifica, utilizzare il rilevamento dinamico anziché creare un handle di associazione diverso per ogni identità. Tuttavia, se l'identità è la stessa, assicurarsi che RPC sia a conoscenza di tale fatto, in modo da evitare che RPC effettui verifiche per l'identità modificata ogni volta.

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a>Usare la funzione RpcGetAuthorizationContextForClient

Se è necessario controllare l'accesso in Windows XP, usare la funzione [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) . I contesti Authz risultanti consentono controlli di accesso molto veloci, che vengono memorizzati nella cache in modo efficiente in base al tempo di esecuzione RPC.

## <a name="do-not-modify-the-token-unless-necessary"></a>Non modificare il token a meno che non sia necessario

Se viene utilizzato il rilevamento dinamico delle identità, non modificare il token del thread o del processo, a meno che non sia assolutamente necessario. Anche se è stato modificato in impostazioni precedenti, il token è spesso abbastanza diverso dal sistema di sicurezza per attivare la creazione di un nuovo contesto di sicurezza.

## <a name="consider-mixed-mode-serialization-for-context-handles"></a>Considerare la serializzazione in modalità mista per gli handle

La modalità di serializzazione predefinita per l'handle di contesto viene serializzata (esclusiva). Si consiglia di effettuare tutte le chiamate che non modificano lo stato dell'handle di contesto in modalità di serializzazione condivisa. Per ulteriori informazioni, vedere [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) .

 

 




