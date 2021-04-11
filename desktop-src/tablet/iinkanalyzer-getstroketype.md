---
description: Recupera il tipo del tratto specificato.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: 'Metodo IInkAnalyzer:: GetStrokeType (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9358b2583f31fd26310ea880470f36404021fec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226153"
---
# <a name="iinkanalyzergetstroketype-method"></a>Metodo IInkAnalyzer:: GetStrokeType

Recupera il tipo del tratto specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStrokeType(
  [in]  LONG       lStrokeId,
  [out] StrokeType *pStrokeType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lStrokeId* \[ in\]
</dt> <dd>

Identificatore del tratto.

</dd> <dt>

*pStrokeType* \[ out\]
</dt> <dd>

Classificazione del tratto specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Se il tipo del tratto è il valore [**StrokeType**](stroketype.md) StrokeType \_ unclassifiedd, [**IInkAnalyzer**](iinkanalyzer.md) classifica il tratto durante l'analisi dell'input penna. In caso contrario, **IInkAnalyzer** usa il tipo impostato sul tratto.

[**IInkAnalyzer**](iinkanalyzer.md) non imposta il valore del tipo di tratto come parte dell'analisi dell'input penna. Per specificare o modificare il tipo di tratto, usare il metodo [**IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) o [**IInkAnalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md).

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

[**Metodo IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




