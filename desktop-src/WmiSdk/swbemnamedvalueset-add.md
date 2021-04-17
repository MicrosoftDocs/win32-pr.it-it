---
description: Il metodo Add dell'oggetto SWbemNamedValueSet aggiunge un oggetto SWbemNamedValue alla raccolta. Se un elemento esiste già nella raccolta con lo stesso nome, il nuovo elemento lo sostituisce.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: Metodo SWbemNamedValueSet. Add (wbemdisp. h)
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
ms.openlocfilehash: 3aa1a3a982d7621c910a5afca95b26db1dd5f4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528482"
---
# <a name="swbemnamedvaluesetadd-method"></a>SWbemNamedValueSet. Add, metodo

Il metodo **Add** dell'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) aggiunge un oggetto [**SWbemNamedValue**](swbemnamedvalue.md) alla raccolta. Se un elemento esiste già nella raccolta con lo stesso nome, il nuovo elemento lo sostituisce.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

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

*strName* \[ in\]
</dt> <dd>

Obbligatorio. Nome del nuovo valore.

</dd> <dt>

*varVal* \[ in\]
</dt> <dd>

Obbligatorio. Variante che rappresenta il nuovo valore.

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Riservato e deve essere impostato su zero se specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questo metodo restituisce l'oggetto [**SWbemNamedValue**](swbemnamedvalue.md) appena modificato o appena creato.

## <a name="remarks"></a>Commenti

Per esempi relativi all'aggiunta e al recupero di valori denominati, vedere [**SWbemNamedValue. Value**](swbemnamedvalue-value.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMNAMEDVALUESET CLSID<br/>                                                    |
| IID<br/>                      | \_ISWBEMNAMEDVALUESET IID<br/>                                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> </dl>

 

 




