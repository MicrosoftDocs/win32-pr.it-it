---
description: SetPriority&\# 32; Il metodo della classe WMI tenta di modificare la priorità di esecuzione del processo.
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: Metodo SetPriority della Win32_Process classe
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
ms.openlocfilehash: decd5892d480e4f236ae9d7acdc1a25c018557166535c963eb35dc3f6f62ffa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675570"
---
# <a name="setpriority-method-of-the-win32_process-class"></a>Metodo SetPriority della classe Process \_ Win32

Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPriority** tenta di modificare la priorità di esecuzione del processo.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Priorità* \[ Pollici\]
</dt> <dd>

Nuova classe di priorità per il processo. Si noti che questi valori sono diversi da quelli indicati in modo esplicito nella **proprietà Priority** del [**processo Win32. \_**](win32-process.md)

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inattivo** (64)


</dt> <dd>

Specificato per un processo con thread eseguiti solo quando il sistema è inattivo. I thread del processo vengono seguiti dai thread di un processo in esecuzione in una classe con priorità più alta, ad esempio un screen saver. La classe con priorità di inattività viene ereditata dai processi figlio.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Sotto normale** (16384)


</dt> <dd>

Indica un processo con priorità superiore a **IDLE \_ PRIORITY \_ CLASS,** ma inferiore a **NORMAL PRIORITY \_ \_ CLASS.**

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** (32)


</dt> <dd>

Specificato per un processo senza esigenze di pianificazione speciali.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Sopra normale** (32768)


</dt> <dd>

Indica un processo con priorità superiore a **NORMAL \_ PRIORITY \_ CLASS,** ma inferiore **a HIGH PRIORITY \_ \_ CLASS.**

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Priorità alta** (128)


</dt> <dd>

Specificato per un processo che esegue attività di importanza critica che devono essere eseguite immediatamente. I thread del processo hanno la precedenza sui thread dei processi con classe di priorità normal o idle. Un esempio è il Elenco attività, che deve rispondere rapidamente quando viene chiamato dall'utente, indipendentemente dal carico sul sistema operativo. Usare estrema attenzione quando si usa la classe ad alta priorità, perché un'applicazione di classe ad alta priorità può usare quasi tutto il tempo di CPU disponibile.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tempo reale** (256)


</dt> <dd>

Specificato per un processo con la priorità più alta possibile. I thread del processo hanno la priorità su tutti gli altri processi, inclusi i processi del sistema operativo che eseguono attività importanti. Ad esempio, un processo in tempo reale che viene eseguito per più di un intervallo molto breve può causare la non scaricamento delle cache del disco o il fatto che un mouse non rispetti.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore. Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Completamento riuscito** (0)
</dt> <dt>

**Accesso negato** (2)
</dt> <dt>

**Privilegi insufficienti** (3)
</dt> <dt>

**Errore sconosciuto** (8)
</dt> <dt>

**Percorso non trovato** (9)
</dt> <dt>

**Parametro non** valido (21)
</dt> <dt>

**Altro** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

Per impostare la priorità su Realtime, il chiamante deve avere **SeIncreaseBasePriorityPrivilege** (**edizione Standard INC BASE PRIORITY \_ \_ \_ \_ PRIVILEGE**). Senza questo privilegio, la priorità più alta può essere impostata su Priorità alta.

## <a name="examples"></a>Esempio

[L'esempio Modify the Priority Of a Running Process](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript modifica la priorità di un'istanza in Notepad.exe da Normale a Sopra normale.

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

 

