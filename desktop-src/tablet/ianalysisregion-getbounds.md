---
description: Ottiene il rettangolo di delimitazione dell'area IAnalysis.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: Metodo IAnalysisRegion::GetBounds (IACom.h)
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
ms.openlocfilehash: 8481ddda9d0d278d2f24873a0c7d8a993c924c816d58153c38de8ef1063e986b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092332"
---
# <a name="ianalysisregiongetbounds-method"></a>Metodo IAnalysisRegion::GetBounds

Ottiene il rettangolo di delimitazione di [**IAnalysisRegion.**](ianalysisregion.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBoundingRectangle* \[ Cambio\]
</dt> <dd>

Rettangolo di delimitazione [**dell'area IAnalysis nelle**](ianalysisregion.md) coordinate dello spazio input penna.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

I limiti sono in coordinate dello spazio input penna.

Se [**IAnalysisRegion**](ianalysisregion.md) rappresenta un'area infinita, i limiti sinistro e superiore sono **INT \_ MIN** e i limiti destro e inferiore sono **INT \_ MAX.**

Se [**IAnalysisRegion rappresenta**](ianalysisregion.md) un'area vuota, tutti i limiti del rettangolo sono 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Area IAnalysis**](ianalysisregion.md)
</dt> <dt>

[**Metodo IAnalysisRegion::GetRegionScans**](ianalysisregion-getregionscans.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




