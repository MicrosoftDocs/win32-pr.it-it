---
description: WMI include costanti di sicurezza usate per il controllo dell'accesso allo spazio dei nomi \_ \_ da SystemSecurity::GetCallerAccessRights.
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: Costanti dei diritti di accesso allo spazio dei nomi (Wbemcli.h)
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
ms.openlocfilehash: 6c23bcde9d085a6668fd5c57ee0ff51a7db61784de44d79080e2b2d2d1ee051f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992751"
---
# <a name="namespace-access-rights-constants"></a>Costanti per i diritti di accesso allo spazio dei nomi

WMI include costanti di sicurezza usate per il controllo dell'accesso allo spazio dei nomi [**\_ \_ da SystemSecurity::GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md). Per informazioni sulla sicurezza degli elenchi di controllo di accesso (ACL, DACL o ACL), vedere Elenchi di controllo di accesso [(ACL)](/windows/desktop/SecAuthZ/access-control-lists) e [**Diritti di accesso standard.**](/windows/desktop/SecAuthZ/standard-access-rights) Queste costanti sono definite **nell'enumerazione WBEM \_ SECURITY \_ FLAGS.**

<dl> <dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ ENABLE**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Abilita l'account e concede all'utente le autorizzazioni di lettura. Si tratta di un diritto di accesso predefinito per tutti gli utenti e corrisponde all'autorizzazione Abilita account scheda Sicurezza del controllo [*WMI*](gloss-w.md). Per altre informazioni, vedere [Impostazione della sicurezza dello spazio dei nomi con il controllo WMI.](setting-namespace-security-with-the-wmi-control.md)


</dt> </dl> </dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**METODO EXECUTE \_ WBEM \_**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Consente l'esecuzione di metodi. I provider possono eseguire controlli di accesso aggiuntivi. Si tratta di un diritto di accesso predefinito per tutti gli utenti e corrisponde all'autorizzazione Execute Methods (Esegui metodi) scheda Sicurezza del controllo WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ FULL \_ WRITE \_ REP**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Consente a un account utente di scrivere nelle classi del repository WMI e nelle istanze di . Un utente non può scrivere nelle classi di sistema. Solo i membri del gruppo Administrators dispongono di questa autorizzazione. **WBEM \_ FULL \_ WRITE \_ REP** corrisponde all'autorizzazione di scrittura completa nel scheda Sicurezza del controllo WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ PARTIAL \_ WRITE \_ REP**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Consente di scrivere dati solo nelle istanze, non nelle classi. Un utente non può scrivere classi nel [*repository WMI*](gloss-w.md). Solo i membri del gruppo Administrators dispongono di questo diritto. **WBEM \_ PARTIAL \_ WRITE \_ REP** corrisponde all'autorizzazione di scrittura parziale per scheda Sicurezza del controllo WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**PROVIDER DI SCRITTURA WBEM \_ \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Consente la scrittura di classi e istanze nei provider. Si noti che i provider possono eseguire controlli di accesso aggiuntivi durante la rappresentazione di un utente. Si tratta di un diritto di accesso predefinito per tutti gli utenti e corrisponde all'autorizzazione di scrittura del provider scheda Sicurezza del controllo WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**ACCESSO REMOTO WBEM \_ \_**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Consente a un account utente di eseguire in remoto tutte le operazioni consentite dalle autorizzazioni descritte in precedenza. Solo i membri del gruppo Administrators dispongono di questo diritto. **WBEM \_ REMOTE \_ ACCESS** corrisponde all'autorizzazione Remote Enable per scheda Sicurezza del controllo WMI.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Wbemcli.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[Protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Oggetti descrittore di sicurezza WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Modifica della sicurezza dell'accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

