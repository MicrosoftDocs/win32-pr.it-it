---
title: RPC_MGR_EPV (Rpcdce.h)
description: Il tipo di dati RPC \_ MGR \_ EPV definisce un vettore del punto di ingresso del gestore.
ms.assetid: 396e76de-065f-471e-ade9-34770b16a958
keywords:
- RPC_MGR_EPV RPC
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
ms.openlocfilehash: 55e40b883192adc53b11f9965f1a92f4637b320d32b5fd6909e2b6d615437a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926295"
---
# <a name="rpc_mgr_epv"></a>RPC \_ MGR \_ EPV

Il tipo di **dati RPC \_ MGR \_ EPV** definisce un vettore del punto di ingresso del gestore.

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a>Membri

<dl> <dt>

<span id="if-name"></span><span id="IF-NAME"></span>**if-name**
</dt> <dd>

Specifica il nome dell'interfaccia

</dd> <dt>

<span id="return-type"></span><span id="RETURN-TYPE"></span>**return-type**
</dt> <dd>

Specifica il tipo restituito dalla funzione **Functionname** indicata nel file IDL.

</dd> <dt>

<span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Functionname**
</dt> <dd>

Specifica il nome della funzione indicata nel file IDL.

</dd> <dt>

<span id="param-list"></span><span id="PARAM-LIST"></span>**param-list**
</dt> <dd>

Specifica i parametri indicati per la funzione **Functionname** nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il vettore del punto di ingresso di gestione è una matrice di puntatori a funzione. La matrice contiene puntatori alle implementazioni delle funzioni specificate nel file IDL. Il numero di elementi nella matrice è impostato sul numero di funzioni specificato nel file IDL. Un'applicazione può anche avere più EPV, che rappresentano più implementazioni delle funzioni specificate nell'interfaccia .

Il compilatore MIDL genera un tipo di dati **EPV** predefinito denominato *if-name***\_ SERVER \_ EPV,** dove *if-name* specifica l'identificatore di interfaccia nel file IDL. Il compilatore MIDL inizializza questo **valore EPV** predefinito in modo da contenere puntatori a funzione per ognuna delle procedure specificate nel file IDL.

Quando il server offre più implementazioni della stessa interfaccia, l'applicazione server deve dichiarare e inizializzare una variabile di tipo *if-name*** \_ SERVER \_ EPV** per ogni implementazione dell'interfaccia. Ogni **EPV** deve contenere un punto di ingresso (puntatore a funzione) per ogni routine definita nel file IDL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Rpcdce.h (includere Rpc.h)</dt> </dl> |



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

 

 





