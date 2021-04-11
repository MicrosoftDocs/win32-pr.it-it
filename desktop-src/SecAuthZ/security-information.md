---
description: Identifica le informazioni di sicurezza relative all'oggetto impostate o sottoposte a query.
ms.assetid: e3e8b35d-9d18-4611-a898-72ca13e40d33
title: SECURITY_INFORMATION (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaad4b9f61a20b26397081433b88782dcbc33f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226314"
---
# <a name="security_information"></a>informazioni di sicurezza \_

Il tipo di dati **\_ informazioni di sicurezza** identifica le informazioni di sicurezza relative a oggetti impostate o sottoposte a query. Queste informazioni di sicurezza includono:

-   Proprietario di un oggetto
-   Gruppo primario di un oggetto
-   [*Elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) di un oggetto
-   [*Elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL) di un oggetto


```C++
typedef DWORD SECURITY_INFORMATION, *PSECURITY_INFORMATION;
```



## <a name="remarks"></a>Commenti

Alcuni membri delle **\_ informazioni di sicurezza** funzionano solo con la funzione [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) . Questi membri non vengono restituiti nella struttura restituita da altre funzioni di sicurezza, ad esempio [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) o [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Ogni elemento di informazioni di sicurezza è designato da un flag di bit. Ogni flag di bit può essere uno dei valori seguenti. Per ulteriori informazioni, vedere le funzioni [**SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask) e [**QuerySecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask) .



| Valore/diritti necessari per eseguire query/set                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_informazioni di sicurezza \_ sugli attributi<br/> Diritto richiesto per eseguire una query: **\_ controllo Read**<br/> Diritto necessario per impostare: **scrittura \_ DAC**<br/>                                                                                     | Proprietà della risorsa dell'oggetto a cui si fa riferimento. Le proprietà delle risorse vengono archiviate \_ in \_ tipi Ace attributo risorsa di sistema \_ nell'elenco SACL del descrittore di sicurezza.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo flag di bit non è disponibile.<br/> <br/>                 |
| \_informazioni sulla sicurezza del backup \_<br/> Diritto richiesto per eseguire una query: **sicurezza del \_ sistema \_** di **\_ controllo** e accesso in lettura<br/> Diritto necessario per impostare: **scrittura dell' \_ applicazione livello dati** e **scrittura del \_ proprietario** e **accesso alla \_ \_ sicurezza del sistema**<br/> | Tutte le parti del descrittore di sicurezza. Questa operazione è utile per il software di backup e ripristino che deve mantenere l'intero descrittore di sicurezza.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo flag di bit non è disponibile.<br/> <br/>                                                  |
| \_informazioni di sicurezza DACL \_<br/> Diritto richiesto per eseguire una query: **\_ controllo Read**<br/> Diritto necessario per impostare: **scrittura \_ DAC**<br/>                                                                                          | Viene fatto riferimento all'elenco DACL dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                                        |
| \_informazioni sulla sicurezza del gruppo \_<br/> Diritto richiesto per eseguire una query: **\_ controllo Read**<br/> Diritto necessario per impostare: **scrittura del \_ proprietario** <br/>                                                                                      | Viene fatto riferimento all'identificatore di gruppo primario dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                    |
| ETICHETTA \_ informazioni di sicurezza \_<br/> Diritto richiesto per eseguire una query: **\_ controllo Read**<br/> Diritto necessario per impostare: **scrittura del \_ proprietario** <br/>                                                                                      | Si fa riferimento all'etichetta di integrità obbligatoria.<br/> L'etichetta di integrità obbligatoria è una voce ACE nell'elenco SACL dell'oggetto.<br/> **Windows Server 2003 e Windows XP:** Questo flag di bit non è disponibile.<br/> <br/>                                                                                                                                    |
| \_informazioni di sicurezza del proprietario \_<br/> Diritto richiesto per eseguire una query: **\_ controllo Read**<br/> Diritto necessario per impostare: **scrittura del \_ proprietario** <br/>                                                                                      | Viene fatto riferimento all'identificatore del proprietario dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                            |
| \_informazioni di \_ sicurezza \_ DACL protette<br/> Diritto richiesto per eseguire una query: non disponibile<br/> Diritto necessario per impostare: **scrittura \_ DAC**<br/>                                                                                   | Il DACL non può ereditare le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE).<br/>                                                                                                                                                                                                                   |
| \_informazioni di \_ sicurezza \_ SACL protette<br/> Diritto richiesto per eseguire una query: non disponibile<br/> Diritto necessario per impostare: **accesso \_ alla \_ sicurezza del sistema**<br/>                                                                     | Il SACL non può ereditare voci ACE.<br/>                                                                                                                                                                                                                                                                                                                                      |
| \_informazioni di sicurezza SACL \_<br/> Diritto richiesto per eseguire una query: **accedere alla \_ \_ sicurezza del sistema**<br/> Diritto necessario per impostare: **accesso \_ alla \_ sicurezza del sistema**<br/>                                                                 | Viene fatto riferimento al SACL dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                                        |
| \_informazioni di sicurezza \_ sull'ambito<br/> Diritto richiesto per eseguire una query: **\_ controllo Read**<br/> Diritto necessario per impostare: **accesso \_ alla \_ sicurezza del sistema**<br/>                                                                           | Identificatore del criterio di accesso centrale applicabile nell'oggetto a cui si fa riferimento. Ogni identificatore del CAP viene archiviato in un \_ \_ \_ \_ tipo ACE con ambito di sistema nell'elenco SACL della SD.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo flag di bit non è disponibile.<br/> <br/> |
| \_informazioni di sicurezza DACL \_ non \_ protette<br/> Diritto richiesto per eseguire una query: non disponibile<br/> Diritto necessario per impostare: **scrittura \_ DAC**<br/>                                                                                 | L'elenco DACL eredita le voci ACE dall'oggetto padre.<br/>                                                                                                                                                                                                                                                                                                                     |
| \_informazioni di sicurezza SACL \_ non \_ protette<br/> Diritto richiesto per eseguire una query: non disponibile<br/> Diritto necessario per impostare: **accesso \_ alla \_ sicurezza del sistema**<br/>                                                                   | Il SACL eredita le voci ACE dall'oggetto padre.<br/>                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Winnt. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo di accesso](access-control.md)
</dt> <dt>

[Strutture di controllo di accesso di base](authorization-structures.md)
</dt> <dt>

[**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
</dt> <dt>

[**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)
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

 

