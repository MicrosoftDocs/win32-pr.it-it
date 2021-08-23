---
description: Il metodo DeleteAll dell'oggetto SWbemNamedValueSet rimuove tutti i valori denominati dalla raccolta, svuotando così il valore.
ms.assetid: db5d2e68-028e-4902-ad42-0b46e1a96bcb
ms.tgt_platform: multiple
title: Metodo SWbemNamedValueSet.DeleteAll (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b6878494c31823b1c081a69b4d58b3a802cf820dd10bbcb20f14ed7087bb84c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612071"
---
# <a name="swbemnamedvaluesetdeleteall-method"></a>Metodo SWbemNamedValueSet.DeleteAll

Il **metodo DeleteAll** dell'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) rimuove tutti i valori denominati dalla raccolta, svuotando così il valore.

## <a name="syntax"></a>Sintassi


```VB
SWbemNamedValueSet.DeleteAll()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **DeleteAll,** **l'oggetto Err** può contenere il codice di errore seguente.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | IID \_ ISWbemNamedValueSet<br/>                                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> <dt>

[**SWbemNamedValueSet.Remove**](swbemnamedvalueset-remove.md)
</dt> </dl>

 

 




