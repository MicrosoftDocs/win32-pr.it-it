---
description: Set di flag di bit che qualificano il significato di un descrittore di sicurezza o dei relativi componenti.
ms.assetid: 9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2
title: SECURITY_DESCRIPTOR_CONTROL (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3def788407093d0a487640d1ad0e445b61fe20e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308136"
---
# <a name="security_descriptor_control"></a>\_controllo descrittore di sicurezza \_

Il tipo di dati del **\_ \_ controllo descrittore di sicurezza** è un set di flag di bit che qualificano il significato di un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) o dei relativi componenti. Ogni descrittore di sicurezza ha un membro del **controllo** che archivia i bit di **\_ \_ controllo del descrittore di sicurezza**


```C++
typedef WORD SECURITY_DESCRIPTOR_CONTROL, *PSECURITY_DESCRIPTOR_CONTROL;
```



## <a name="remarks"></a>Commenti

Per ottenere i bit di controllo di un descrittore di sicurezza, chiamare la funzione [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) . Per impostare i bit di controllo di un descrittore di sicurezza, utilizzare le funzioni per la modifica dei descrittori di sicurezza. Per un elenco di queste funzioni, vedere la sezione vedere anche.

Le applicazioni possono utilizzare la funzione [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) per impostare i bit di controllo relativi all'ereditarietà automatica delle voci ACE.

Il valore del controllo recuperato dalla funzione [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) può includere una combinazione dei seguenti flag di bit del **\_ \_ controllo del descrittore di sicurezza** .



