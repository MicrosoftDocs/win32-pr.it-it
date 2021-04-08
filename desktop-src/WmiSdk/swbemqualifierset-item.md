---
description: Il metodo Item dell'oggetto dell'SWbemQualifierSet restituisce un oggetto oggetto SWbemQualifier denominato dalla raccolta. Questo è il metodo predefinito di questo oggetto.
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: Metodo dell'SWbemQualifierSet. Item (wbemdisp. h)
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
ms.openlocfilehash: 9c89ff554b049e6730a64ebf7e5f017fc8a5652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885217"
---
# <a name="swbemqualifiersetitem-method"></a>Metodo dell'SWbemQualifierSet. Item

Il metodo **Item** dell'oggetto [**dell'SWbemQualifierSet**](swbemqualifierset.md) restituisce un oggetto [**oggetto SWbemQualifier**](swbemqualifier.md) denominato dalla raccolta. Questo è il metodo predefinito di questo oggetto.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strName* \[ in\]
</dt> <dd>

Obbligatorio. Nome del qualificatore da recuperare.

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Riservato. Il valore predefinito è 0 (zero).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'esito è positivo, viene restituito l'oggetto [**oggetto SWbemQualifier**](swbemqualifier.md) richiesto.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **Item** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Il parametro *iFlags* non è valido.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

Il qualificatore specificato non esiste.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_Dell'SWBEMQUALIFIERSET CLSID<br/>                                                     |
| IID<br/>                      | \_ISWBEMQUALIFIERSET IID<br/>                                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Dell'SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**Oggetto SWbemQualifier**](swbemqualifier.md)
</dt> </dl>

 

 




