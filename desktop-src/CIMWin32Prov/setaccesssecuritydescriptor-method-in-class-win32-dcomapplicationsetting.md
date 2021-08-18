---
description: Aggiorna il descrittore di sicurezza di accesso dell'applicazione DCOM con un nuovo descrittore di sicurezza definito da un'istanza di una classe \_ SecurityDescriptor Win32.
ms.assetid: 71b708ba-5eb7-400e-bee2-37ca93966c3f
ms.tgt_platform: multiple
title: Metodo SetAccessSecurityDescriptor della Win32_DCOMApplicationSetting classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetAccessSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ab668b12d6f08e205c770f4c717eda6f996971897fedb48e70702fc2d80a3c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752691"
---
# <a name="setaccesssecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a>Metodo SetAccessSecurityDescriptor della classe \_ DCOMApplicationSetting Win32

Il **metodo SetAccessSecurityDescriptor** aggiorna il descrittore di sicurezza di accesso dell'applicazione DCOM con un nuovo descrittore di sicurezza definito da un'istanza di una [**classe \_ SecurityDescriptor Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Questo descrittore di sicurezza controlla chi può accedere all'applicazione. L'account che esegue lo script o l'applicazione che chiama questo metodo deve avere i privilegi **SeSecurityPrivilege** e **SeRestorePrivilege.** Per altre informazioni, vedere [Modifica della sicurezza degli accessi per gli oggetti a protezione diretta.](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)

## <a name="syntax"></a>Sintassi


```mof
uint32 SetAccessSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Descrittore* \[ Pollici\]
</dt> <dd>

Descrittore di sicurezza da impostare per l'applicazione DCOM.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore. Per altre informazioni, vedere [Codici restituiti WMI](/windows/desktop/WmiSdk/wmi-return-codes) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)

<dl> <dt>

**Success**
</dt> <dd>

0

Operazione completata

</dd> <dt>

**2**
</dt> <dd>

L'utente non ha accesso alle informazioni richieste

</dd> <dt>

**8**
</dt> <dd>

Errore sconosciuto

</dd> <dt>

**9**
</dt> <dd>

L'utente non dispone dei privilegi adeguati per eseguire il metodo

</dd> <dt>

**21**
</dt> <dd>

Un parametro specificato nella chiamata al metodo non è valido

</dd> <dt>

**Altri**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Commenti

[**L'istanza \_ di Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di accesso discrezionale (DACL) e un elenco di controllo di accesso [*di*](/windows/desktop/SecGloss/s-gly) sistema (SACL). [](/windows/desktop/SecGloss/d-gly) Per altre informazioni, vedere Elenchi [di controllo di accesso.](/windows/desktop/SecAuthZ/access-control-lists)

Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL. Per altre informazioni, vedere [**Costanti di privilegi ed**](/windows/desktop/WmiSdk/privilege-constants) Esecuzione di operazioni con [privilegi.](/windows/desktop/WmiSdk/executing-privileged-operations)

È possibile aggiornare sia l'elenco DACL che l'elenco SACL nell'istanza [**\_ SecurityDescriptor win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) quando si chiama questo metodo, ma è anche possibile aggiornare solo l'elenco DACL o solo l'elenco SACL.

I valori seguenti in [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determinano se l'elenco DACL, l'elenco SACL o entrambi sono aggiornati.

-   **\_edizione Standard DACL \_ PRESENT**

    Indica che l'elenco DACL deve essere aggiornato. Se non è impostato, WMI mantiene il valore originale dell'elenco DACL.

-   **\_edizione Standard SACL \_ PRESENT**

    Indica che l'elenco SACL deve essere aggiornato. Se non è impostata, WMI mantiene il valore originale dell'elenco SACL. Per aggiornare l'elenco SACL, l'account deve avere il **privilegio SeSecurityPrivilege** abilitato. Per lo scripting, il nome del privilegio **è SeSecurityPrivilege.** Per altre informazioni, vedere [**Costanti di privilegio.**](/windows/desktop/WmiSdk/privilege-constants)

Se le proprietà Trustee group e Owner trustee non sono **NULL,** vengono aggiornate. In caso contrario, WMI mantiene i valori originali. Per altre informazioni, vedere [Oggetti descrittore di sicurezza WMI.](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)

Quando un nuovo SACL è **NULL** in una chiamata a questo metodo, il SACL del descrittore di sicurezza nell'oggetto a protezione diretta di destinazione rimane invariato.

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

[**Costanti privilege**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Oggetti descrittore di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Modifica della sicurezza dell'accesso per gli oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

