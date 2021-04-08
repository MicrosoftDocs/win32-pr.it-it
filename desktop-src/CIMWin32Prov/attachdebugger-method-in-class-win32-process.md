---
description: Avvia il debugger attualmente registrato per questo processo.
ms.assetid: 63c30db8-6117-4353-9132-4f39c72a6637
ms.tgt_platform: multiple
title: Metodo AttachDebugger della classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.AttachDebugger
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 041bdeeab634ebed5c7ec2eccffe01f7cecce709
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877413"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a>Metodo AttachDebugger della classe di \_ processo Win32

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AttachDebugger** avvia il debugger attualmente registrato per questo processo.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione completata**
</dt> <dd>

0

Operazione completata.

</dd> <dt>

**Accesso negato**
</dt> <dd>

2

L'utente non ha accesso alle informazioni richieste.

</dd> <dt>

**Privilegio insufficiente**
</dt> <dd>

3

L'utente non dispone di privilegi sufficienti.

</dd> <dt>

**Errore sconosciuto**
</dt> <dd>

8

Errore sconosciuto.

</dd> <dt>

**Impossibile trovare il percorso**
</dt> <dd>

9

Il percorso specificato non esiste.

</dd> <dt>

**Parametro non valido**
</dt> <dd>

21

Il parametro specificato non è valido.

</dd> <dt>

**Altri**
</dt> <dd>

22 4294967295

</dd> </dl>

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

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Processo Win32**](win32-process.md)
</dt> </dl>

 

