---
description: Imposta il parametro rights come bitmap con ogni bit corrispondente a un diritto di accesso.
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: Metodo GetCallerAccessRights della classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetCallerAccessRights
api_type:
- COM
api_location:
- All
ms.openlocfilehash: c86ea3044411e33026ed6328fcfc227e615648b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315997"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a>Metodo GetCallerAccessRights della \_ \_ classe SystemSecurity

Il metodo **\_ \_ SystemSecurity:: GetCallerAccessRights** imposta il parametro *Rights* come bitmap con ogni bit corrispondente a un diritto di accesso. Qualsiasi client può chiamare questo oggetto per determinare i diritti di cui dispone il client. Questo metodo è utile per i client che abilitano o disabilitano le funzionalità. Ad esempio, un'applicazione GUI potrebbe disabilitare un pulsante se l'utente attualmente connesso non dispone dei diritti di esecuzione del metodo.

Qualsiasi client abilitato ha il diritto di chiamare **GetCallerAccessRights**, anche se tale client non dispone dei diritti generali di esecuzione del metodo.

## <a name="syntax"></a>Sintassi


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*diritti* \[ di out\]
</dt> <dd>

Diritti di accesso del client. Per ulteriori informazioni, vedere [**\_ \_ SystemSecurity**](--systemsecurity.md) e le [costanti di sicurezza WMI](wmi-security-constants.md).

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ Abilita** (1 (0x1))


</dt> <dd>

Abilita l'account e concede le autorizzazioni di lettura dell'utente. Questo è il diritto di accesso predefinito per tutti gli utenti.

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ METODO \_ Execute** (2 (0x2))


</dt> <dd>

Consente l'esecuzione di metodi.

> [!Note]  
> I provider possono eseguire ulteriori controlli di accesso.

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ \_ \_ Rep scrittura completa** (4 (0x4))


</dt> <dd>

Consente al chiamante, al contesto di sicurezza o all'utente di scrivere in classi e istanze ad eccezione delle classi di sistema.

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ \_ \_ Rep scrittura parziale** (8 (0x8))


</dt> <dd>

Consente al chiamante, al contesto di sicurezza o all'utente di scrivere le istanze del provider ma non le classi statiche o le istanze statiche nel repository.

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ \_Provider di scrittura** (16 (0x10))


</dt> <dd>

Consente al chiamante, al contesto di sicurezza o all'utente di scrivere classi e istanze nei provider.

> [!Note]  
> I provider di rappresentazione possono eseguire ulteriori controlli di accesso.

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ \_Accesso remoto** (32 (0x20))


</dt> <dd>

Consente a un account utente di eseguire in modalità remota qualsiasi operazione consentita dalle autorizzazioni impostate da altri bit.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Leggi \_ CONTROLLO** (131072 (0x20000))


</dt> <dd>

Consente l'accesso in lettura ai descrittori di sicurezza.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Scrivi \_ DAC** (262144 (0x40000))


</dt> <dd>

Consente l'accesso in scrittura agli elenchi di controllo di accesso discrezionale (DACL).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un valore **HRESULT** che indica lo stato della chiamata al metodo. Nell'elenco seguente sono elencati i valori restituiti significativi per [**Set9XUserList**](--systemsecurity-set9xuserlist.md). Per gli script e le applicazioni Visual Basic, il risultato può essere ottenuto da [OutParameters. returnValue](parsing-outparameters-objects.md). Per altre informazioni, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**WBEM \_ E \_ metodo \_ disabilitato**
</dt> <dd>

Questo metodo non è supportato nelle versioni supportate di Windows.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity:: GetSd**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity:: SetD**](--systemsecurity-setsd.md)
</dt> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Sicurezza degli spazi dei nomi WMI](securing-wmi-namespaces.md)
</dt> <dt>

Costanti di sicurezza WMI
</dt> </dl>

 

