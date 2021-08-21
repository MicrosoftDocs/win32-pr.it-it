---
description: Usare il metodo SpawnDerivedClass dell'oggetto SWbemObject per creare un oggetto classe derivata \_ dall'oggetto corrente. L'oggetto deve essere una definizione di classe che diventa la classe padre dell'oggetto generato.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: SWbemObject.SpawnDerivedClass_ metodo (Wbemdisp.h)
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
ms.openlocfilehash: 0ed0a01926c76ecfc4d393a4de8225d7d0c98a9904f113aed18cd1cb5f8ccabb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313795"
---
# <a name="swbemobjectspawnderivedclass_-method"></a>Metodo SWbemObject.SpawnDerivedClass \_

Usare il **metodo SpawnDerivedClass \_** dell'oggetto [**SWbemObject**](swbemobject.md) per creare un oggetto classe derivata dall'oggetto corrente. L'oggetto deve essere una definizione di classe che diventa la classe padre dell'oggetto generato.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iFlags* \[ Opzionale\]
</dt> <dd>

Riservato e deve essere 0 (zero) se specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la chiamata ha esito positivo, [**l'oggetto SWbemObject**](swbemobject.md) contiene il nuovo oggetto definizione di classe. Non viene restituito alcun oggetto in caso di errore.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo \_ SpawnDerivedClass,** l'oggetto **Err** può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrIllegalOperation** - 2147749918 (0x8004101E)
</dt> <dd>

L'utente ha richiesto un'operazione non valida, ad esempio la generazione di una classe da un'istanza di .

</dd> <dt>

**wbemErrIncompleteClass** - 2147749920 (0x80041020)
</dt> <dd>

La classe di origine non è stata completamente definita o registrata con WMI, pertanto non è consentita una nuova classe derivata.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'oggetto restituito diventa automaticamente una sottoclasse dell'oggetto corrente. Questo comportamento non può essere sottoposto a override. Non esiste alcun altro metodo con cui è possibile creare classi derivate.

Non è possibile creare una classe derivata da una classe locale rispetto al proprio processo client. Prima di usare questo metodo per creare una classe derivata, è necessario creare la classe di base. Per creare la classe di base, chiamare [**SWbemObject.Put \_**](swbemobject-put-.md)e recuperare la classe di base usando [**SWbemServices.Get**](swbemservices-get.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




