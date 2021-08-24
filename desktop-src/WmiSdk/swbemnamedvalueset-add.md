---
description: Il metodo Add dell'oggetto SWbemNamedValueSet aggiunge un oggetto SWbemNamedValue alla raccolta. Se nella raccolta esiste già un elemento con lo stesso nome, il nuovo elemento lo sostituisce.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: Metodo SWbemNamedValueSet.Add (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a7a911dcfa6371421fd4033524400d0c818e814d3bd52f90b677ac7c9fcf1b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612121"
---
# <a name="swbemnamedvaluesetadd-method"></a>Metodo SWbemNamedValueSet.Add

Il **metodo Add** dell'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) aggiunge un oggetto [**SWbemNamedValue**](swbemnamedvalue.md) alla raccolta. Se nella raccolta esiste già un elemento con lo stesso nome, il nuovo elemento lo sostituisce.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objNamedValue = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strName* \[ Pollici\]
</dt> <dd>

Obbligatorio. Nome del nuovo valore.

</dd> <dt>

*varVal* \[ Pollici\]
</dt> <dd>

Obbligatorio. Variante che rappresenta il nuovo valore.

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Se specificato, riservato e devono essere impostati su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questo metodo restituisce l'oggetto [**SWbemNamedValue**](swbemnamedvalue.md) appena modificato o appena creato.

## <a name="remarks"></a>Commenti

Per esempi di aggiunta e recupero di valori denominati, vedere [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).

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
</dt> </dl>

 

 




