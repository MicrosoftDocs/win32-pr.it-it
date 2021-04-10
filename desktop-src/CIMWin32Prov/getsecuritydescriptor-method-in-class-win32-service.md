---
description: Restituisce il descrittore di sicurezza che controlla l'accesso al servizio.
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
ms.openlocfilehash: 5bf8dee49893a5a1d3b628e72b0b0746a6215fb0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049151"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Metodo GetSecurityDescriptor della classe Win32_Service (provider WMI CIMWin32)

Il metodo **GetSecurityDescriptor** restituisce il descrittore di sicurezza che controlla l'accesso al servizio. Il descrittore viene restituito come un'istanza di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Descrittore* \[ out\]
</dt> <dd>

Descrittore di sicurezza associato al servizio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

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

Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.

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

Impossibile trovare il percorso di directory del file eseguibile del servizio.

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

Questo servizio verrà rimosso dal sistema.

</dd> <dt>


</dt> <dd>

17

Il servizio non dispone di un thread di esecuzione.

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

Sono stati passati parametri non validi al servizio.

</dd> <dt>


</dt> <dd>

22

L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.

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

L' [**istanza Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati di [**\_ \_ controllo del descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) e un elenco di controllo di accesso di [*sistema*](/windows/desktop/SecGloss/s-gly) (SACL). Per altre informazioni, vedere [elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).

Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL. Per altre informazioni, vedere [**costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants) ed [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Esempio

Quando si recupera un descrittore di sicurezza in VBScript, assicurarsi di "sicurezza" ed eseguire come amministratore, come illustrato nel frammento di codice seguente. In caso contrario, il codice potrebbe generare un errore di autorizzazione.


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



Analogamente, in VB.NET, assicurarsi di impostare "EnablePrivileges = true" ed eseguire l'applicazione come amministratore.


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
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Servizio Win32**](win32-service.md)
</dt> <dt>

[**Costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Oggetti descrittore di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Modifica della sicurezza di accesso per gli oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

