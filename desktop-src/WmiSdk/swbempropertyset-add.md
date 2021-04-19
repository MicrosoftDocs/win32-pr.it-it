---
description: Il metodo Add dell'oggetto SWbemPropertySet aggiunge un oggetto SWbemProperty alla raccolta SWbemPropertySet. Se nella raccolta esiste già una proprietà con lo stesso nome, il relativo contenuto viene sostituito con la nuova definizione.
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: Metodo SWbemPropertySet. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Add
- ISWbemPropertySet.Add
- ISWbemPropertySet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ad5b40d31d162b287bdb1a387cd0602e0be1ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318172"
---
# <a name="swbempropertysetadd-method"></a>SWbemPropertySet. Add, metodo

Il metodo **Add** dell'oggetto [**SWbemPropertySet**](swbempropertyset.md) aggiunge un oggetto [**SWbemProperty**](swbemproperty.md) alla raccolta **SWbemPropertySet** . Se nella raccolta esiste già una proprietà con lo stesso nome, il relativo contenuto viene sostituito con la nuova definizione.

> [!Note]  
> Il valore della proprietà aggiunta è **null** (non assegnato) dopo questa operazione. Per impostare o modificare il valore di una proprietà WMI, è necessario impostare la proprietà [**value**](swbemdatetime-value.md) dell'oggetto [**SWbemProperty**](swbemproperty.md) restituito.

 

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objProperty = .Add( _
  ByVal strName, _
  ByVal iCIMType, _
  [ ByVal bIsArray ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strName* \[ in\]
</dt> <dd>

Obbligatorio. Nome della nuova proprietà.

</dd> <dt>

*iCIMType* \[ in\]
</dt> <dd>

Obbligatorio. Intero che rappresenta il qualificatore **CimType** della nuova proprietà. Vedere [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) per l'elenco con i qualificatori **CimType** e i relativi valori.

</dd> <dt>

*bIsArray* \[ in, facoltativo\]
</dt> <dd>

Specifica se la proprietà è un tipo di matrice. Il valore predefinito per questo parametro è **false**.

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Riservato e deve essere zero se specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questo metodo restituisce un oggetto [**SWbemProperty**](swbemproperty.md) che rappresenta la nuova proprietà. In caso contrario, viene restituito un oggetto **null** .

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **Add** , l'oggetto **Err** può contenere uno dei codici di errore riportati di seguito.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per l'esecuzione di questo metodo.

</dd> <dt>

**wbemErrInvalidPropertyType** -2147749930
</dt> <dd>

Qualificatore **CimType** non riconosciuto.

</dd> </dl>

## <a name="examples"></a>Esempio

Per un esempio di codice che usa questo metodo, vedere l'argomento [**SWbemPropertySet**](swbempropertyset.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTYSET CLSID<br/>                                                      |
| IID<br/>                      | \_ISWBEMPROPERTYSET IID<br/>                                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemPropertySet**](swbempropertyset.md)
</dt> <dt>

[**SWbemPropertySet. Remove**](swbempropertyset-remove.md)
</dt> <dt>

[**SWbemProperty. Value**](swbemproperty-value.md)
</dt> </dl>

 

 




