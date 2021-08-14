---
description: Il metodo Clone dell'oggetto SWbemLastError restituisce un nuovo oggetto che è un \_ clone dell'oggetto SWbemLastError corrente.
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: SWbemLastError.Clone_ metodo (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Clone_
- ISWbemLastError.Clone_
- ISWbemLastError.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 162944eeb4ee7ca0c72102b704e9f75851bbfb41885e6b79e86d1a438487473f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314667"
---
# <a name="swbemlasterrorclone_-method"></a>Metodo SWbemLastError.Clone \_

Il **\_ metodo Clone** dell'oggetto [**SWbemLastError**](swbemlasterror.md) restituisce un nuovo oggetto che è un clone dell'oggetto **SWbemLastError** corrente.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il **metodo \_ Clone** ha esito positivo, restituisce un [**nuovo oggetto SWbemLastError.**](swbemlasterror.md)

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **Clone, \_** l'oggetto **Err** può contenere uno dei codici di errore seguenti.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

Un parametro specificato non è valido.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare il metodo **Clone \_** per duplicare una definizione di classe o un'istanza. Questo metodo è utile quando è necessario eseguire il backup della copia originale dell'oggetto mentre si modifica una nuova copia. Usare inoltre questo metodo per creare molte nuove istanze da una singola istanza di origine. Ad esempio, usare [**\_ SWbemObject.SpawnInstance**](swbemobject-spawninstance-.md) per creare una singola istanza iniziale e **usare SWbemLastError.Clone \_** per produrre rapidamente 100 copie dell'istanza. Successivamente, è possibile modificare gli oggetti, fornendo valori specifici a ogni oggetto.

Non è possibile usare questo metodo per convertire una definizione di classe in un'istanza di o per convertire un'istanza in una definizione di classe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



 

 




