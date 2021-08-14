---
description: Il metodo Item dell'oggetto SWbemPrivilegeSet restituisce un oggetto SWbemPrivilege dalla raccolta. Il metodo Item è il metodo predefinito di un oggetto SWbemPrivilegeSet.
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.tgt_platform: multiple
title: Metodo SWbemPrivilegeSet.Item (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 93180f168820acce2bf2564ef108c509713a22e68cfa16fbb8f2abeff17b5bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313523"
---
# <a name="swbemprivilegesetitem-method"></a>Metodo SWbemPrivilegeSet.Item

Il **metodo Item** dell'oggetto [**SWbemPrivilegeSet**](swbemprivilegeset.md) restituisce un [**oggetto SWbemPrivilege**](swbemprivilege.md) dalla raccolta. Il **metodo Item** è il metodo predefinito di un oggetto **SWbemPrivilegeSet.**

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objPrivilege = .Item( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iPrivilege* 
</dt> <dd>

Obbligatorio. Una delle costanti WMI del gruppo [**WbemPrivilegeEnum.**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) Queste costanti sono essenzialmente numeri interi che rappresentano privilegi specifici. Ad esempio, per ottenere il privilegio che consente di arrestare un sistema Windows, usare la costante **wbemPrivilegeShutdown** o l'equivalente numerico di 23 (0x17).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, viene [**restituito l'oggetto SWbemPrivilege**](swbemprivilege.md) richiesto.

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **Item,** **l'oggetto Err** può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrNotFound** - 2147749890 (0x80041002)
</dt> <dd>

Il privilegio specificato non esiste.

</dd> </dl>

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene utilizzato il **metodo Item**


```VB
strComputer ="."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")
Set colServices = objWMIService.ExecQuery( _
    "Select * from Win32_Service")
For Each objService In colServices
    WScript.Echo objService.Properties_.Item("Caption")
Next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemPrivilegeSet<br/>                                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[Esecuzione di operazioni con privilegi](executing-privileged-operations.md)
</dt> <dt>

[**SWbemPrivilege**](swbemprivilege.md)
</dt> </dl>

 

 




