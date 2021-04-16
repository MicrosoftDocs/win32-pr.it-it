---
description: Il&di priorità \# 32; Il metodo della classe WMI tenta di modificare la priorità di esecuzione del processo.
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: Metodo di priorità della classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.SetPriority
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf08057ec075448d9912e37c33b6087c381f97d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524145"
---
# <a name="setpriority-method-of-the-win32_process-class"></a>Metodo di priorità della classe di \_ processo Win32

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) di **priorità** tenta di modificare la priorità di esecuzione del processo.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Priorità* \[ di in\]
</dt> <dd>

Nuova classe di priorità per il processo. Si noti che questi valori sono diversi da quelli indicati in modo esplicito nella proprietà **Priority** del [**\_ processo Win32**](win32-process.md).

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inattività** (64)


</dt> <dd>

Specificata per un processo con thread eseguiti solo quando il sistema è inattivo. I thread del processo vengono interrotti dai thread di un processo eseguito in una classe di priorità superiore, ad esempio, un screen saver. La classe di priorità inattiva viene ereditata dai processi figlio.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Inferiore al normale** (16384)


</dt> <dd>

Indica un processo con priorità superiore alla **\_ \_ classe di priorità di inattività**, ma al di sotto della **\_ \_ classe di priorità normale**.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** (32)


</dt> <dd>

Specificato per un processo senza particolari esigenze di pianificazione.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Superiore al normale** (32768)


</dt> <dd>

Indica un processo con priorità superiore alla **\_ \_ classe di priorità normale**, ma al di sotto della **\_ \_ classe con priorità alta**.

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Priorità alta** (128)


</dt> <dd>

Specificato per un processo che esegue attività critiche al tempo che devono essere eseguite immediatamente. I thread del processo hanno la precedenza sui thread dei processi con classe di priorità normal o idle. Un esempio è il Elenco attività, che deve rispondere rapidamente quando viene chiamato dall'utente, indipendentemente dal carico sul sistema operativo. Prestare particolare attenzione quando si utilizza la classe con priorità alta, perché un'applicazione di classe con priorità alta può utilizzare quasi tutto il tempo di CPU disponibile.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tempo reale** (256)


</dt> <dd>

Specificato per un processo con la massima priorità possibile. I thread del processo hanno la precedenza sui thread di tutti gli altri processi, inclusi i processi del sistema operativo che eseguono attività importanti. Ad esempio, un processo in tempo reale che viene eseguito per più di un intervallo molto breve può causare la mancata scaricamento delle cache del disco o la mancata risposta del mouse.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Completamento** completato (0)
</dt> <dt>

**Accesso negato** (2)
</dt> <dt>

**Privilegio insufficiente** (3)
</dt> <dt>

**Errore sconosciuto** (8)
</dt> <dt>

**Percorso non trovato** (9)
</dt> <dt>

**Parametro non valido** (21)
</dt> <dt>

**Altro** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

Per impostare la priorità su realtime, il chiamante deve disporre del privilegio di priorità di base **SeIncreaseBasePriorityPrivilege** (**se \_ Inc \_ \_ \_**). Senza questo privilegio, la priorità più alta può essere impostata su è alta.

## <a name="examples"></a>Esempio

L'esempio di [modifica della priorità di un processo in esecuzione](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript modifica la priorità di un'istanza in esecuzione di Notepad.exe da normale a superiore al normale.

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

 

