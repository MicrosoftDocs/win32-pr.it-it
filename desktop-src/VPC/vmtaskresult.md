---
title: Enumerazione VMTaskResult (VPCCOMInterfaces.h)
description: Specifica il risultato di un'attività.
ms.assetid: 34aa193a-466d-492e-8648-467c286a8c11
keywords:
- Enumerazione VMTaskResult Virtual PC
topic_type:
- apiref
api_name:
- VMTaskResult
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0884d89776ac840586f221f21f8335f1d93c18886fd36bbe790164ebd1ba4cd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998441"
---
# <a name="vmtaskresult-enumeration"></a>Enumerazione VMTaskResult

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Specifica il risultato di un'attività.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  vmTaskResult_Success                      = 0,
  vmTaskResult_Cancelled                    = 1,
  vmTaskResult_UnexpectedError              = 2,
  vmTaskResult_OutOfMemoryError             = 3,
  vmTaskResult_DiskRelatedError             = 4,
  vmTaskResult_IncompatibleSavedStateError  = 5,
  vmTaskResult_TimeOutError                 = 6,
  vmTaskResult_IllegalValueError            = 7,
  vmTaskResult_ThreadCrashError             = 8,
  vmTaskResult_ShutdownAbort                = 9
} VMTaskResult;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmTaskResult \_ Success**
</dt> <dd>

L'attività è stata completata.

</dd> <dt>

<span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmTaskResult \_ Cancelled**
</dt> <dd>

L'attività è stata annullata.

</dd> <dt>

<span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmTaskResult \_ UnexpectedError**
</dt> <dd>

Errore imprevisto dell'attività.

</dd> <dt>

<span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmTaskResult \_ OutOfMemoryError**
</dt> <dd>

Memoria insufficiente per il completamento dell'attività.

</dd> <dt>

<span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmTaskResult \_ DiskRelatedError**
</dt> <dd>

Si è verificato un errore dell'attività durante la scrittura su disco (assicurarsi che lo spazio su disco sia sufficiente).

</dd> <dt>

<span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmTaskResult \_ IncompatibleSavedStateError**
</dt> <dd>

La macchina virtuale non è stata ripristinata perché lo stato salvato era incompatibile.

</dd> <dt>

<span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**VmTaskResult \_ TimeOutError**
</dt> <dd>

Timeout dell'attività.

</dd> <dt>

<span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmTaskResult \_ IllegalValueError**
</dt> <dd>

È stato letto un valore di preferenza non valido durante l'elaborazione dell'attività.

</dd> <dt>

<span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**VmTaskResult \_ ThreadCrashError**
</dt> <dd>

Un thread associato all'attività si è arrestato in modo anomalo.

</dd> <dt>

<span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmTaskResult \_ ShutdownAbort**
</dt> <dd>

L'arresto richiesto è stato interrotto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMTask::Result**](ivmtask-result.md)
</dt> </dl>

 

