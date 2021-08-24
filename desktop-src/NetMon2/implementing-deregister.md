---
description: Network Monitor passa tutti i frame di un'acquisizione ai parser e quindi inizia a chiamare la funzione Deregister per tutti i protocolli identificati. Ogni DLL del parser deve implementare una funzione Deregister per ogni protocollo supportato dalla DLL del parser.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Implementazione dell'annullamento della registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444502ba3ab19921a6372d4cda872aed85e879cbbdadc2f0176a7187bfc24491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890481"
---
# <a name="implementing-deregister"></a>Implementazione dell'annullamento della registrazione

Network Monitor passa tutti i frame di un'acquisizione ai parser e quindi inizia a chiamare la funzione [**Deregister**](deregister.md) per tutti i protocolli identificati. Ogni DLL del parser deve implementare **una funzione Deregister** per ogni protocollo supportato dalla DLL del parser.

Ogni implementazione [**della funzione Deregister**](deregister.md) deve chiamare la [**funzione DestroyProtocolDatabase**](destroypropertydatabase.md) per rilasciare le risorse usate per creare il database.

La procedura seguente identifica il passaggio necessario per implementare [**Deregister**](deregister.md).

**Per implementare l'annullamento della registrazione per un protocollo**

-   Chiamare [**DestroyProtocolDatabase per**](destroypropertydatabase.md) rilasciare le risorse del database.

Di seguito è riportata un'implementazione di base [**di Deregister.**](deregister.md) Si noti che nell'esempio di codice viene illustrata la versione delle risorse usate per creare un database delle proprietà.

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



