---
description: Invia un processo a un sistema operativo per l'esecuzione in un'ora e in una data specificate in futuro.
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Metodo Create della classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a7788c894646b3ebb07fc9d3d98aeeda54b9172b5dde01e7eb65975bb2d95d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547411"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a>Metodo Create della classe ScheduledJob Win32 \_

Il **metodo** [Crea classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) invia un processo a un sistema operativo per l'esecuzione a un'ora e a una data specificate in futuro. Questo metodo richiede che il servizio di pianificazione sia avviato nel computer a cui viene inviato il processo.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Create(
  [in]           string   Command,
  [in]           datetime StartTime,
  [in, optional] boolean  RunRepeatedly,
  [in, optional] uint32   DaysOfWeek,
  [in, optional] uint32   DaysOfMonth,
  [in, optional] boolean  InteractWithDesktop,
  [out]          uint32   JobId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Comando* \[ Pollici\]
</dt> <dd>

Nome del comando, del programma batch o del file binario e dei parametri della riga di comando utilizzati dal servizio di pianificazione per richiamare il processo.

Esempio: "defrag /q /f".

</dd> <dt>

*StartTime* \[ Pollici\]
</dt> <dd>

Coordinated Universal Time (UTC) per l'esecuzione di un processo. Il formato deve essere: "AAAAMMGGHHMMSS. MMMMMM(+-)OOO", dove "AAAAMMGG" deve essere sostituito da " \* \* \* \* \* \* \* \* ". Ad esempio: " \* \* \* \* \* \* \* \* 143000.000000-420" specifica 14.30 (2:30 P.M.) PST con ora legale in vigore.

La sezione "(+-)OOO" del valore della proprietà StartTime è la distorsione corrente per la conversione dell'ora locale. La differenza è la differenza tra l'ora UTC e l'ora locale. Per calcolare la distorsione per il fuso orario, moltiplicare il numero di ore in cui il fuso orario è avanti o indietro rispetto all'ora di Greenwich (GMT) per 60 (usare un numero positivo per il numero di ore se il fuso orario è superiore a GMT e un numero negativo se il fuso orario è indietro rispetto a GMT). Aggiungere altri 60 al calcolo se il fuso orario usa l'ora legale. Ad esempio, il fuso orario standard del Pacifico è otto ore indietro rispetto a GMT, pertanto la deviazione è uguale a -420 (-8 60 + 60) quando è in uso l'ora legale e \* -480 (-8 60) quando l'ora legale non è \* in uso. È anche possibile determinare il valore della distorsione tramite una query sulla proprietà bias della [**classe \_ TimeZone Win32.**](win32-timezone.md)

</dd> <dt>

*RunRepeatedly* \[ in, facoltativo\]
</dt> <dd>

Se **True,** un processo pianificato viene eseguito ripetutamente in giorni specifici. Il valore predefinito è **False**.

</dd> <dt>

*DaysOfWeek* \[ in, facoltativo\]
</dt> <dd>

Giorni della settimana in cui è pianificata l'esecuzione di un processo; usato solo quando il *parametro RunRepeatedly* è **True.** Per pianificare un processo per più di un giorno della settimana, unire i valori appropriati in un OR logico. Ad esempio, per pianificare un processo per martedì e venerdì, il valore di *DaysOfWeek* è 2 O 16.

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Lunedì** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Martedì** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Mercoledì** (4)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Giovedì** (8)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Venerdì** (16)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sabato** (32)


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Domenica** (64)


</dt> <dd></dd> </dl> </dd> <dt>

*DaysOfMonth* \[ in, facoltativo\]
</dt> <dd>

Giorni del mese in cui è pianificata l'esecuzione di un processo; usato solo quando il *parametro RunRepeatedly* è **True.**

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1)


</dt> <dd>

Giorno 1 di un mese

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2** (2)


</dt> <dd>

Giorno 2 di un mese

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3** (4)


</dt> <dd>

Giorno 3 di un mese

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4** (8)


</dt> <dd>

Giorno 4 di un mese

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5** (16)


</dt> <dd>

Giorno 5 di un mese

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6** (32)


</dt> <dd>

Giorno 6 di un mese

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7** (64)


</dt> <dd>

Giorno 7 di un mese

</dd> <dt>

<span id="8"></span>

