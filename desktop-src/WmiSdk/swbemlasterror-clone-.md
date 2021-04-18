---
description: Il \_ Metodo Clone dell'oggetto SWbemLastError restituisce un nuovo oggetto che è un clone dell'oggetto SWbemLastError corrente.
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: Metodo SWbemLastError.Clone_ (wbemdisp. h)
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
ms.openlocfilehash: 7d4d43f73ab42021235db39adba0a77bc783b97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314568"
---
# <a name="swbemlasterrorclone_-method"></a>Metodo SWbemLastError. Clone \_

Il **metodo \_ Clone** dell'oggetto [**SWbemLastError**](swbemlasterror.md) restituisce un nuovo oggetto che è un clone dell'oggetto **SWbemLastError** corrente.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il **metodo \_ Clone** ha esito positivo, restituisce un nuovo oggetto [**SWbemLastError**](swbemlasterror.md) .

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **Clone \_** , l'oggetto **Err** può contenere uno dei codici di errore riportati di seguito.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Parametro specificato non valido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare il **metodo \_ Clone** per duplicare una definizione di classe o un'istanza di. Questo metodo è utile quando è necessario eseguire il backup della copia originale dell'oggetto durante la modifica di una nuova copia. Usare inoltre questo metodo per creare molte nuove istanze di da un'unica istanza di origine. Utilizzare, ad esempio, [**SWbemObject. \_ SpawnInstance**](swbemobject-spawninstance-.md) per creare una singola istanza iniziale e utilizzare **SWbemLastError. \_ Clone** per produrre rapidamente 100 copie dell'istanza. Successivamente, è possibile modificare gli oggetti, fornendo valori specifici per ogni oggetto.

Non è possibile utilizzare questo metodo per convertire una definizione di classe in un'istanza o per convertire un'istanza in una definizione di classe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMLASTERROR CLSID<br/>                                                        |
| IID<br/>                      | \_ISWBEMLASTERROR IID<br/>                                                         |



 

 




