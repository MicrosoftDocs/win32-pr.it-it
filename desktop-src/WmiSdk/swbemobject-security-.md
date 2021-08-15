---
description: La proprietà Security dell'oggetto SWbemObject viene usata per leggere o impostare le impostazioni di sicurezza per un \_ oggetto SWbemObject.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: SWbemObject.Security_ proprietà (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Security_
- ISWbemObject.Security_
- ISWbemObject.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d83a155057e445848e727615978c3414e96f63334ffc70c78d5f055a396b53f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313785"
---
# <a name="swbemobjectsecurity_-property"></a>Proprietà SWbemObject.Security \_

La **\_ proprietà Security** dell'oggetto [**SWbemObject**](swbemobject.md) viene usata per leggere o impostare le impostazioni di sicurezza per un **oggetto SWbemObject.** Questa proprietà è un [**oggetto SWbemSecurity.**](swbemsecurity.md) Le impostazioni di sicurezza in questo oggetto non indicano le impostazioni di autenticazione, rappresentazione o privilegio effettuate in una connessione a Strumentazione gestione Windows (WMI) o la sicurezza in vigore per il proxy quando un oggetto viene recapitato a un sink in una chiamata asincrona. Per altre informazioni, vedere [Gestione della sicurezza WMI.](maintaining-wmi-security.md)

> [!Note]  
> **L'impostazione \_ della** proprietà Security di [**un oggetto SWbemObject**](swbemobject.md) su **NULL** concede sempre l'accesso illimitato a tutti gli utenti. Per altre informazioni, vedere [**SWbemSecurity.**](swbemsecurity.md)

 

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemObject.Security_ As Object
```



## <a name="property-value"></a>Valore proprietà

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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto SWbem**](swbemobject.md)
</dt> <dt>

[Creazione di un'applicazione o uno script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Impostazione della sicurezza \_ del processo \_ dell'applicazione client](setting-client-application-process-security.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Costanti privilege**](privilege-constants.md)
</dt> </dl>

 

 




