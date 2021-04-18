---
title: /version_stamp opzione
description: L' \_ interruttore/Version Stamp disattiva la generazione di macro che specificano il numero minimo di versione necessario del file di intestazione RPC, Rpcndr. h.
ms.assetid: ec03f68b-60f7-431e-9fba-4434ef082058
keywords:
- /version_stamp switch MIDL
topic_type:
- apiref
api_name:
- /version_stamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704393dce869df4e5f715a1157cdb57967135e42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299170"
---
# <a name="version_stamp-switch"></a>\_opzione Stamp/Version

L'interruttore **/version \_ Stamp** disattiva la generazione di macro che specificano il numero minimo di versione necessario del file di intestazione RPC, Rpcndr. h.

Le nuove funzionalità MIDL potrebbero richiedere definizioni aggiuntive per compilare correttamente lo stub, quindi lo stub include macro che controllano la compatibilità tra i file binari MIDL e l'ambiente di compilazione. Potrebbe essere necessario usare questa opzione se si sposta MIDL in un ambiente di compilazione diverso da quello in cui sono stati installati prima i file binari MIDL.

Si noti che la combinazione di ambienti di compilazione non è supportata.

``` syntax
midl /version_stamp
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

 

 




