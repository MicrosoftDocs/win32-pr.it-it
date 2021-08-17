---
description: Recupera una matrice di identificatori per i tratti all'interno dell'oggetto IContextNode.
ms.assetid: 2420afec-6859-449b-92d8-0f4327281852
title: Metodo IContextNode::GetStrokeIds (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ebe66d514b20fc558adce39c013cf559fbc63bb38f772bff73b0819c10426960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967371"
---
# <a name="icontextnodegetstrokeids-method"></a>Metodo IContextNode::GetStrokeIds

Recupera una matrice di identificatori per i tratti all'interno [**dell'oggetto IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

Numero di tratti. Il valore passato non viene utilizzato.

</dd> <dt>

*pplStrokes* \[ Cambio\]
</dt> <dd>

Puntatore alla matrice di identificatori di tratto per questo [**oggetto IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *pplStrokes* quando le informazioni non sono più necessarie.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetStrokeId**](icontextnode-getstrokeid.md)
</dt> <dt>

[**IContextNode::GetStrokeCount**](icontextnode-getstrokecount.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

