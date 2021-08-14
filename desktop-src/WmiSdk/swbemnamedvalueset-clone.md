---
description: Il metodo Clone dell'oggetto SWbemNamedValueSet restituisce un nuovo oggetto che è un clone della raccolta corrente.
ms.assetid: 0e7fab2e-8175-45e5-aa70-1109502e2b3f
ms.tgt_platform: multiple
title: Metodo SWbemNamedValueSet.Clone (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9158901a39fa80e49404912ee5458c416069bbe354e19059ef4622ae4257fda9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314192"
---
# <a name="swbemnamedvaluesetclone-method"></a>Metodo SWbemNamedValueSet.Clone

Il **metodo Clone** dell'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) restituisce un nuovo oggetto che è un clone della raccolta corrente.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objwbemNamedValueSet = .Clone( _
)
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, viene [**restituito un nuovo oggetto SWbemNamedValueSet.**](swbemnamedvalueset.md)

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **Clone,** **l'oggetto Err** può contenere uno dei codici di errore seguenti.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per clonare l'oggetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare questo metodo per duplicare [**una raccolta SWbemNamedValueSet.**](swbemnamedvalueset.md)

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

 

 




