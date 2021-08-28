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
ms.openlocfilehash: 86ec5e31afef484733381d94bfdfa48595401d963443c2ab407ee6166d5d0f4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959170"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a>Metodo AttachDebugger della classe Win32 \_ Process

Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AttachDebugger** avvia il debugger attualmente registrato per questo processo.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione completata**
</dt> <dd>

0

Completamento.

</dd> <dt>

**Accesso negato**
</dt> <dd>

2

L'utente non ha accesso alle informazioni richieste.

</dd> <dt>

**Privilegi insufficienti**
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
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Processo \_ Win32**](win32-process.md)
</dt> </dl>

 

