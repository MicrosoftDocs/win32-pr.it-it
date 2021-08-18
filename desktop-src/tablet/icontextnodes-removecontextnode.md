---
description: Rimuove un oggetto IContextNode da questa raccolta.
ms.assetid: ddda506d-4e39-486d-ac7d-211dc7869a73
title: Metodo IContextNodes::RemoveContextNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.RemoveContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8fa1fd222e671dfd87f15862108ea66df3b99e530d453cf4614b7572d31b275c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092302"
---
# <a name="icontextnodesremovecontextnode-method"></a>Metodo IContextNodes::RemoveContextNode

Rimuove un [**oggetto IContextNode**](icontextnode.md) da questa raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContextNode* \[ Pollici\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) da rimuovere.

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

 

 




