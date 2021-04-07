---
description: Il \_ Metodo Clone dell'oggetto SWbemObject restituisce un nuovo oggetto che è un clone dell'oggetto corrente.
ms.assetid: d0773c94-30b5-4217-8a9a-0bceb9e75f02
ms.tgt_platform: multiple
title: Metodo SWbemObject.Clone_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Clone_
- ISWbemObject.Clone_
- ISWbemObject.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84ca02bf749fd69db01ca7925b554c4eb0d95c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058096"
---
# <a name="swbemobjectclone_-method"></a>Metodo SWbemObject. Clone \_

Il **metodo \_ Clone** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce un nuovo oggetto che è un clone dell'oggetto corrente.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questo metodo restituisce un nuovo oggetto [**SWbemObject**](swbemobject.md) .

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo \_ Clone** , l'oggetto **Err** può contenere uno dei codici di errore riportati di seguito.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Non è stato specificato **alcun** elemento come parametro e non è accettabile in questo utilizzo.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per clonare l'oggetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare il **metodo \_ Clone** per duplicare una definizione di classe o un'istanza di. Questa operazione è utile quando è necessaria la copia originale dell'oggetto a scopo di backup mentre si modifica una nuova copia. Analogamente, utilizzare questo metodo per creare numerose nuove istanze di da un'unica istanza di origine. Utilizzare, ad esempio, [**SWbemObject. \_ SpawnInstance**](swbemobject-spawninstance-.md) per creare una singola istanza iniziale e utilizzare **SWbemObject. Clone \_** per produrre rapidamente 100 copie dell'istanza. Successivamente, è possibile modificare gli oggetti, assegnando a ognuno valori specifici.

Non è possibile usare questo metodo per convertire una definizione di classe in un'istanza o per convertire un'istanza in una definizione di classe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



 

 




