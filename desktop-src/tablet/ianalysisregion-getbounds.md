---
description: Ottiene il rettangolo di delimitazione di IAnalysisRegion.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: 'Metodo IAnalysisRegion:: GetBounds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetBounds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 12bbb8163aa866648a83effc75d668bc4032c8d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751874"
---
# <a name="ianalysisregiongetbounds-method"></a>Metodo IAnalysisRegion:: GetBounds

Ottiene il rettangolo di delimitazione di [**IAnalysisRegion**](ianalysisregion.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBoundingRectangle* \[ out\]
</dt> <dd>

Rettangolo di delimitazione di [**IAnalysisRegion**](ianalysisregion.md) nelle coordinate dello spazio di input penna.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

I limiti si trovano nelle coordinate dello spazio input penna.

Se il [**IAnalysisRegion**](ianalysisregion.md) rappresenta un'area infinita, i limiti sinistro e superiore sono di **tipo int \_ min**, mentre i limiti destro e inferiore sono di **tipo int \_ Max**.

Se [**IAnalysisRegion**](ianalysisregion.md) rappresenta un'area vuota, tutti i limiti del rettangolo sono pari a 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**Metodo IAnalysisRegion:: GetRegionScans**](ianalysisregion-getregionscans.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




