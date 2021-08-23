---
description: Indica se la stringa riconosciuta di questo IContextNode deriva dal dizionario di sistema, dal dizionario utente o dall'elenco di parole.
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: Metodo IContextNode::IsStringSupported (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2eef383f059897665c013e3575d452564295ccd9bd014ae8084fd1635892bd99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709111"
---
# <a name="icontextnodeisstringsupported-method"></a>Metodo IContextNode::IsStringSupported

Indica se la stringa riconosciuta di [**questo IContextNode**](icontextnode.md) deriva dal dizionario di sistema, dal dizionario utente o dall'elenco di parole.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pfIsSupported* \[ out, retval\]
</dt> <dd>

**VARIANT \_ TRUE** se il valore stringa riconosciuto di [**questo IContextNode**](icontextnode.md) è supportato da [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) con tutti i nodi hint corrispondenti applicati; in caso contrario, **VARIANT \_ FALSE.**

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

[**IContextNode**](icontextnode.md)
</dt> </dl>

 

 




