---
description: Modifica il tipo del tratto specificato.
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: Metodo IInkAnalyzer::SetStrokeType (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6d65c01ba3618bad563ee2b8c8a9c4fee3479a12c796b2f2f570832fac1d826c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709031"
---
# <a name="iinkanalyzersetstroketype-method"></a>Metodo IInkAnalyzer::SetStrokeType

Modifica il tipo del tratto specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetStrokeType(
  [in] LONG       lStrokeId,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lStrokeId* \[ Pollici\]
</dt> <dd>

Identificatore del tratto a cui assegnare *StrokeType.*

</dd> <dt>

*Tipo di tratto* \[ Pollici\]
</dt> <dd>

Valore [**StrokeType**](stroketype.md) da assegnare al tratto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Se il tipo del tratto è il valore [**StrokeType StrokeType**](stroketype.md) **\_ Unclassified,** [**IInkAnalyzer**](iinkanalyzer.md) classifica il tratto durante l'analisi dell'input penna. In caso contrario, **IInkAnalyzer** usa il tipo impostato sul tratto.

[**IInkAnalyzer**](iinkanalyzer.md) non imposta il valore del tipo di tratto come parte dell'analisi dell'input penna. Per specificare o modificare il tipo di tratto, usare il metodo **IInkAnalyzer::SetStrokeType** o il metodo [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md).

Se un tratto è associato a un [**oggetto IContextNode**](icontextnode.md) che non è un nodo input penna non classificato (vedere [**IContextNode::GetType),**](icontextnode-gettype.md)questo metodo sposta il tratto in un nodo input penna non classificato che contiene tratti della stessa lingua. Se tale nodo di contesto non esiste, questo metodo crea un nuovo nodo input penna non classificato e vi aggiunge il tratto. Un nodo input penna non classificato è **un elemento IContextNode** di tipo UnclassifiedInk.

Se questo metodo sposta un tratto da un [**oggetto IContextNode**](icontextnode.md) che non è un nodo input penna non classificato, questo metodo aggiunge anche il rettangolo di selezione del tratto all'area dirty dell'analizzatore input penna (vedere [**Metodo IInkAnalyzer::GetDirtyRegion).**](iinkanalyzer-getdirtyregion.md)

Questo metodo non sposta un tratto se il *parametro StrokeType* corrisponde al tipo corrente del tratto.

L'impostazione del tipo di tratto sui tratti associati a un ContextNode con NodeTypeAndProperties confermato genererà un'eccezione InvalidOperationException.

Se il tratto specificato non è associato a [**IInkAnalyzer,**](iinkanalyzer.md)questo metodo restituisce senza aggiornare **LInkAnalyzer.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetStrokeType**](iinkanalyzer-getstroketype.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




