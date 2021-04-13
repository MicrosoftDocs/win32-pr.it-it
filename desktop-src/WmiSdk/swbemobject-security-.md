---
description: La \_ proprietà di sicurezza dell'oggetto SWbemObject viene utilizzata per leggere o impostare le impostazioni di sicurezza per un oggetto SWbemObject.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: Proprietà SWbemObject.Security_ (wbemdisp. h)
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
ms.openlocfilehash: f4d4b9aec7b6d800fa27609abd5d0cb1f3a435a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349221"
---
# <a name="swbemobjectsecurity_-property"></a>Proprietà SWbemObject. Security \_

La proprietà di **\_ sicurezza** dell'oggetto [**SWbemObject**](swbemobject.md) viene utilizzata per leggere o impostare le impostazioni di sicurezza per un oggetto **SWbemObject** . Questa proprietà è un oggetto [**SWbemSecurity**](swbemsecurity.md) . Le impostazioni di sicurezza in questo oggetto non indicano le impostazioni di autenticazione, rappresentazione o privilegio effettuate in una connessione a Strumentazione gestione Windows (WMI) o la sicurezza attiva per il proxy quando un oggetto viene recapitato a un sink in una chiamata asincrona. Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).

> [!Note]  
> Impostando la proprietà di **\_ sicurezza** di un oggetto [**SWbemObject**](swbemobject.md) su **null** , viene concesso l'accesso illimitato a tutti i tempi. Per ulteriori informazioni, vedere [**SWbemSecurity**](swbemsecurity.md).

 

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

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
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[Creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Impostazione della \_ sicurezza del processo dell'applicazione client \_](setting-client-application-process-security.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Costanti Privilege**](privilege-constants.md)
</dt> </dl>

 

 




