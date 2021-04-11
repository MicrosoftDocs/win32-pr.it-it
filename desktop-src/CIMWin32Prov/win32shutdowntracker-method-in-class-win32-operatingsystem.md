---
description: Il metodo Win32ShutdownTracker fornisce lo stesso set di opzioni di arresto supportate dal metodo Win32Shutdown in Win32 \_ OperatingSystem, ma consente anche di specificare i commenti, il motivo dell'arresto o il timeout.
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Metodo Win32ShutdownTracker della classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32ShutdownTracker
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c86972d014da906b98ad8d3bd8e98d01f1cfcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126072"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a>Metodo Win32ShutdownTracker della \_ classe OperatingSystem Win32

Il metodo **Win32ShutdownTracker** fornisce lo stesso set di opzioni di arresto supportate dal metodo [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) in [**Win32 \_ OperatingSystem**](win32-operatingsystem.md), ma consente anche di specificare i commenti, il motivo dell'arresto o il timeout.

## <a name="syntax"></a>Sintassi


```mof
uint32 Win32ShutdownTracker(
  [in] uint32 Timeout,
  [in] string Comment,
  [in] uint32 ReasonCode,
  [in] sint32 Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Timeout* \[ in\]
</dt> <dd>

Tempo, in secondi, prima dell'arresto. Il valore predefinito è 0 (zero).

</dd> <dt>

*Commento* \[ in\]
</dt> <dd>

Messaggio da visualizzare nella finestra di dialogo di arresto, anch ' esso archiviato come commento nella voce del registro eventi.

</dd> <dt>

*ReasonCode* \[ in\]
</dt> <dd>

Motivo per l'avvio dell'arresto.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Set di flag bitmap per arrestare il computer. Per forzare un comando, aggiungere il flag di forzatura (4) al valore del comando. L'utilizzo di Force in combinazione con l'arresto o il riavvio di un computer remoto arresta immediatamente tutti gli elementi, inclusi WMI, COM e così via, oppure riavvia il computer remoto. Ciò comporta un valore restituito indeterminato.

<dt>

0 (0x0)
</dt> <dd>

Disconnetti

</dd> <dt>

4 (0x4)
</dt> <dd>

Disconnessione forzata (0 + 4)

</dd> <dt>

1 (0x1)
</dt> <dd>

Arresta

</dd> <dt>

5 (0x5)
</dt> <dd>

Arresto forzato (1 + 4)

</dd> <dt>

2 (0x2)
</dt> <dd>

Riavvio

</dd> <dt>

6 (0x6)
</dt> <dd>

Riavvio forzato (2 + 4)

</dd> <dt>

8 (0x8)
</dt> <dd>

Spegnimento

</dd> <dt>

12 (0xC)
</dt> <dd>

Spegnimento forzato (8 + 4)

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per i codici di errore, vedere [**costanti di errore WMI**](../wmisdk/wmi-error-constants.md) o [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](../debug/system-error-codes.md).

<dl> <dt>

**Operazione riuscita** (0)
</dt> <dt>

**Altro** (1-4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

Il processo chiamante deve avere il privilegio di **\_ arresto del \_ nome** .

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene descritto come chiamare **Win32ShutdownTracker**.


```VB
Set objArgs = Wscript.Arguments 

intTimeOut = objArgs(0) 'Countdown time (in seconds) before action
strComment = objArgs(1) 'Message to display
intFlags = objArgs(2) 'Set of flags to shutdown the computer:
'0 = Logoff, 4 = Forced Logoff (0+4), 1 = Shutdown, 2 = Reboot, 6 = Forced Reboot (2+4), 8 = Power Off, 12 = Forced Power Off (8+4) - 2 (Reboot) 

strComputer = "." 

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,(Shutdown)}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery ("Select * from Win32_OperatingSystem") 

For Each objOperatingSystem in colOperatingSystems 
objOperatingSystem.Win32ShutdownTracker intTimeOut,strComment,0,intFlags 
Next
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

[Classi del sistema operativo](./operating-system-classes.md)
</dt> <dt>

[**\_OperatingSystem Win32**](win32-operatingsystem.md)
</dt> <dt>

[**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
