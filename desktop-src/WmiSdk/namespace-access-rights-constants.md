---
description: "WMI include costanti di sicurezza usate per il controllo dell'accesso allo spazio dei nomi da \\_ \\_ SystemSecurity:: GetCallerAccessRights."
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: Costanti dei diritti di accesso allo spazio dei nomi (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEM_ENABLE
- WBEM_METHOD_EXECUTE
- WBEM_FULL_WRITE_REP
- WBEM_PARTIAL_WRITE_REP
- WBEM_WRITE_PROVIDER
- WBEM_REMOTE_ACCESS
api_type:
- HeaderDef
api_location:
- Wbemcli.h
ms.openlocfilehash: 469e036b7cd385fa2ac2bae23e0da081288b536b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049342"
---
# <a name="namespace-access-rights-constants"></a>Costanti dei diritti di accesso allo spazio dei nomi

WMI include costanti di sicurezza usate per il controllo dell'accesso allo spazio dei nomi da [**\_ \_ SystemSecurity:: GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md). Per informazioni di sicurezza sugli elenchi di controllo di accesso (ACL, DACL o SACL), vedere [elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) e [**diritti di accesso standard**](/windows/desktop/SecAuthZ/standard-access-rights). Queste costanti sono definite nell'enumerazione **flag di \_ sicurezza \_ WBEM** .

<dl> <dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**\_Abilitazione di WBEM**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Abilita l'account e concede le autorizzazioni di lettura dell'utente. Si tratta di un diritto di accesso predefinito per tutti gli utenti e corrisponde all'autorizzazione Abilita account per la scheda sicurezza del [*controllo WMI*](gloss-w.md). Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi con il controllo WMI](setting-namespace-security-with-the-wmi-control.md).


</dt> </dl> </dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**\_esecuzione del metodo WBEM \_**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Consente l'esecuzione di metodi. I provider possono eseguire ulteriori controlli di accesso. Si tratta di un diritto di accesso predefinito per tutti gli utenti e corrisponde all'autorizzazione Execute Methods nella scheda sicurezza del controllo WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**\_ \_ Rep scrittura completa \_ WBEM**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Consente a un account utente di scrivere nelle classi del repository WMI e delle istanze di. Un utente non può scrivere in classi di sistema. Solo i membri del gruppo Administrators dispongono di questa autorizzazione. **WBEM \_ Il \_ \_ rep di scrittura completo** corrisponde all'autorizzazione di scrittura completa nella scheda sicurezza del controllo WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**\_ \_ Rep scrittura parziale \_ WBEM**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Consente di scrivere i dati solo nelle istanze, non nelle classi. Un utente non può scrivere classi nel [*repository WMI*](gloss-w.md). Solo i membri del gruppo Administrators dispongono di questo diritto. **WBEM \_ Il \_ \_ rep di scrittura parziale** corrisponde all'autorizzazione di scrittura parziale nella scheda sicurezza del controllo WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**\_provider di scrittura WBEM \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Consente di scrivere classi e istanze nei provider. Si noti che i provider possono eseguire ulteriori controlli di accesso durante la rappresentazione di un utente. Si tratta di un diritto di accesso predefinito per tutti gli utenti e corrisponde all'autorizzazione di scrittura del provider nella scheda sicurezza del controllo WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**\_accesso remoto \_ WBEM**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Consente a un account utente di eseguire in modalità remota qualsiasi operazione consentita dalle autorizzazioni descritte in precedenza. Solo i membri del gruppo Administrators dispongono di questo diritto. **WBEM \_ \_Accesso remoto** corrisponde all'autorizzazione Abilita remoto nella scheda sicurezza del controllo WMI.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Wbemcli. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[Sicurezza degli spazi dei nomi WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Oggetti descrittore di sicurezza WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

