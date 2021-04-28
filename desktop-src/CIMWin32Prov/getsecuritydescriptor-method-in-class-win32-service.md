---
description: "Metodo GetSecurityDescriptor della classe Win32_Service (provider WMI CIMWin32): restituisce il descrittore di sicurezza che controlla l'accesso al servizio."
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: Metodo GetSecurityDescriptor della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c19f22cf57a811a7caebfbcc9bf4202c8d2ad7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096989"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Metodo GetSecurityDescriptor della classe Win32_Service (provider WMI CIMWin32)

Il **metodo GetSecurityDescriptor** restituisce il descrittore di sicurezza che controlla l'accesso al servizio. Il descrittore viene restituito come istanza di [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

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

Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore. Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Success**
</dt> <dd>

0

La richiesta è stata accettata.

</dd> <dt>


</dt> <dd>

1

La richiesta non è supportata.

</dd> <dt>

**Accesso negato**
</dt> <dd>

2

L'utente non dispone dell'accesso necessario.

</dd> <dt>


</dt> <dd>

3

Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.

</dd> <dt>


</dt> <dd>

4

Il codice di controllo richiesto non è valido o non è accettabile per il servizio.

</dd> <dt>


</dt> <dd>

5

Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** ) è uguale a 0, 1 o 2.

</dd> <dt>


</dt> <dd>

6

Il servizio non è stato avviato.

</dd> <dt>


</dt> <dd>

7

Il servizio non ha risposto in tempo utile alla richiesta di avvio.

</dd> <dt>

**Errore sconosciuto**
</dt> <dd>

8

Errore sconosciuto durante l'avvio del servizio.

</dd> <dt>

**Privilegio mancante**
</dt> <dd>

9

Impossibile trovare il percorso della directory del file eseguibile del servizio.

</dd> <dt>


</dt> <dd>

10

Il servizio è già in esecuzione.

</dd> <dt>


</dt> <dd>

11

Il database a cui aggiungere il nuovo servizio è bloccato.

</dd> <dt>


</dt> <dd>

12

Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.

</dd> <dt>


</dt> <dd>

13

Impossibile trovare un servizio dipendente necessario.

</dd> <dt>


</dt> <dd>

14

Il servizio è stato disabilitato dal sistema.

</dd> <dt>


</dt> <dd>

15

Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.

</dd> <dt>


</dt> <dd>

16

Questo servizio viene rimosso dal sistema.

</dd> <dt>


</dt> <dd>

17

Il servizio non ha thread di esecuzione.

</dd> <dt>


</dt> <dd>

18

Il servizio ha dipendenze circolari all'avvio.

</dd> <dt>


</dt> <dd>

19

Un servizio è in esecuzione con lo stesso nome.

</dd> <dt>


</dt> <dd>

20

Il nome del servizio contiene caratteri non validi.

</dd> <dt>

**Parametro non valido**
</dt> <dd>

21

Al servizio sono stati passati parametri non validi.

</dd> <dt>


</dt> <dd>

22

L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.

</dd> <dt>


</dt> <dd>

23

Il servizio esiste già nel database dei servizi disponibili dal sistema.

</dd> <dt>


</dt> <dd>

24

Il servizio è attualmente sospeso nel sistema.

</dd> <dt>

**Altri**
</dt> <dd>

22 4294967295

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
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Servizio \_ Win32**](win32-service.md)
</dt> <dt>

[**Costanti dei privilegi**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Oggetti descrittori di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Modifica della sicurezza degli accessi per gli oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

