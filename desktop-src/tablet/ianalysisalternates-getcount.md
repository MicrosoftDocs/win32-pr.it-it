---
description: Recupera il numero di oggetti IAnalysisAlternate contenuti nella raccolta IAnalysisAlternates.
ms.assetid: 17b71b5a-638a-4e6e-a43b-4ca3c8eba257
title: Metodo IAnalysisAlternates::GetCount (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84ff5941d4db6ca569c8a7a10a622e4b3dcdfc947284064fa009e030adae1493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967490"
---
# <a name="ianalysisalternatesgetcount-method"></a>Metodo IAnalysisAlternates::GetCount

Recupera il numero di [**oggetti IAnalysisAlternate**](ianalysisalternate.md) contenuti nella raccolta [**IAnalysisAlternates.**](ianalysisalternates.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulCount* \[ Cambio\]
</dt> <dd>

Intero senza segno a 32 bit impostato sul numero di oggetti [**IAnalysisAlternate**](ianalysisalternate.md) contenuti nella raccolta [**IAnalysisAlternates.**](ianalysisalternates.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




