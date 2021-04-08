---
title: RPC_MGR_EPV (rpcdce. h)
description: Il tipo di dati RPC \_ Mgr \_ EPV definisce un vettore del punto di ingresso di gestione.
ms.assetid: 396e76de-065f-471e-ade9-34770b16a958
keywords:
- RPC RPC_MGR_EPV
topic_type:
- apiref
api_name:
- RPC_MGR_EPV
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549ca4b5245b12bda07b46407041a01175955693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740215"
---
# <a name="rpc_mgr_epv"></a>EPV di gestione RPC \_ \_

Il tipo di dati **RPC \_ Mgr \_ EPV** definisce un vettore del punto di ingresso di gestione.

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a>Membri

<dl> <dt>

<span id="if-name"></span><span id="IF-NAME"></span>**If-name**
</dt> <dd>

Specifica il nome dell'interfaccia

</dd> <dt>

<span id="return-type"></span><span id="RETURN-TYPE"></span>**tipo restituito**
</dt> <dd>

Specifica il tipo restituito dalla funzione **FunctionName** indicata nel file IDL.

</dd> <dt>

<span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**FunctionName**
</dt> <dd>

Specifica il nome della funzione indicata nel file IDL.

</dd> <dt>

<span id="param-list"></span><span id="PARAM-LIST"></span>**param-list**
</dt> <dd>

Specifica i parametri indicati per la funzione **FunctionName** nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il vettore del punto di ingresso di gestione (EPV) è una matrice di puntatori a funzione. La matrice contiene i puntatori alle implementazioni delle funzioni specificate nel file IDL. Il numero di elementi nella matrice è impostato sul numero di funzioni specificate nel file IDL. Un'applicazione può avere anche più EPV, che rappresentano più implementazioni delle funzioni specificate nell'interfaccia.

Il compilatore MIDL genera un tipo di dati **EPV** predefinito denominato * if-name ***\_ server \_ EPV**, dove *if-name* specifica l'identificatore di interfaccia nel file IDL. Il compilatore MIDL Inizializza questo **EPV** predefinito in modo che contenga i puntatori a funzione per ogni routine specificata nel file IDL.

Quando il server offre più implementazioni della stessa interfaccia, l'applicazione server deve dichiarare e inizializzare una variabile di tipo *if-name * * * \_ server \_ EPV** per ogni implementazione dell'interfaccia. Ogni **EPV** deve contenere un punto di ingresso (puntatore a funzione) per ogni procedura definita nel file IDL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Rpcdce. h (include RPC. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





