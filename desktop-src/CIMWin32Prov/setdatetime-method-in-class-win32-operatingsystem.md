---
description: Valore DateTime&\# 8194; Il metodo della classe WMI imposta l'ora di sistema corrente nel computer.
ms.assetid: b9b86a52-c3d7-489d-8632-b297970dbeac
ms.tgt_platform: multiple
title: Metodo sedatetime della classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.SetDateTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60316904d58ffec38aa912a1454082e7edfae5a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304513"
---
# <a name="setdatetime-method-of-the-win32_operatingsystem-class"></a>Metodo sedatetime della classe Win32 \_ OperatingSystem

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DateTime** imposta l'ora di sistema corrente nel computer.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetDateTime(
  [in] datetime LocalDatetime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LocalDatetime* \[ in\]
</dt> <dd>

Valore dell'ora corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per i codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione riuscita** (0)
</dt> <dt>

**Altro** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

Il processo chiamante deve avere il \_ privilegio di \_ nome SYSTEMTIME.

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

[**\_OperatingSystem Win32**](win32-operatingsystem.md)
</dt> <dt>

[Attività WMI: gestione desktop](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

