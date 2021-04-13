---
description: La proprietà Privileges è un oggetto SWbemPrivilegeSet. Questa proprietà viene utilizzata per abilitare o disabilitare i privilegi di Windows specifici. Potrebbe essere necessario impostare uno di questi privilegi per eseguire attività specifiche mediante l'API Strumentazione gestione Windows (WMI).
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: Proprietà SWbemSecurity. Privileges (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.Privileges
- ISWbemSecurity.Privileges
- ISWbemSecurity.get_Privileges
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6fd8e1c0f9b6667b49d0956bcea5ac9e187443d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226803"
---
# <a name="swbemsecurityprivileges-property"></a>Proprietà SWbemSecurity. Privileges

La proprietà **Privileges** è un oggetto [**SWbemPrivilegeSet**](swbemprivilegeset.md) . Questa proprietà viene utilizzata per abilitare o disabilitare i privilegi di Windows specifici. Potrebbe essere necessario impostare uno di questi privilegi per eseguire attività specifiche mediante l'API Strumentazione gestione Windows (WMI).

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Questa impostazione consente di concedere o revocare i privilegi come parte di una stringa del moniker WMI. Per l'elenco completo dei valori applicabili, vedere [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) and [**Privilege Constants**](privilege-constants.md).

È possibile modificare i privilegi definiti per gli oggetti [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) aggiungendo oggetti [**SWbemPrivilege**](swbemprivilege.md) alla proprietà **Privileges** .

Esistono differenze fondamentali nel modo in cui le diverse versioni di Windows gestiscono le modifiche ai privilegi. Se si sviluppa un'applicazione che viene usata solo nelle piattaforme Windows, è possibile impostare o revocare i privilegi in qualsiasi momento.

Nell'esempio seguente viene impostato **SeDebugPrivilege** sulla connessione iniziale del moniker per ottenere un oggetto [**SWbemServices**](swbemservices.md) .


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



Per altre informazioni su come formattare la stringa di sicurezza per una connessione moniker, vedere [**costanti Privilege**](privilege-constants.md).

Nell'esempio seguente viene eseguita la stessa attività, ma viene impostato il privilegio dopo l'accesso iniziale a WMI.


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



Si noti che per le chiamate a [**SwbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md), è necessario usare il nome completo del privilegio di sicurezza, ad esempio, "SeDebugPrivilege" invece di "debug".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSECURITY CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMSECURITY IID<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Esecuzione di operazioni con privilegi](executing-privileged-operations.md)
</dt> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> </dl>

 

 




