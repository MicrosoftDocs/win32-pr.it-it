---
description: Il metodo Add dell'oggetto SWbemPrivilegeSet aggiunge un oggetto SWbemPrivilege alla raccolta SWbemPrivilegeSet. Se nella raccolta esiste già un privilegio con lo stesso nome, viene sostituito.
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: Metodo SWbemPrivilegeSet. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 080b9d3e3ab6dbfc0ed8afc8ac0476981b7c26e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049755"
---
# <a name="swbemprivilegesetadd-method"></a>SWbemPrivilegeSet. Add, metodo

Il metodo **Add** dell'oggetto [**SWbemPrivilegeSet**](swbemprivilegeset.md) aggiunge un oggetto [**SWbemPrivilege**](swbemprivilege.md) alla raccolta **SWbemPrivilegeSet** . Se nella raccolta esiste già un privilegio con lo stesso nome, viene sostituito.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iPrivilege* 
</dt> <dd>

Obbligatorio. Una delle costanti WMI del gruppo [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) . Queste costanti sono essenzialmente numeri interi che rappresentano privilegi specifici. Ad esempio, per aggiungere il privilegio che consente di arrestare un sistema di computer, usare la costante **wbemPrivilegeShutdown** . In uno script è necessario usare l'equivalente numerico 23 (0x17). Per un elenco completo di queste costanti e delle stringhe dei privilegi associate, vedere [**costanti Privilege**](privilege-constants.md).

</dd> <dt>

*bIsEnabled* \[ opzionale\]
</dt> <dd>

Valore booleano che Abilita o Disabilita questo privilegio. Il valore predefinito è **true**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, il metodo restituisce un oggetto [**SWbemPrivilege**](swbemprivilege.md) che rappresenta il nuovo privilegio. In caso contrario, viene restituito un oggetto null.

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **Add** , l'oggetto **Err** può contenere il codice di errore riportato nell'elenco seguente.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> </dl>

## <a name="examples"></a>Esempio

Un esempio di codice che usa questo metodo è descritto nell'argomento [**SWbemPrivilegeSet**](swbemprivilegeset.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPRIVILEGESET CLSID<br/>                                                     |
| IID<br/>                      | \_ISWBEMPRIVILEGESET IID<br/>                                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[Esecuzione di operazioni con privilegi](executing-privileged-operations.md)
</dt> <dt>

[Esecuzione di operazioni con privilegi tramite VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md)
</dt> <dt>

[**SWbemPrivilegeSet. Remove**](swbemprivilegeset-remove.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Costanti Privilege**](privilege-constants.md)
</dt> </dl>

 

 




