---
description: Usare il \_ Metodo SpawnDerivedClass dell'oggetto SWbemObject per creare un oggetto classe derivata dall'oggetto corrente. L'oggetto deve essere una definizione di classe che diventa la classe padre dell'oggetto generato.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: Metodo SWbemObject.SpawnDerivedClass_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b26e1d894e5ccc0d0fcec9d7ac9ad0101d18c7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226814"
---
# <a name="swbemobjectspawnderivedclass_-method"></a>SWbemObject. SpawnDerivedClass, \_ Metodo

Usare il **metodo \_ SpawnDerivedClass** dell'oggetto [**SWbemObject**](swbemobject.md) per creare un oggetto classe derivata dall'oggetto corrente. L'oggetto deve essere una definizione di classe che diventa la classe padre dell'oggetto generato.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iFlags* \[ opzionale\]
</dt> <dd>

Riservato e deve essere 0 (zero) se specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la chiamata ha esito positivo, l'oggetto [**SWbemObject**](swbemobject.md) contiene il nuovo oggetto definizione di classe. Non viene restituito alcun oggetto quando si verifica un errore.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **SpawnDerivedClass \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrIllegalOperation** -2147749918 (0x8004101E)
</dt> <dd>

L'utente ha richiesto un'operazione non valida, ad esempio la generazione di una classe da un'istanza.

</dd> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020)
</dt> <dd>

La classe di origine non è stata completamente definita o è stata registrata con WMI, pertanto non è consentita una nuova classe derivata.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'oggetto restituito diventa automaticamente una sottoclasse dell'oggetto corrente. Non è possibile eseguire l'override di questo comportamento. Non esiste un altro metodo tramite il quale è possibile creare classi derivate.

Non è possibile creare una classe derivata da una classe locale per il proprio processo client. Prima di usare questo metodo per creare una classe derivata, è necessario creare la classe di base. Per creare la classe di base, chiamare [**SWbemObject. \_ put**](swbemobject-put-.md)e recuperare la classe di base utilizzando [**SWbemServices. Get**](swbemservices-get.md).

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



 

 




