---
description: Il metodo Win32ShutdownTracker fornisce lo stesso set di opzioni di arresto supportate dal metodo Win32Shutdown in Win32 OperatingSystem, ma consente anche di specificare commenti, un motivo per l'arresto o un \_ timeout.
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Metodo Win32ShutdownTracker della Win32_OperatingSystem classe
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
ms.openlocfilehash: 58c83e90f5256b2b2abb681048678b7c3bb4df3e9c4f4cdade16cb9ea00c4e48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079525"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a>Metodo Win32ShutdownTracker della classe OperatingSystem Win32 \_

Il **metodo Win32ShutdownTracker** fornisce lo stesso set di opzioni di arresto supportate dal metodo [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) in [**Win32 \_ OperatingSystem,**](win32-operatingsystem.md)ma consente anche di specificare commenti, un motivo per l'arresto o un timeout.

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

*Timeout* \[ Pollici\]
</dt> <dd>

Tempo, in secondi, prima dell'arresto. Il valore predefinito è 0 (zero).

</dd> <dt>

*Commento* \[ Pollici\]
</dt> <dd>

Messaggio da visualizzare nella finestra di dialogo di arresto archiviata anche come commento nella voce del registro eventi.

</dd> <dt>

*Codice motivo* \[ Pollici\]
</dt> <dd>

Motivo dell'avvio dell'arresto.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Set di flag bitmap per arrestare il computer. Per forzare un comando, aggiungere il flag Force (4) al valore del comando. L'uso di Forza in combinazione con Arresta o Riavvia in un computer remoto arresta immediatamente tutti gli elementi (inclusi WMI, COM e così via) o riavvia il computer remoto. Il risultato è un valore restituito indeterminato.

<dt>

0 (0x0)
</dt> <dd>

Disconiti

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

Interruzione dell'alimentazione

</dd> <dt>

12 (0xC)
</dt> <dd>

Alimentazione forzata (8 + 4)

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per i codici di errore, [**vedere Costanti di errore WMI**](../wmisdk/wmi-error-constants.md) o [**WbemErrorEnum.**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](../debug/system-error-codes.md)

<dl> <dt>

**Operazione** riuscita (0)
</dt> <dt>

**Altro** (1-4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

Il processo chiamante deve avere il **edizione Standard \_ SHUTDOWN \_ NAME.**

## <a name="examples"></a>Esempio

L'esempio di codice VBScript seguente descrive come chiamare **Win32ShutdownTracker.**


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
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> <dt>

[**Sistema operativo \_ Win32**](win32-operatingsystem.md)
</dt> <dt>

[**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
