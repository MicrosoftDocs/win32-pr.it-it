---
description: Indica se la stringa riconosciuta specificata proviene dal dizionario di sistema, dal dizionario utente o dall'elenco di parole.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: 'Metodo IContextNode:: IsAlternateStringSupported (IACom. h)'
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
ms.openlocfilehash: 93dfcdc59851aad3b06fb1451178e97b36ee0a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307425"
---
# <a name="icontextnodeisalternatestringsupported-method"></a>Metodo IContextNode:: IsAlternateStringSupported

Indica se la stringa riconosciuta specificata proviene dal dizionario di sistema, dal dizionario utente o dall'elenco di parole. Tutti i dati di restrizione, ad esempio liste, guide o factoids, in qualsiasi nodo hint corrispondente verranno usati per determinare se la stringa è supportata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrAlternateString* \[ in\]
</dt> <dd>

Stringa riconosciuta da verificare.

</dd> <dt>

*pfIsSupported* \[ out\]
</dt> <dd>

**Variante \_ TRUE** se la stringa specificata è supportata da [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) con qualsiasi nodo hint corrispondente applicato; **Variante \_ FALSE** se non è supportato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> </dl>

 

 




