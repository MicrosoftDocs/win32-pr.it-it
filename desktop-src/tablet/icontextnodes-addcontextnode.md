---
description: Aggiunge un oggetto IContextNode a questa raccolta.
ms.assetid: 48feae05-1cc8-46c3-97cd-4493ee28b8e5
title: Metodo IContextNodes::AddContextNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.AddContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 81b054f805f746522b957de3e8003d471b37a14e8804635e97c6f1bef091f3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935341"
---
# <a name="icontextnodesaddcontextnode-method"></a>Metodo IContextNodes::AddContextNode

Aggiunge un [**oggetto IContextNode**](icontextnode.md) a questa raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContextNode* \[ Pollici\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




