---
title: Prestazioni RPC varie Suggerimenti
description: Questa sezione illustra vari suggerimenti sulle prestazioni per lo sviluppo di server RPC ad alte prestazioni. In questa sezione vengono forniti molti suggerimenti che fanno riferimento al client RPC. Lo sviluppo corretto di un client RPC consente al server RPC di eseguire meno operazioni.
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0946b83aae296f7b908babca9135c35a0afe8dbe7588a8292ad66bc19dc6488
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928070"
---
# <a name="miscellaneous-rpc-performance-tips"></a>Prestazioni RPC varie Suggerimenti

Questa sezione illustra vari suggerimenti sulle prestazioni per lo sviluppo di server RPC ad alte prestazioni. In questa sezione vengono forniti molti suggerimenti che fanno riferimento al client RPC. Lo sviluppo corretto di un client RPC consente al server RPC di eseguire meno operazioni.

## <a name="use-kerberos"></a>Usare Kerberos

Se si usa la sicurezza, usare Kerberos. Sul lato server, Kerberos non richiede l'accesso al KDC. In questo modo il carico di lavoro viene spostato dal server al client, che offre server con prestazioni migliori.

## <a name="use-static-identity-tracking"></a>Usare il rilevamento delle identità statiche

Se si usa la sicurezza, provare a usare il rilevamento delle identità statiche. Il rilevamento delle identità statiche è più economico in termini di utilizzo delle risorse rispetto al rilevamento dinamico delle identità. Se l'identità del client cambia e il server non deve essere a conoscenza della modifica, usare il rilevamento dinamico anziché creare un handle di associazione diverso per ogni identità. Tuttavia, se l'identità è la stessa, assicurarsi che RPC sia a conoscenza di questo fatto per evitare che RPC controlli ogni volta la modifica dell'identità.

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a>Usare la funzione RpcGetAuthorizationContextForClient

Se è necessario controllare l'accesso in Windows XP, usare la [**funzione RpcGetAuthorizationContextForClient.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) I contesti Authz risultanti consentono controlli di accesso molto rapidi, che vengono memorizzati in modo efficiente nella cache dal runtime RPC.

## <a name="do-not-modify-the-token-unless-necessary"></a>Non modificare il token a meno che non sia necessario

Se viene usato il rilevamento dinamico delle identità, non modificare il token thread/processo a meno che non sia assolutamente necessario. Anche se viene modificato in base alle impostazioni in precedenza, il token è spesso sufficientemente diverso dal sistema di sicurezza per attivare la creazione di un nuovo contesto di sicurezza.

## <a name="consider-mixed-mode-serialization-for-context-handles"></a>Considerare la serializzazione in modalità mista per gli handle di contesto

La modalità di serializzazione predefinita per l'handle di contesto è serializzata (esclusiva). Valutare la possibilità di effettuare tutte le chiamate che non modificano lo stato dell'handle di contesto in modalità di serializzazione condivisa. Per [**altre informazioni, vedere RpcSsContextLockExclusive.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive)

 

 




