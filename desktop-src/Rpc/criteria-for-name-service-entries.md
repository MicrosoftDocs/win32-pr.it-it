---
title: Criteri per le voci del servizio dei nomi
description: Criteri per le voci del servizio di denominazione con RPC (Remote Procedure Call).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb32314dc86b179ea98bdf07000dc5ea359bdc77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471454"
---
# <a name="criteria-for-name-service-entries"></a>Criteri per le voci del servizio dei nomi

Quando si elaborano le voci del servizio di nome, vengono usati i criteri seguenti:

-   Se si specifica un nome di voce non **null** per [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), tale voce sarà l'unica voce cercata per gli handle di associazione. Se si passa **null**, verrà eseguita una ricerca in tutte le voci del dominio di accesso. Si noti che questo non include domini trusted.
-   Se si fornisce un handle di interfaccia, gli handle di associazione vengono restituiti da una voce solo se la sezione dell'interfaccia della voce contiene una versione compatibile di tale UUID dell'interfaccia. Questo significa che il numero di versione principale deve essere uguale a quello dell'interfaccia UUID, mentre il numero di versione secondario deve essere uguale o maggiore di quello dell'utente.
-   Se si specifica un UUID per l'oggetto, gli handle di associazione vengono restituiti da una voce solo se la sezione UUID dell'oggetto della voce contiene tale UUID dell'oggetto specifico.

Se una voce del servizio nome sopravvive ai criteri descritti in precedenza, vengono raccolti tutti gli handle di binding da tali voci. Gli handle con una sequenza di protocollo non supportata dal client vengono rimossi e gli handle rimanenti vengono restituiti all'utente come output di [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).

 

 




