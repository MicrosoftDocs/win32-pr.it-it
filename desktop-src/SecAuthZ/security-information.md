---
description: Identifica le informazioni di sicurezza relative all'oggetto impostate o su cui viene eseguita una query.
ms.assetid: e3e8b35d-9d18-4611-a898-72ca13e40d33
title: SECURITY_INFORMATION (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eda92db81cc2325dcc2eb084c06aa5ac7ca92475cca92d8221e394af9704c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907201"
---
# <a name="security_information"></a>INFORMAZIONI DI \_ SICUREZZA

Il **tipo di dati SECURITY \_ INFORMATION** identifica le informazioni di sicurezza relative agli oggetti impostate o su cui viene eseguita una query. Queste informazioni di sicurezza includono:

-   Proprietario di un oggetto
-   Gruppo primario di un oggetto
-   Elenco [*di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) di un oggetto
-   Elenco [*di controllo di accesso*](/windows/desktop/SecGloss/s-gly) di sistema (SACL) di un oggetto


```C++
typedef DWORD SECURITY_INFORMATION, *PSECURITY_INFORMATION;
```



## <a name="remarks"></a>Commenti

Alcuni **membri di SECURITY \_ INFORMATION** funzionano solo con [**la funzione SetNamedSecurityInfo.**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) Questi membri non vengono restituiti nella struttura restituita da altre funzioni di sicurezza, ad esempio [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**o ConvertStringSecurityDescriptorToSecurityDescriptor.**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

Ogni elemento di informazioni di sicurezza è designato da un flag di bit. Ogni flag di bit può essere uno dei valori seguenti. Per altre informazioni, vedere le [**funzioni SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask) [**e QuerySecurityAccessMask.**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask)



| Valore/diritti necessari per eseguire query/impostare                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| INFORMAZIONI SULLA \_ SICUREZZA DEGLI \_ ATTRIBUTI<br/> Diritto necessario per eseguire una query: **READ \_ CONTROL**<br/> Diritto necessario per l'impostazione: **WRITE \_ DAC**<br/>                                                                                     | Proprietà della risorsa dell'oggetto a cui si fa riferimento. Le proprietà delle risorse vengono archiviate nei tipi ACE SYSTEM \_ RESOURCE \_ ATTRIBUTE \_ nell'elenco SACL del descrittore di sicurezza.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo flag di bit non è disponibile.<br/> <br/>                 |
| BACKUP \_ SECURITY \_ INFORMATION<br/> Diritto necessario per eseguire query: **READ \_ CONTROL** e **ACCESS SYSTEM \_ \_ SECURITY**<br/> Diritto necessario per l'impostazione: **WRITE \_ DAC** e **WRITE \_ OWNER** e **ACCESS SYSTEM \_ \_ SECURITY**<br/> | Tutte le parti del descrittore di sicurezza. Ciò è utile per il backup e il ripristino di software che deve mantenere l'intero descrittore di sicurezza.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo flag di bit non è disponibile.<br/> <br/>                                                  |
| INFORMAZIONI SULLA SICUREZZA \_ \_ DACL<br/> Diritto necessario per eseguire una query: **READ \_ CONTROL**<br/> Diritto necessario per l'impostazione: **WRITE \_ DAC**<br/>                                                                                          | Viene fatto riferimento all'elenco DACL dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                                        |
| INFORMAZIONI SULLA \_ SICUREZZA DEI \_ GRUPPI<br/> Diritto necessario per eseguire una query: **READ \_ CONTROL**<br/> Diritto necessario per l'impostazione: **WRITE \_ OWNER** <br/>                                                                                      | Viene fatto riferimento all'identificatore di gruppo primario dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                    |
| INFORMAZIONI SULLA \_ SICUREZZA DELLE \_ ETICHETTE<br/> Diritto necessario per eseguire una query: **READ \_ CONTROL**<br/> Diritto necessario per l'impostazione: **WRITE \_ OWNER** <br/>                                                                                      | Viene fatto riferimento all'etichetta di integrità obbligatoria.<br/> L'etichetta di integrità obbligatoria è una ACE nell'elenco SACL dell'oggetto.<br/> **Windows Server 2003 e Windows XP:** Questo flag di bit non è disponibile.<br/> <br/>                                                                                                                                    |
| INFORMAZIONI SULLA \_ SICUREZZA DEL \_ PROPRIETARIO<br/> Diritto necessario per eseguire una query: **READ \_ CONTROL**<br/> Diritto necessario per l'impostazione: **WRITE \_ OWNER** <br/>                                                                                      | Viene fatto riferimento all'identificatore del proprietario dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                            |
| INFORMAZIONI \_ DI SICUREZZA DACL \_ \_ PROTETTE<br/> Diritto necessario per eseguire una query: Non disponibile<br/> Diritto necessario per l'impostazione: **WRITE \_ DAC**<br/>                                                                                   | L'elenco DACL non può [*ereditare le voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE).<br/>                                                                                                                                                                                                                   |
| INFORMAZIONI \_ SULLA SICUREZZA SACL \_ \_ PROTETTE<br/> Diritto necessario per eseguire una query: Non disponibile<br/> Diritto necessario per l'impostazione: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                     | L'elenco SACL non può ereditare ACE.<br/>                                                                                                                                                                                                                                                                                                                                      |
| INFORMAZIONI SULLA SICUREZZA \_ \_ SACL<br/> Diritto necessario per eseguire query: **ACCESS \_ SYSTEM \_ SECURITY**<br/> Diritto necessario per l'impostazione: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                 | Si fa riferimento all'elenco SACL dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                                        |
| INFORMAZIONI SULLA \_ SICUREZZA \_ DELL'AMBITO<br/> Diritto necessario per eseguire una query: **READ \_ CONTROL**<br/> Diritto necessario per l'impostazione: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                           | Identificatore dei criteri di accesso centrale applicabile all'oggetto a cui si fa riferimento. Ogni identificatore CAP viene archiviato in un tipo ACE SYSTEM \_ SCOPED \_ POLICY ID \_ \_ nell'elenco SACL della DS.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo flag di bit non è disponibile.<br/> <br/> |
| INFORMAZIONI DI SICUREZZA \_ DACL \_ NON \_ PROTETTE<br/> Diritto necessario per eseguire una query: Non disponibile<br/> Diritto necessario per l'impostazione: **WRITE \_ DAC**<br/>                                                                                 | L'elenco DACL eredita le voci ACE dall'oggetto padre.<br/>                                                                                                                                                                                                                                                                                                                     |
| INFORMAZIONI DI SICUREZZA \_ SACL \_ NON \_ PROTETTE<br/> Diritto necessario per eseguire una query: Non disponibile<br/> Diritto necessario per l'impostazione: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                   | L'elenco SACL eredita le voci ACE dall'oggetto padre.<br/>                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Winnt.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo di accesso](access-control.md)
</dt> <dt>

[Strutture di controllo di accesso di base](authorization-structures.md)
</dt> <dt>

[**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
</dt> <dt>

[**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)
</dt> <dt>

[**GetFileSecurity**](/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)
</dt> <dt>

[**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)
</dt> <dt>

[**GetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity)
</dt> <dt>

[**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)
</dt> <dt>

[**GetUserObjectSecurity**](/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity)
</dt> <dt>

[**QuerySecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask)
</dt> <dt>

[**SetFileSecurity**](/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya)
</dt> <dt>

[**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity)
</dt> <dt>

[**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)
</dt> <dt>

[**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)
</dt> <dt>

[**SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[**SetUserObjectSecurity**](/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity)
</dt> <dt>

[**TreeResetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-treeresetnamedsecurityinfoa)
</dt> <dt>

[**TreeSetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-treesetnamedsecurityinfoa)
</dt> </dl>

 

