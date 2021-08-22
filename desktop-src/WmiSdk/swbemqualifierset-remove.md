---
description: Il metodo Remove dell'oggetto SWbemQualifierSet elimina un qualificatore denominato dalla raccolta.
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.tgt_platform: multiple
title: Metodo SWbemQualifierSet.Remove (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f4ca62276e39822964d33b58345b4718354bfd63039ec42ab30ac5daf95f6e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463611"
---
# <a name="swbemqualifiersetremove-method"></a>Metodo SWbemQualifierSet.Remove

Il **metodo Remove** dell'oggetto [**SWbemQualifierSet**](swbemqualifierset.md) elimina un qualificatore denominato dalla raccolta.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemQualifierSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strName* \[ Pollici\]
</dt> <dd>

Obbligatorio. Nome del qualificatore da rimuovere.

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Riservato. Il valore predefinito è 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento **del metodo Remove,** l'oggetto **Err** può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

Il *parametro iFlags* non è valido.

</dd> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrNotFound** - 2147749890 (0x80041002)
</dt> <dd>

Il qualificatore specificato non esiste.

</dd> <dt>

**wbemErrInvalidOperation** - 2147749910 (0x80041016)
</dt> <dd>

La rimozione di questo qualificatore non è valida.

</dd> </dl>

## <a name="remarks"></a>Commenti

Non è possibile eseguire l'iterazione di una raccolta durante la rimozione di elementi perché quando si rimuove un elemento da una raccolta, il puntatore alla raccolta viene spostato all'elemento successivo. Per altre informazioni, vedere [Accesso a una raccolta](accessing-a-collection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemQualifierSet<br/>                                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifierSet.Add**](swbemqualifierset-add.md)
</dt> </dl>

 

 




