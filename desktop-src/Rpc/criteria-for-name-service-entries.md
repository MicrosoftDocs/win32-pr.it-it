---
title: Criteri per le voci del servizio dei nomi
description: Criteri per le voci del servizio dei nomi con RPC (Remote Procedure Call).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609c545c72687a0b9b73db56d2f08654941e464c790e091ee886159d9e9593ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931120"
---
# <a name="criteria-for-name-service-entries"></a>Criteri per le voci del servizio dei nomi

Durante l'elaborazione delle voci del servizio dei nomi vengono utilizzati i criteri seguenti:

-   Se si specifica un nome di voce non **NULL** per [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), tale voce sarà l'unica voce cercata per gli handle di associazione. Se si passa **NULL,** verranno ricercate tutte le voci nel dominio di accesso. Si noti che non sono inclusi i domini trusted.
-   Se si fornisce un handle di interfaccia, gli handle di associazione vengono restituiti da una voce solo se la sezione dell'interfaccia della voce contiene una versione compatibile di tale UUID di interfaccia. Ciò significa che il numero di versione principale deve essere uguale all'UUID dell'interfaccia, mentre il numero di versione secondaria deve essere uguale o maggiore del proprio.
-   Se si specifica un UUID dell'oggetto, gli handle di associazione vengono restituiti da una voce solo se la sezione UUID dell'oggetto della voce contiene tale UUID oggetto specifico.

Se una voce del servizio dei nomi non soddisfa i criteri descritti in precedenza, vengono raccolti tutti gli handle di associazione da tali voci. Gli handle con una sequenza di protocollo non supportata dal client vengono eliminati e gli handle rimanenti vengono restituiti come output da [**RpcNsBindingLookupNext.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)

 

 