| Valore                                                     | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SE \_ DACL \_ auto \_ eredita \_ automaticamente<br/> 0x0100<br/> | Indica un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) necessario in cui l' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) viene configurato per supportare la propagazione automatica di voci di controllo di [*accesso*](/windows/desktop/SecGloss/a-gly) ereditabili (ACE) a oggetti figlio esistenti.<br/> Per gli [*elenchi di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) che supportano l'ereditarietà automatica, questo bit è sempre impostato. I server protetti possono chiamare la funzione [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) per convertire un descrittore di sicurezza e impostare questo flag. <br/> |
| SE \_ DACL \_ viene \_ ereditato automaticamente<br/> 0x0400<br/>    | Indica un descrittore di sicurezza in cui l' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) viene configurato per supportare la propagazione automatica delle [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) ereditabili agli oggetti figlio esistenti.<br/> Per gli [*elenchi di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) che supportano l'ereditarietà automatica, questo bit è sempre impostato. I server protetti possono chiamare la funzione [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) per convertire un descrittore di sicurezza e impostare questo flag. <br/>                                                                                                  |
| SE \_ DACL è \_ impostato come predefinito<br/> 0x0008<br/>          | Indica un descrittore di sicurezza con un DACL predefinito. Se, ad esempio, l'autore di un oggetto non specifica un DACL, l'oggetto riceve l'elenco DACL predefinito dal [*token di accesso*](/windows/desktop/SecGloss/a-gly) del creatore. Questo flag può influire sul modo in cui il sistema considera l'elenco DACL rispetto all'ereditarietà ACE. Questo flag viene ignorato dal sistema se il \_ flag if \_ non è impostato.<br/> Questo flag viene utilizzato per determinare il modo in cui deve essere calcolato l'elenco DACL finale nell'oggetto e non viene archiviato fisicamente nel controllo del descrittore di sicurezza dell'oggetto a protezione diretta.<br/> Per impostare questo flag, utilizzare la funzione [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) .<br/>                                                                                                                                                                      |
| \_elenco DACL se \_ presente<br/> 0x0004<br/>            | Indica un descrittore di sicurezza con un DACL. Se questo flag non è impostato o se questo flag è impostato e l'elenco DACL è **null**, il descrittore di sicurezza consente l'accesso completo a tutti gli utenti.<br/> Questo flag viene utilizzato per mantenere le informazioni di sicurezza specificate da un chiamante finché il descrittore di sicurezza non è associato a un oggetto a protezione diretta. Quando il descrittore di sicurezza è associato a un oggetto a protezione diretta, il \_ \_ flag di presenza DACL se è sempre impostato nel controllo del descrittore di sicurezza.<br/> Per impostare questo flag, utilizzare la funzione [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) .<br/>                                                                                                                                                                                                                                                                                                   |
| \_elenco DACL se \_ protetto<br/> 0x1000<br/>          | Impedisce la modifica del DACL del descrittore di sicurezza da parte di ACE ereditabili. Per impostare questo flag, utilizzare la funzione [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_gruppo se \_ impostato come predefinito<br/> 0x0002<br/>         | Indica che l' [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) del gruppo di descrittori di sicurezza è stato fornito da un meccanismo predefinito. Questo flag può essere usato da un gestore di risorse per identificare gli oggetti il cui gruppo di descrittori di sicurezza è stato impostato da un meccanismo predefinito. Per impostare questo flag, utilizzare la funzione [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SE il \_ proprietario è \_ impostato come predefinito<br/> 0x0001<br/>         | Indica che il SID del proprietario del descrittore di sicurezza è stato fornito da un meccanismo predefinito. Questo flag può essere usato da un gestore di risorse per identificare gli oggetti il cui proprietario è stato impostato da un meccanismo predefinito. Per impostare questo flag, utilizzare la funzione [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| \_controllo RM \_ se \_ valido<br/> 0x4000<br/>       | Indica che il controllo Resource Manager è valido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| SE \_ SACL \_ auto \_ eredita automaticamente \_ req<br/> 0x0200<br/> | Indica un descrittore di sicurezza necessario in cui l' [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL) viene configurato per supportare la propagazione automatica delle ACE ereditabili agli oggetti figlio esistenti.<br/> Questo bit viene impostato dal sistema quando viene eseguito l'algoritmo di ereditarietà automatica per l'oggetto e i relativi oggetti figlio esistenti. Per convertire un descrittore di sicurezza e impostare questo flag, i server protetti possono chiamare la funzione [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) .<br/>                                                                                                                                                                                                                                                                                   |
| SE \_ SACL \_ viene \_ ereditato automaticamente<br/> 0x0800<br/>    | Indica un descrittore di sicurezza in cui l' [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL) viene configurato per supportare la propagazione automatica di ACE ereditabili a oggetti figlio esistenti.<br/> Questo bit viene impostato dal sistema quando viene eseguito l'algoritmo di ereditarietà automatica per l'oggetto e i relativi oggetti figlio esistenti. Per convertire un descrittore di sicurezza e impostare questo flag, i server protetti possono chiamare la funzione [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) . <br/>                                                                                                                                                                                                                                                                                           |
| il \_ SACL se è \_ impostato come predefinito<br/> 0x0008<br/>          | Un meccanismo predefinito, anziché il [*provider*](/windows/desktop/SecGloss/p-gly) originale del descrittore di sicurezza, fornito il SACL. Questo flag può influire sul modo in cui il sistema considera l'elenco SACL, rispetto all'ereditarietà ACE. Questo flag viene ignorato dal sistema se \_ \_ non è impostato il flag se è presente. Per impostare questo flag, utilizzare la funzione [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_SACL se \_ presente<br/> 0x0010<br/>            | Indica un descrittore di sicurezza con un SACL. Per impostare questo flag, utilizzare la funzione [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SE \_ SACL è \_ protetto<br/> 0x2000<br/>          | Impedisce la modifica del SACL del descrittore di sicurezza da parte di ACE ereditabili. Per impostare questo flag, utilizzare la funzione [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SE \_ \_ relativo<br/> 0x8000<br/>           | Indica un [*descrittore di sicurezza relativo a se stesso*](/windows/desktop/SecGloss/s-gly). Se questo flag non è impostato, il descrittore di sicurezza è in formato assoluto. Per ulteriori informazioni, vedere la pagina relativa ai [descrittori di sicurezza assoluti e Self-Relative](absolute-and-self-relative-security-descriptors.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Winnt. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo di accesso di basso livello](low-level-access-control.md)
</dt> <dt>

[Strutture di controllo di accesso di base](authorization-structures.md)
</dt> <dt>

[**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity)
</dt> <dt>

[**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol)
</dt> <dt>

[**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)
</dt> <dt>

[**GetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)
</dt> <dt>

[**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)
</dt> <dt>

[**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)
</dt> <dt>

[**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol)
</dt> <dt>

[**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)
</dt> <dt>

[**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)
</dt> <dt>

[**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)
</dt> <dt>

[**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)
</dt> </dl>

 

