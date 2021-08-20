---
description: Recupera una matrice di rettangoli che definisce l'area di IAnalysisRegion.
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: Metodo IAnalysisRegion::GetRegionScans (IACom.h)
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
ms.openlocfilehash: e197126a99023fb96c2798343b391d53de4f6cd97aaaa141918f0fe705e5ad1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045318"
---
# <a name="ianalysisregiongetregionscans-method"></a>Metodo IAnalysisRegion::GetRegionScans

Recupera una matrice di rettangoli che definisce l'area di [**IAnalysisRegion.**](ianalysisregion.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulCount* \[ Cambio\]
</dt> <dd>

Numero di rettangoli restituiti in *pRegionScans.*

</dd> <dt>

*pRegionScans* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di rettangoli che definisce l'area di [**IAnalysisRegion.**](ianalysisregion.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Se *pRegionScans viene* passato come **NULL,** il **metodo GetRegionScans** restituisce **S \_ OK** e il numero di rettangoli viene restituito in *pulCount*.

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *pRegionScans* quando non sono più necessarie le informazioni.

 

I limiti dei rettangoli sono in coordinate dello spazio input penna.

L'unione dei rettangoli restituiti rappresenta l'area di [**IAnalysisRegion.**](ianalysisregion.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come ottenere i rettangoli che definiscono l'area di [**IAnalysisRegion**](ianalysisregion.md)e come ottenere solo il `region` numero di rettangoli.


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
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Area IAnalysis**](ianalysisregion.md)
</dt> <dt>

[**Metodo IAnalysisRegion::GetBounds**](ianalysisregion-getbounds.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

