---
description: Recupera il tipo del tratto specificato.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: Metodo IInkAnalyzer::GetStrokeType (IACom.h)
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
ms.openlocfilehash: 71bf3775be1c21e59cf41a51fa5a6140e86e44ac81a2863892c1f252666e0f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092141"
---
# <a name="iinkanalyzergetstroketype-method"></a>Metodo IInkAnalyzer::GetStrokeType

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

*lStrokeId* \[ Pollici\]
</dt> <dd>

Identificatore del tratto.

</dd> <dt>

*pStrokeType* \[ Cambio\]
</dt> <dd>

Classificazione del tratto specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Se il tipo del tratto è il [**valore StrokeType StrokeType**](stroketype.md) \_ Unclassified, [**IInkAnalyzer**](iinkanalyzer.md) classifica il tratto durante l'analisi dell'input penna. In caso contrario, **IInkAnalyzer** usa il tipo impostato sul tratto.

[**IInkAnalyzer**](iinkanalyzer.md) non imposta il valore del tipo di tratto come parte dell'analisi dell'input penna. Per specificare o modificare il tipo di tratto, usare il metodo [**IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md) o il metodo [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