<span id="8"></span>**8** (128)


</dt> <dd>

Giorno 8 di un mese

</dd> <dt>

<span id="9"></span>

<span id="9"></span>**9** (256)


</dt> <dd>

Giorno 9 di un mese

</dd> <dt>

<span id="10"></span>

<span id="10"></span>**10** (512)


</dt> <dd>

Giorno 10 di un mese

</dd> <dt>

<span id="11"></span>

<span id="11"></span>**11** (1024)


</dt> <dd>

Giorno 11 di un mese

</dd> <dt>

<span id="12"></span>

<span id="12"></span>**12** (2048)


</dt> <dd>

Giorno 12 di un mese

</dd> <dt>

<span id="13"></span>

<span id="13"></span>**13** (4096)


</dt> <dd>

Giorno 13 di un mese

</dd> <dt>

<span id="14"></span>

<span id="14"></span>**14** (8192)


</dt> <dd>

Giorno 14 di un mese

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384)


</dt> <dd>

Giorno 15 di un mese

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768)


</dt> <dd>

Giorno 16 di un mese

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536)


</dt> <dd>

Giorno 17 di un mese

</dd> <dt>

<span id="18"></span>

<span id="18"></span>**18** (131072)


</dt> <dd>

Giorno 18 di un mese

</dd> <dt>

<span id="19"></span>

<span id="19"></span>**19** (262144)


</dt> <dd>

Giorno 19 di un mese

</dd> <dt>

<span id="20"></span>

<span id="20"></span>**20** (524288)


</dt> <dd>

Giorno 20 di un mese

</dd> <dt>

<span id="21"></span>

<span id="21"></span>**21** (1048576)


</dt> <dd>

Giorno 21 di un mese

</dd> <dt>

<span id="22"></span>

<span id="22"></span>**22** (2097152)


</dt> <dd>

Giorno 22 di un mese

</dd> <dt>

<span id="23"></span>

<span id="23"></span>**23** (4194304)


</dt> <dd>

Giorno 23 di un mese

</dd> <dt>

<span id="24"></span>

<span id="24"></span>**24** (8388608)


</dt> <dd>

Giorno 24 di un mese

</dd> <dt>

<span id="25"></span>

<span id="25"></span>**25** (16777216)


</dt> <dd>

Giorno 25 di un mese

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432)


</dt> <dd>

Giorno 26 di un mese

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864)


</dt> <dd>

Giorno 27 di un mese

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728)


</dt> <dd>

Giorno 28 di un mese

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456)


</dt> <dd>

Giorno 29 di un mese

</dd> <dt>

<span id="30"></span>

<span id="30"></span>**30** (536870912)


</dt> <dd>

Giorno 30 di un mese

</dd> <dt>

<span id="31"></span>

<span id="31"></span>**31** (1073741824)


</dt> <dd>

Giorno 31 di un mese

</dd> </dl> </dd> <dt>

*InteractWithDesktop* \[ in, facoltativo\]
</dt> <dd>

Se **True,** il processo specificato deve essere interattivo, ovvero un utente può fornire input a un processo pianificato durante l'esecuzione del processo. Il valore predefinito è **False**.

</dd> <dt>

*JobId* \[ Cambio\]
</dt> <dd>

Numero di identificatore di un processo. Questo parametro è un handle per un processo pianificato in un computer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) in caso di esito positivo e un numero diverso per indicare un errore. Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione completata**
</dt> <dd>

0

La richiesta viene accettata.

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

Impossibile trovare il percorso della directory del file eseguibile del servizio.

</dd> <dt>

**Parametro non valido**
</dt> <dd>

21

Al servizio sono stati passati parametri non validi.

</dd> <dt>

**Servizio non avviato**
</dt> <dd>

22

L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.

</dd> <dt>

**Altri**
</dt> <dd>

23 4294967295

</dd> </dl>

## <a name="remarks"></a>Commenti

Se il processo pianificato avvia un programma interattivo, ad esempio Blocco note, la proprietà **InteractWithDeskto** deve essere impostata su **True** o la schermata del programma non è visibile. Il processo viene comunque visualizzato **Gestione attività** anche se non viene visualizzato sullo schermo.

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

[**Processo pianificato \_ Win32**](win32-scheduledjob.md)
</dt> </dl>

 

