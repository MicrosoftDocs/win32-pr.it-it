---
description: L'oggetto SWbemSecurity Ottiene o imposta le impostazioni di sicurezza, ad esempio i privilegi, le rappresentazioni COM e i livelli di autenticazione assegnati a un oggetto.
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.tgt_platform: multiple
title: Oggetto SWbemSecurity (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity
- ISWbemSecurity
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: da59c3b996a80384c133336503124141f0907f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309784"
---
# <a name="swbemsecurity-object"></a>Oggetto SWbemSecurity

L'oggetto **SWbemSecurity** Ottiene o imposta le impostazioni di sicurezza, ad esempio i privilegi, le rappresentazioni com e i livelli di autenticazione assegnati a un oggetto. Gli oggetti [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md)e [**SWbemEventSource**](swbemeventsource.md) hanno una proprietà **di \_ sicurezza** , che corrisponde all'oggetto **SWbemSecurity** . Quando si recupera un'istanza o si Visualizza il registro di protezione WMI, potrebbe essere necessario impostare le proprietà dell'oggetto di **sicurezza \_** .

La chiamata [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript non è in grado di creare l'oggetto di sicurezza. Le impostazioni di sicurezza in questo oggetto non identificano le impostazioni di autenticazione, rappresentazione o privilegio in una connessione a WMI oppure la sicurezza attiva per il proxy quando un oggetto viene recapitato a un sink in una chiamata asincrona. Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).

## <a name="members"></a>Membri

L'oggetto **SWbemSecurity** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **SWbemSecurity** dispone di queste proprietà.



| Proprietà                                                                    | Tipo di accesso           | Descrizione                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)<br/> | Lettura/Scrittura<br/> | Valore numerico che definisce il livello di autenticazione COM assegnato a questo oggetto. Questa impostazione determina la modalità di protezione delle informazioni inviate da WMI.<br/>                                                                 |
| [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md)<br/>   | Lettura/Scrittura<br/> | Valore numerico che definisce il livello di rappresentazione COM assegnato a questo oggetto. Questa impostazione determina se i processi di proprietà di WMI possono rilevare o utilizzare le credenziali di sicurezza quando si effettuano chiamate ad altri processi.<br/> |
| [**Privilegi**](swbemsecurity-privileges.md)<br/>                   | Sola lettura<br/>  | Oggetto [**SWbemPrivilegeSet**](swbemprivilegeset.md) che definisce i privilegi per questo oggetto. Per ulteriori informazioni, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).<br/>                    |



 

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

[Oggetti API di scripting](scripting-api-objects.md)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> <dt>

[Impostazione della \_ sicurezza del processo dell'applicazione client \_](setting-client-application-process-security.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 

