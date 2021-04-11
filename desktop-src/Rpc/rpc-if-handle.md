---
title: RPC_IF_HANDLE (rpcdce. h)
description: Il \_ tipo di dati RPC if \_ handle dichiara un handle di interfaccia.
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9590973d5ae1e82d89d6151e224b771d9f55ecc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964684"
---
# <a name="rpc_if_handle"></a>\_gestore RPC if \_

Il tipo di dati **RPC \_ if \_ handle** dichiara un handle di interfaccia.


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a>Commenti

La libreria di runtime RPC utilizza gli handle di interfaccia per accedere alla struttura dei dati di specifica dell'interfaccia. Il compilatore MIDL crea automaticamente una struttura di dati di specifica dell'interfaccia da ogni file IDL e crea una variabile globale di tipo RPC \_ se \_ handle per la specifica dell'interfaccia.

Il compilatore MIDL include un handle di interfaccia in ogni file di intestazione generato per l'interfaccia. Le funzioni che richiedono la specifica dell'interfaccia come parametro mostrano un tipo di dati di **RPC \_ if \_ handle**. Il formato di ogni nome dell'handle di interfaccia è il seguente:

-   *if-name* \_ ClientIfHandle (per il client)
-   *if-name* \_ ServerIfHandle (per il server)

La parte *if-name* specifica l'identificatore di interfaccia nel file IDL.

Ad esempio:

Hello \_ ClientIfHandle

Hello \_ ServerIfHandle

> [!Note]  
> La lunghezza massima del nome dell'handle dell'interfaccia è 31 caratteri.

 

Poiché le \_ parti "ClientIfHandle" e " \_ ServerIfHandle" dei nomi richiedono 15 caratteri, la lunghezza dell'elemento *if-name* non può superare i 16 caratteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Rpcdce. h (include RPC. h)</dt> </dl> |



 

 





