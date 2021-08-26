---
description: Il metodo Add dell'oggetto SWbemQualifierSet aggiunge un oggetto SWbemQualifier alla raccolta SWbemQualifierSet. Se nella raccolta esiste già un qualificatore con lo stesso nome, viene sostituito.
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: Metodo SWbemQualifierSet.Add (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Add
- ISWbemQualifierSet.Add
- ISWbemQualifierSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 64a85e10614595d9dd6492d3f4b412f1d89432c0188801ea60a09e294846297b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897781"
---
# <a name="swbemqualifiersetadd-method"></a>Metodo SWbemQualifierSet.Add

Il **metodo Add** dell'oggetto [**SWbemQualifierSet**](swbemqualifierset.md) aggiunge un [**oggetto SWbemQualifier**](swbemqualifier.md) alla **raccolta SWbemQualifierSet.** Se nella raccolta esiste già un qualificatore con lo stesso nome, viene sostituito.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objQualifier = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal bPropagatesToSubclasses ], _
  [ ByVal bPropagatesToInstances ], _
  [ ByVal bOverridable ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strName* \[ Pollici\]
</dt> <dd>

Obbligatorio. Nome del nuovo qualificatore.

</dd> <dt>

*varVal* \[ Pollici\]
</dt> <dd>

Obbligatorio. Valore Variant del nuovo qualificatore.

</dd> <dt>

*bPropagatesToSubclasses* \[ in, facoltativo\]
</dt> <dd>

Valore booleano che indica se questo nuovo qualificatore viene propagato alle sottoclassi. Il valore predefinito è **TRUE.**

</dd> <dt>

*bPropagatesToInstances* \[ in, facoltativo\]
</dt> <dd>

Valore booleano che indica se questo nuovo qualificatore viene propagato alle istanze. Il valore predefinito è **TRUE.**

</dd> <dt>

*bOverridable* \[ in, facoltativo\]
</dt> <dd>

Valore booleano che indica se è possibile eseguire l'override di questo qualificatore quando viene propagato. Il valore predefinito è **TRUE.**

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Riservato. Il valore predefinito è 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questo metodo restituisce un [**oggetto SWbemQualifier**](swbemqualifier.md) che rappresenta il nuovo qualificatore. In caso contrario, **viene restituito** un oggetto Null.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo Add,** l'oggetto **Err** può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

Il *parametro iFlags* non è valido.

</dd> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrCannotBeKey** - 2147749919 (0x8004101F)
</dt> <dd>

Tentativo non valido di specificare un **qualificatore key** in una proprietà che non può essere una chiave. Le chiavi sono specificate nella definizione della classe per un oggetto e non possono essere alterate per singole istanze.

</dd> <dt>

**wbemErrInvalidQualifierType** - 2147749929 (0x80041029)
</dt> <dd>

Il *parametro varVal* non è di un tipo di qualificatore valido.

</dd> <dt>

**wbemErrOverrideNotAllowed** - 2147749914 (0x8004101A)
</dt> <dd>

Non è possibile eseguire **l'operazione SWbemQualifierSet.Add** su questo qualificatore perché l'oggetto proprietario non consente override.

</dd> </dl>

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

[**SWbemQualifierSet.Remove**](swbemqualifierset-remove.md)
</dt> </dl>

 

 




