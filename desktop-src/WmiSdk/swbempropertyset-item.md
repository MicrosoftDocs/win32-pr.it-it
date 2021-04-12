---
description: Il metodo Item dell'oggetto SWbemPropertySet ottiene un SWbemProperty denominato dalla raccolta. Questo è il metodo predefinito per questo oggetto.
ms.assetid: 72025676-01dd-4fd7-b000-de6b09ecc6dc
ms.tgt_platform: multiple
title: Metodo SWbemPropertySet. Item (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Item
- ISWbemPropertySet.Item
- ISWbemPropertySet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d4dcbbbcb8b5225af038bf71e67c3a14260942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233796"
---
# <a name="swbempropertysetitem-method"></a>Metodo SWbemPropertySet. Item

Il metodo **Item** dell'oggetto [**SWbemPropertySet**](swbempropertyset.md) ottiene un [**SWbemProperty**](swbemproperty.md) denominato dalla raccolta. Questo è il metodo predefinito per questo oggetto.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objProperty = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strName* \[ in\]
</dt> <dd>

Obbligatorio. Nome della proprietà da recuperare.

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Riservato. Se specificato, questo valore deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'esito è positivo, viene restituito l'oggetto [**SWbemProperty**](swbemproperty.md) richiesto.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **Item** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749896
</dt> <dd>

Memoria insufficiente per l'esecuzione di questo metodo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTYSET CLSID<br/>                                                      |
| IID<br/>                      | \_ISWBEMPROPERTYSET IID<br/>                                                       |



 

 




