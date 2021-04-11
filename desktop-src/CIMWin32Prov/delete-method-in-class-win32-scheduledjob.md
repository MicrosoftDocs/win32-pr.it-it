---
description: Il&Delete \# 8194; Il metodo della classe WMI Elimina un processo pianificato.
ms.assetid: 064ff3f8-6d41-4f8d-a511-6c051bb48a5b
ms.tgt_platform: multiple
title: Metodo Delete della classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd375c3da85bd72bddfc97ed3f57e52103578441
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127759"
---
# <a name="delete-method-of-the-win32_scheduledjob-class"></a>Metodo Delete della classe Win32 \_ ScheduledJob

Il metodo **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) Elimina un processo pianificato.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione completata**
</dt> <dd>

0

La richiesta è stata accettata.

</dd> <dt>

**Non supportato**
</dt> <dd>

1

La richiesta non è supportata.

</dd> <dt>

**Accesso negato**
</dt> <dd>

2

L'utente non dispone dell'accesso necessario.

</dd> <dt>

**Errore sconosciuto**
</dt> <dd>

8

Processo interattivo.

</dd> <dt>

**Impossibile trovare il percorso**
</dt> <dd>

9

Impossibile trovare il percorso di directory del file eseguibile del servizio.

</dd> <dt>

**Parametro non valido**
</dt> <dd>

21

Sono stati passati parametri non validi al servizio.

</dd> <dt>

**Servizio non avviato**
</dt> <dd>

22

L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.

</dd> <dt>

**Altri**
</dt> <dd>

23 4294967295

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

[**\_ScheduledJob Win32**](win32-scheduledjob.md)
</dt> </dl>

 

