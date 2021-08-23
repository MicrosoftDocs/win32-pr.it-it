---
description: Il metodo Item dell'oggetto SWbemObjectSet ottiene un oggetto SWbemObject dalla raccolta.
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: Metodo SWbemObjectSet.Item (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Item
- ISWbemObjectSet.Item
- ISWbemObjectSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a0d357eda1098bd20e4ebc68f5b959b7ac5ffd4fb46788ffac99d1f18678d6a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857221"
---
# <a name="swbemobjectsetitem-method"></a>Metodo SWbemObjectSet.Item

Il **metodo Item** dell'oggetto [**SWbemObjectSet**](swbemobjectset.md) ottiene un [**oggetto SWbemObject**](swbemobject.md) dalla raccolta.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obbligatorio. Percorso relativo dell'oggetto da recuperare dalla raccolta. Esempio: Win32 \_ LogicalDisk="C:"

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, [**l'oggetto SWbemObject**](swbemobject.md) richiesto restituisce .

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **Item,** **l'oggetto Err** può contenere uno dei codici di errore seguenti.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> <dt>

**wbemErrNotFound** - 2147749890 (0x80041002)
</dt> <dd>

L'elemento richiesto non è stato trovato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **metodo Item** può richiedere molto tempo del processore perché l'enumerazione completa da parte del provider degli elementi del set è necessaria per restituire il risultato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



 

 




