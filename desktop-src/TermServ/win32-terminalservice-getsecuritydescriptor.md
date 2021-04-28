---
title: Metodo GetSecurityDescriptor della classe Win32_Service (Servizi Desktop remoto)
description: "Metodo GetSecurityDescriptor della classe Win32_Service (Servizi Desktop remoto): restituisce il descrittore di sicurezza che controlla l'accesso al servizio."
ms.assetid: 9898091A-5BE2-42A0-BF81-13AB74696ACB
ms.tgt_platform: multiple
keywords:
- scripting Strumentazione gestione Windows , sicurezza
- sicurezza Strumentazione gestione Windows , scripting
- Metodo GetSecurityDescriptor Servizi Desktop remoto
- Il metodo GetSecurityDescriptor Servizi Desktop remoto , Win32_Service classe
- Win32_Service classe Servizi Desktop remoto, metodo GetSecurityDescriptor
topic_type:
- apiref
api_name:
- Win32_Service.GetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5b8a9b945048f947aa273e1ccc1f4514469681
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090649"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a>Metodo GetSecurityDescriptor della classe Win32_Service (Servizi Desktop remoto)

Il **metodo GetSecurityDescriptor** restituisce il descrittore di sicurezza che controlla l'accesso al servizio. Il descrittore viene restituito come istanza di [**Win32 \_ SecurityDescriptor.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

## <a name="syntax"></a>Sintassi


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Descrittore* \[ Cambio\]
</dt> <dd>

Descrittore di sicurezza associato al servizio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore. Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**0**
</dt> <dd>

La richiesta è stata accettata.

</dd> <dt>

**1**
</dt> <dd>

La richiesta non è supportata.

</dd> <dt>

**2**
</dt> <dd>

L'utente non aveva l'accesso necessario.

</dd> <dt>

**3**
</dt> <dd>

Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.

</dd> <dt>

**4**
</dt> <dd>

Il codice di controllo richiesto non è valido o non è accettabile per il servizio.

</dd> <dt>

**5**
</dt> <dd>

Il codice di controllo richiesto non può essere inviato al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State)** è uguale a 0, 1 o 2.

</dd> <dt>

**6**
</dt> <dd>

Il servizio non è stato avviato.

</dd> <dt>

**7**
</dt> <dd>

Il servizio non ha risposto in tempo utile alla richiesta di avvio.

</dd> <dt>

**8**
</dt> <dd>

Errore sconosciuto durante l'avvio del servizio.

</dd> <dt>

**9**
</dt> <dd>

Impossibile trovare il percorso della directory del file eseguibile del servizio.

</dd> <dt>

**10**
</dt> <dd>

Il servizio è già in esecuzione.

</dd> <dt>

**11**
</dt> <dd>

Il database a cui aggiungere il nuovo servizio è bloccato.

</dd> <dt>

**12**
</dt> <dd>

Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.

</dd> <dt>

**13**
</dt> <dd>

Impossibile trovare un servizio dipendente necessario.

</dd> <dt>

**14**
</dt> <dd>

Il servizio è stato disabilitato dal sistema.

</dd> <dt>

**15**
</dt> <dd>

Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.

</dd> <dt>

**16**
</dt> <dd>

Questo servizio viene rimosso dal sistema.

</dd> <dt>

**17**
</dt> <dd>

Il servizio non ha thread di esecuzione.

</dd> <dt>

**18**
</dt> <dd>

Il servizio ha dipendenze circolari all'avvio.

</dd> <dt>

**19**
</dt> <dd>

Un servizio è in esecuzione con lo stesso nome.

</dd> <dt>

**20**
</dt> <dd>

Il nome del servizio contiene caratteri non validi.

</dd> <dt>

**21**
</dt> <dd>

Al servizio sono stati passati parametri non validi.

</dd> <dt>

**22**
</dt> <dd>

L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.

</dd> <dt>

**23**
</dt> <dd>

Il servizio esiste già nel database dei servizi disponibili dal sistema.

</dd> <dt>

**24**
</dt> <dd>

Il servizio è attualmente sospeso nel sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

[**L'istanza \_ di Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di accesso discrezionale (DACL) e un elenco di controllo di accesso [*di*](/windows/desktop/SecGloss/s-gly) sistema (SACL). [](/windows/desktop/SecGloss/d-gly) Per altre informazioni, vedere [Elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).

Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL. Per altre informazioni, vedere [**Costanti dei privilegi**](/windows/desktop/WmiSdk/privilege-constants) ed Esecuzione di operazioni con [privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Esempio

Quando si recupera un descrittore di sicurezza in VBScript, assicurarsi di "Sicurezza" ed eseguire come Amministratore, come illustrato nel frammento di codice seguente. In caso contrario, il codice potrebbe generare un errore di autorizzazione.


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



Analogamente, in VB.NET assicurarsi di impostare "EnablePrivileges = True" ed eseguire l'applicazione come amministratore.


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Servizio \_ Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[**Costanti privilege**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Oggetti descrittore di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Modifica della sicurezza dell'accesso per gli oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

