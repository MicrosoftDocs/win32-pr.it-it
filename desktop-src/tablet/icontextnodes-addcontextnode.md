---
description: Aggiunge un oggetto IContextNode alla raccolta.
ms.assetid: 48feae05-1cc8-46c3-97cd-4493ee28b8e5
title: 'Metodo IContextNodes:: AddContextNode (IACom. h)'
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
ms.openlocfilehash: 18a7438c09fb2a850637bbae549ada61c37fb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129486"
---
# <a name="icontextnodesaddcontextnode-method"></a>Metodo IContextNodes:: AddContextNode

Aggiunge un oggetto [**IContextNode**](icontextnode.md) alla raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContextNode* \[ in\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




