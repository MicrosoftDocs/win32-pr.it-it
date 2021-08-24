---
description: Ottiene il descrittore di sicurezza che controlla chi può avviare un'applicazione DCOM.
ms.assetid: ba02807f-aa2a-4b1c-9692-2803d93cd2ee
ms.tgt_platform: multiple
title: Metodo GetLaunchSecurityDescriptor della classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.GetLaunchSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b76a37db5b1edbc230c4cc4aed712ef4eee9dd4221cc4cb85fb8f205db69d35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878951"
---
# <a name="getlaunchsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a>Metodo GetLaunchSecurityDescriptor della classe \_ DCOMApplicationSetting Win32

Il **metodo WMI GetLaunchSecurityDescriptor** ottiene il descrittore di sicurezza che controlla chi può avviare un'applicazione DCOM. Il descrittore di sicurezza è un'istanza della [**classe \_ SecurityDescriptor Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) L'account che esegue lo script o l'applicazione che chiama questo metodo deve avere i privilegi **SeSecurityPrivilege** e **SeRestorePrivilege.** Per altre informazioni, vedere [Modifica della sicurezza degli accessi in oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetLaunchSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Descrittore* \[ Cambio\]
</dt> <dd>

Descrittore di sicurezza da impostare che controlla chi può avviare l'applicazione DCOM.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore. Per altre informazioni, vedere [Codici restituiti WMI](/windows/desktop/WmiSdk/wmi-return-codes) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)

<dl> <dt>

**Success**
</dt> <dd>

0

Completamento.

</dd> <dt>

**2**
</dt> <dd>

L'utente non ha accesso alle informazioni richieste.

</dd> <dt>

**8**
</dt> <dd>

Errore sconosciuto.

</dd> <dt>

**9**
</dt> <dd>

L'utente non dispone di privilegi adeguati per eseguire il metodo .

</dd> <dt>

**21**
</dt> <dd>

Un parametro specificato nella chiamata al metodo non è valido.

</dd> <dt>

**Altri**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Commenti

[**L'istanza \_ di Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di accesso discrezionale (DACL) e un elenco di controllo di accesso [*di*](/windows/desktop/SecGloss/s-gly) sistema (SACL). [](/windows/desktop/SecGloss/d-gly) Per altre informazioni, vedere [Elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).

Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL. Per altre informazioni, vedere [**Costanti dei privilegi**](/windows/desktop/WmiSdk/privilege-constants) ed Esecuzione di operazioni con [privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ DCOMApplicationSetting**](win32-dcomapplicationsetting.md)
</dt> <dt>

[**Costanti dei privilegi**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Oggetti descrittori di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Modifica della sicurezza degli accessi per gli oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

