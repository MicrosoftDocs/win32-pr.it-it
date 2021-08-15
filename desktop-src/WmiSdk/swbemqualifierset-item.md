---
description: Il metodo Item dell'oggetto SWbemQualifierSet restituisce un oggetto SWbemQualifier denominato dalla raccolta. Questo è il metodo predefinito di questo oggetto.
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: Metodo SWbemQualifierSet.Item (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Item
- ISWbemQualifierSet.Item
- ISWbemQualifierSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 99b735f52ac4d311af6e35f7e214322c55345e4c029e73a342baa52dfa72de6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312992"
---
# <a name="swbemqualifiersetitem-method"></a>Metodo SWbemQualifierSet.Item

Il **metodo Item** dell'oggetto [**SWbemQualifierSet**](swbemqualifierset.md) restituisce un oggetto [**SWbemQualifier**](swbemqualifier.md) denominato dalla raccolta. Questo è il metodo predefinito di questo oggetto.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strName* \[ Pollici\]
</dt> <dd>

Obbligatorio. Nome del qualificatore da recuperare.

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Riservato. Il valore predefinito è 0 (zero).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, viene restituito [**l'oggetto SWbemQualifier**](swbemqualifier.md) richiesto.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo Item,** l'oggetto **Err** può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

Il *parametro iFlags* non è valido.

</dd> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrNotFound** - 2147749890 (0x80041002)
</dt> <dd>

Il qualificatore specificato non esiste.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemQualifierSet<br/>                                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifier**](swbemqualifier.md)
</dt> </dl>

 

 




