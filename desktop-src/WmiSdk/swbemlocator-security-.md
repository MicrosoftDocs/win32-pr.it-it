---
description: La \_ proprietà di sicurezza dell'oggetto SWbemLocator viene utilizzata per leggere o impostare le impostazioni di sicurezza per un oggetto SWbemLocator. Questa proprietà è un oggetto SWbemSecurity.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: Proprietà SWbemLocator.Security_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2aa61ebc3ef48c82405d960d5de42ab8f23dc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755026"
---
# <a name="swbemlocatorsecurity_-property"></a>Proprietà SWbemLocator. Security \_

La proprietà di **\_ sicurezza** dell'oggetto [**SWbemLocator**](swbemlocator.md) viene utilizzata per leggere o impostare le impostazioni di sicurezza per un oggetto **SWbemLocator** . Questa proprietà è un oggetto [**SWbemSecurity**](swbemsecurity.md) .

> [!Note]  
> Impostando la proprietà di **\_ sicurezza** di un oggetto [**SWbemLocator**](swbemlocator.md) su **null** , viene concesso l'accesso illimitato a tutti gli utenti in qualsiasi momento. Per ulteriori informazioni, vedere [**SWbemSecurity**](swbemsecurity.md).

 

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Le proprietà di un oggetto **SWbemLocator. \_ Security** non hanno valori predefiniti. Se si tenta di ottenere il valore di [**SWbemSecurity. AuthenticationLevel**](swbemsecurity-authenticationlevel.md) o [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) su un oggetto [**SWbemLocator**](swbemlocator.md) prima di impostarlo, viene restituito un errore [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMLOCATOR CLSID<br/>                                                          |
| IID<br/>                      | \_ISWBEMLOCATOR IID<br/>                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[Creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Esecuzione di operazioni con privilegi tramite VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[Impostazione della \_ sicurezza del processo dell'applicazione client \_](setting-client-application-process-security.md)
</dt> <dt>

[**Oggetto SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




