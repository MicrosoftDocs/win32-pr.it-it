---
description: Indica se la stringa riconosciuta specificata deriva dal dizionario di sistema, dal dizionario utente o dall'elenco di parole.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: Metodo IContextNode::IsAlternateStringSupported (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsAlternateStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cbf18c63ce81a439092ba3bdabfae38c5f52882ec5364ef5c8fbd67cab5d81a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119266301"
---
# <a name="icontextnodeisalternatestringsupported-method"></a>Metodo IContextNode::IsAlternateStringSupported

Indica se la stringa riconosciuta specificata deriva dal dizionario di sistema, dal dizionario utente o dall'elenco di parole. Tutti i dati di limitazione, ad esempio elenchi di parole, guide o factoid, in qualsiasi nodo dei suggerimenti corrispondente verranno usati per determinare se la stringa è supportata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrAlternateString* \[ Pollici\]
</dt> <dd>

Stringa riconosciuta da verificare.

</dd> <dt>

*pfIsSupported* \[ Cambio\]
</dt> <dd>

**VARIANT \_ TRUE** se la stringa specificata è supportata da [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) con tutti i nodi hint corrispondenti applicati; **VARIANT \_ FALSE se** non è supportato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Osservazioni

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

 

 




