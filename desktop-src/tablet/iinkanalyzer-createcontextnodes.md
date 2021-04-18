---
description: Crea un oggetto IContextNodes.
ms.assetid: d6d37595-307b-4cbc-9d48-ad10f8b272dd
title: 'Metodo IInkAnalyzer:: CreateContextNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07bdfc9a32fd4aec8e716cdd3c788c211c1adaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307394"
---
# <a name="iinkanalyzercreatecontextnodes-method"></a>Metodo IInkAnalyzer:: CreateContextNodes

Crea un oggetto [**IContextNodes**](icontextnodes.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateContextNodes(
  [out] IContextNodes **ppContextNodes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppContextNodes* \[ out\]
</dt> <dd>

Puntatore all'oggetto [**IContextNodes**](icontextnodes.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodes* quando non è più necessario utilizzare l'oggetto.

 

Utilizzare questo metodo per creare una raccolta [**IContextNodes**](icontextnodes.md) vuota associata a [**IInkAnalyzer**](iinkanalyzer.md). La nuova raccolta **IContextNodes** non fa parte dell'albero del contesto dell'oggetto **IInkAnalyzer** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

