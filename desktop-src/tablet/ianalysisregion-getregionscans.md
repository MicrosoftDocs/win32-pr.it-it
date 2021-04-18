---
description: Recupera una matrice di rettangoli che definisce l'area di IAnalysisRegion.
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: 'Metodo IAnalysisRegion:: GetRegionScans (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetRegionScans
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6cb8db60b5818f5bc2bc38892912e9ec40af1eb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307467"
---
# <a name="ianalysisregiongetregionscans-method"></a>Metodo IAnalysisRegion:: GetRegionScans

Recupera una matrice di rettangoli che definisce l'area di [**IAnalysisRegion**](ianalysisregion.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulCount* \[ out\]
</dt> <dd>

Numero di rettangoli restituiti in *pRegionScans*.

</dd> <dt>

*pRegionScans* \[ out\]
</dt> <dd>

Puntatore a una matrice di rettangoli che definisce l'area di [**IAnalysisRegion**](ianalysisregion.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Se *pRegionScans* viene passato come **null**, il metodo **GetRegionScans** restituisce **S \_ OK** e viene restituito il numero di rettangoli in *pulCount*.

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *pRegionScans* quando le informazioni non sono più necessarie.

 

I limiti dei rettangoli si trovano in coordinate di spazio input penna.

L'Unione dei rettangoli restituiti rappresenta l'area di [**IAnalysisRegion**](ianalysisregion.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come ottenere i rettangoli che definiscono l'area di [**IAnalysisRegion**](ianalysisregion.md) `region` e come ottenere solo il numero di rettangoli.


```C++
// Get the count and the rectangles.
ULONG count = 0;
RECT* rects = 0;
region->GetRegionScans(&count, &rects);

// Use rects

::CoTaskMemFree(rects);

// GetRegionScans just gets the count and returns S_OK
ULONG number = 0;
region->GetRegionScans(&number, NULL); 
```



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

[**Metodo IAnalysisRegion:: GetBounds**](ianalysisregion-getbounds.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

