---
description: Elenca i tipi ACE attualmente definiti.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (Winnt.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa93490c4cf74ac33e3b15eeb888f011f81aa2b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470987"
---
# <a name="ace"></a>ASSO

Una **voce ACE** è una [*voce di controllo di accesso*](/windows/desktop/SecGloss/a-gly) in un elenco di [*controllo*](/windows/desktop/SecGloss/a-gly) di accesso (ACL).

Nella tabella seguente sono elencati i tipi **ACE** attualmente definiti.




| Tipo ACE | Struttura | Tipo ACL | 
|----------|-----------|----------|
| <ul><li>Accesso consentito</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a> | Discrezionale | 
| <ul><li>Accesso consentito</li><li>Consente il callback durante il controllo di accesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a> | Discrezionale | 
| <ul><li>Accesso consentito</li><li>Specifico dell'oggetto</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a> | Discrezionale | 
| <ul><li>Accesso consentito</li><li>Specifico dell'oggetto</li><li>Consente il callback durante il controllo di accesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a> | Discrezionale | 
| <ul><li>Accesso negato</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a> | Discrezionale | 
| <ul><li>Accesso negato</li><li>Consente il callback durante il controllo di accesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a> | Discrezionale | 
| <ul><li>Accesso negato</li><li>Specifico dell'oggetto</li><li>Consente il callback durante il controllo di accesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a> | Discrezionale | 
| <ul><li>Accesso negato</li><li>Specifico dell'oggetto</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a> | Discrezionale | 
| <ul><li>Allarme di sistema</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a> | Sistema | 
| <ul><li>Allarme di sistema</li><li>Consente il callback durante il controllo di accesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a> | Sistema | 
| <ul><li>Allarme di sistema</li><li>Specifico dell'oggetto</li><li>Consente il callback durante il controllo di accesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a> | Sistema | 
| <ul><li>Allarme di sistema</li><li>Specifico dell'oggetto</li></ul> | <a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a> | Sistema | 
| <ul><li>Controllo del sistema</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a> | Sistema | 
| <ul><li>Controllo del sistema</li><li>Consente il callback durante il controllo di accesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a> | Sistema | 
| <ul><li>Controllo del sistema</li><li>Specifico dell'oggetto</li><li>Consente il callback durante il controllo di accesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a> | Sistema | 
| <ul><li>Controllo del sistema</li><li>Specifico dell'oggetto</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a> | Sistema | 




 

Le voci ACE di allarme di sistema e specifiche dell'oggetto non sono attualmente supportate.

> [!Note]  
> Ogni ACE inizia con una [**struttura ACE \_ HEADER.**](/windows/desktop/api/Winnt/ns-winnt-ace_header) Il formato dei dati che segue l'intestazione varia in base al tipo ACE specificato nell'intestazione.

 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Winnt.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[**ACCESSO \_ CONSENTITO \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[**ACE \_ ACCESSO \_ NEGATO**](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[**ACE \_ DI SYSTEM ALARM \_**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[**ACE \_ DI CONTROLLO \_ DEL SISTEMA**](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

