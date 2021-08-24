---
description: Il metodo Item dell'oggetto SWbemMethodSet restituisce un oggetto SWbemMethod denominato dalla raccolta .
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: Metodo SWbemMethodSet.Item (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet.Item
- ISWbemMethodSet.Item
- ISWbemMethodSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fd78277be4611507a7f7a488dae0d4edda832afeac8c4a947d4c56277d9af397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679451"
---
# <a name="swbemmethodsetitem-method"></a>Metodo SWbemMethodSet.Item

Il **metodo Item** dell'oggetto [**SWbemMethodSet**](swbemmethodset.md) restituisce un [**oggetto SWbemMethod**](swbemmethod.md) denominato dalla raccolta .

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strName* \[ Pollici\]
</dt> <dd>

Obbligatorio. Nome del metodo da recuperare.

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Riservato. Il valore predefinito è 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, viene [**restituito l'oggetto SWbemMethod**](swbemmethod.md) richiesto.

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **Item,** **l'oggetto Err** può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

Il *parametro iFlags* non è valido.

</dd> <dt>

**wbemErrFailed** - 2147749894
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrNotFound** - 2147749890 (0x80041002)
</dt> <dd>

Il metodo specificato non esiste.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethodSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemMethodSet<br/>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemMethodSet**](swbemmethodset.md)
</dt> <dt>

[**SWbemMethod**](swbemmethod.md)
</dt> </dl>

 

 




