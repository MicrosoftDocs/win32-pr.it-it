---
description: Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso alla stampante.
ms.assetid: 6a709043-473e-4b24-8b52-6c68b670ebcf
ms.tgt_platform: multiple
title: Metodo SetSecurityDescriptor della Win32_Printer classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8621c1977c4553f610299695c2c68a72f5a9d6f2ecfcbe6df46b8646c379c2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958959"
---
# <a name="setsecuritydescriptor-method-of-the-win32_printer-class"></a>Metodo SetSecurityDescriptor della classe Printer Win32 \_

Il **metodo SetSecurityDescriptor** scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso alla stampante. Il descrittore di sicurezza è un'istanza della [**classe \_ SecurityDescriptor Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Per altre informazioni, vedere [Modifica della sicurezza degli accessi per gli oggetti a protezione diretta.](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)

In questo argomento viene Managed Object Format sintassi MOF (Managed Object Format). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Descrittore* \[ Pollici\]
</dt> <dd>

Descrittore di sicurezza associato alla stampante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore. Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**0**
</dt> <dd>

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

L'utente non dispone dei privilegi adeguati per eseguire il metodo .

</dd> <dt>

**21**
</dt> <dd>

Un parametro specificato nella chiamata al metodo non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

[**L'istanza \_ di Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di accesso discrezionale (DACL) e un elenco di controllo di accesso [*di*](/windows/desktop/SecGloss/s-gly) sistema (SACL). [](/windows/desktop/SecGloss/d-gly) Per altre informazioni, vedere Elenchi [di controllo di accesso.](/windows/desktop/SecAuthZ/access-control-lists)

Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL. Per altre informazioni, vedere [**Costanti di privilegi ed**](/windows/desktop/WmiSdk/privilege-constants) Esecuzione di operazioni con [privilegi.](/windows/desktop/WmiSdk/executing-privileged-operations)

È possibile aggiornare sia l'elenco DACL che l'elenco SACL nell'istanza [**\_ SecurityDescriptor win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) quando si chiama questo metodo, ma è anche possibile aggiornare solo l'elenco DACL o solo l'elenco SACL.

I valori seguenti in [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determinano se l'elenco DACL, l'elenco SACL o entrambi sono aggiornati.

-   **\_edizione Standard DACL \_ PRESENT**

    Indica che l'elenco DACL deve essere aggiornato. Se non è impostata, WMI mantiene il valore originale dell'elenco DACL.

-   **\_edizione Standard SACL \_ PRESENT**

    Indica che l'elenco SACL deve essere aggiornato. Se non è impostata, WMI mantiene il valore originale dell'elenco SACL. Per aggiornare l'elenco SACL, l'account deve avere il **privilegio SeSecurityPrivilege** abilitato. Per lo scripting, il nome del privilegio **è SeSecurityPrivilege.** Per altre informazioni, vedere [**Costanti privilege.**](/windows/desktop/WmiSdk/privilege-constants)

Se le proprietà Trustee group e Owner trustee non sono **NULL,** vengono aggiornate. In caso contrario, WMI mantiene i valori originali. Per altre informazioni, vedere [Oggetti descrittore di sicurezza WMI.](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)

Quando un nuovo SACL è **NULL** in una chiamata a questo metodo, il SACL del descrittore di sicurezza nell'oggetto a protezione diretta di destinazione rimane invariato.

## <a name="examples"></a>Esempio

L'esempio di PowerShell [Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) sostituisce le autorizzazioni (ACL) da una stampante a un'altra.

L'esempio di codice di PowerShell seguente descrive come impostare il descrittore di sicurezza per una stampante.


```PowerShell
# Specify the user or group
$user = "everyone"

# create instances of necessary classes
$SD = ([WMIClass] "Win32_SecurityDescriptor").CreateInstance()
$ace = ([WMIClass] "Win32_Ace").CreateInstance()
$Trustee = ([WMIClass] "Win32_Trustee").CreateInstance()

# Translate a name of user or group to SID
$SID = (new-object security.principal.ntaccount $user).translate([security.principal.securityidentifier])

# Get binary form from SID and byte Array
[byte[]] $SIDArray = ,0 * $SID.BinaryLength
$SID.GetBinaryForm($SIDArray,0)

# Fill Trustee object parameters
$Trustee.Name = $user
$Trustee.SID = $SIDArray

# Set AccessMask which can contain following values:
# Takeownership - 524288
# ReadPermissions - 131072
# ChangePermissions - 262144
# ManageDocuments - 983088
# ManagePrinters - 983052
# Print + ReadPermissions - 131080
$ace.AccessMask = 983052

# Set AceType. Can be 0 (Allow), or 1 (Deny), or 2 (System Audit)
$ace.AceType = 0
$ace.AceFlags = 0  

# Write Win32_Trustee object to Win32_Ace Trustee property
$ace.Trustee = $Trustee

# Write Win32_Ace and Win32_Trustee objects to SecurityDescriptor object
$SD.DACL = $ace

# Set SE_DACL_PRESENT control flag
$SD.ControlFlags = 0x0004

# Get printer object. For example 'CutePDF Writer' printer object
$Printer = gwmi win32_printer -filter "name = 'CutePDF Writer'"

# Enable SeSecurityPrivilege privilegies
$Printer.psbase.Scope.Options.EnablePrivileges = $true

# Invoke SetSecurityDescriptor method and write new ACE to specified
# printer ACL.
$Printer.SetSecurityDescriptor($SD)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Stampante \_ Win32**](win32-printer.md)
</dt> <dt>

[**Costanti privilege**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Oggetti descrittore di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Modifica della sicurezza dell'accesso per gli oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

