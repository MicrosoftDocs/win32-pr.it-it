---
description: Network Monitor passa tutti i frame di un'acquisizione ai parser, quindi inizia a chiamare la funzione di annullamento della registrazione per tutti i protocolli identificati. Ogni DLL del parser deve implementare una funzione di annullamento della registrazione per ogni protocollo supportato dalla DLL del parser.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Implementazione della deregistrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee07c5b6b3c746e9c29811332b9e7674e49db26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306560"
---
# <a name="implementing-deregister"></a>Implementazione della deregistrazione

Network Monitor passa tutti i frame di un'acquisizione ai parser, quindi inizia a chiamare la funzione di [**annullamento della registrazione**](deregister.md) per tutti i protocolli identificati. Ogni DLL del parser deve implementare una funzione di **annullamento della registrazione** per ogni protocollo supportato dalla dll del parser.

Ogni implementazione della funzione [**deregister**](deregister.md) deve chiamare la funzione [**DestroyProtocolDatabase**](destroypropertydatabase.md) per rilasciare le risorse utilizzate per creare il database.

Nella procedura seguente viene identificato il passaggio necessario per implementare la [**Deregistrazione**](deregister.md).

**Per implementare la deregistrazione per un protocollo**

-   Chiamare [**DestroyProtocolDatabase**](destroypropertydatabase.md) per rilasciare le risorse di database.

Di seguito è riportata un'implementazione di base di [**deregister**](deregister.md). Si noti che nell'esempio di codice viene illustrata la versione delle risorse utilizzate per la creazione di un database di proprietà.

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



