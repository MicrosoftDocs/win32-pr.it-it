---
title: RPC_IF_HANDLE (Rpcdce.h)
description: Il tipo \_ di dati RPC IF HANDLE dichiara un handle di \_ interfaccia.
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4652fbd08c583ad0a33638e52face9569e6ff701cb6dc2b775c7060134b60437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926440"
---
# <a name="rpc_if_handle"></a>RPC \_ IF \_ HANDLE

Il **tipo di dati RPC IF \_ \_ HANDLE** dichiara un handle di interfaccia.


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a>Commenti

La libreria di runtime RPC usa handle di interfaccia per accedere alla struttura dei dati di specifica dell'interfaccia. Il compilatore MIDL crea automaticamente una struttura di dati di specifica dell'interfaccia da ogni file IDL e crea una variabile globale di tipo RPC IF HANDLE per \_ \_ la specifica dell'interfaccia.

Il compilatore MIDL include un handle di interfaccia in ogni file di intestazione generato per l'interfaccia. Le funzioni che richiedono la specifica dell'interfaccia come parametro mostrano un tipo di dati **RPC \_ IF \_ HANDLE**. Il formato di ogni nome di handle di interfaccia è il seguente:

-   *if-name* \_ ClientIfHandle (per il client)
-   *if-name* \_ ServerIfHandle (per il server)

La *parte if-name* specifica l'identificatore di interfaccia nel file IDL.

Esempio:

hello \_ ClientIfHandle

hello \_ ServerIfHandle

> [!Note]  
> La lunghezza massima del nome dell'handle di interfaccia è di 31 caratteri.

 

Poiché le \_ parti "ClientIfHandle" e "ServerIfHandle" dei nomi richiedono 15 caratteri, l'elemento if-name non può contenere più di \_ 16 caratteri. 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Rpcdce.h (includere Rpc.h)</dt> </dl> |



 

 





