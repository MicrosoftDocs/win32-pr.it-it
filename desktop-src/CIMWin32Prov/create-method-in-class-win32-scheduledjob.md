---
description: Invia un processo a un sistema operativo per l'esecuzione a una data e ora specificate in futuro.
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
ms.openlocfilehash: 9f1acae94ea29d2d57b2952c0b0adc267ad3066c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342351"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a>Metodo Create della classe Win32 \_ ScheduledJob

Il metodo **Crea** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) Invia un processo a un sistema operativo per l'esecuzione a una data e ora specificate in futuro. Questo metodo richiede che il servizio Schedule venga avviato nel computer a cui viene inviato il processo.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

*Comando* \[ in\]
</dt> <dd>

Nome del comando, del programma batch o dei parametri del file binario e della riga di comando utilizzati dal servizio Schedule per richiamare il processo.

Esempio: "Defrag/q/f".

</dd> <dt>

*StartTime* \[ in\]
</dt> <dd>

Ora UTC (Coordinated Universal Time) per l'esecuzione di un processo. Il formato deve essere: "ad aaaammgghhmmss. MMMMMM (+-) OOO ", dove" AAAAMMGG "deve essere sostituito da" \* \* \* \* \* \* \* \* ". Ad esempio: " \* \* \* \* \* \* \* \* 143000.000000-420" specifica 14,30 (2:30) PST con ora legale in vigore.

La sezione "(+-) OOO" del valore della proprietà StartTime è la distorsione corrente per la conversione dell'ora locale. La distorsione è la differenza tra l'ora UTC e l'ora locale. Per calcolare la distorsione per il fuso orario, moltiplicare il numero di ore per cui il fuso orario è in anticipo o dietro la ora di Greenwich (GMT) di 60 (usare un numero positivo per il numero di ore se il fuso orario è preceduto da GMT e un numero negativo se il fuso orario è dietro GMT). Aggiungere un ulteriore 60 al calcolo se il fuso orario USA l'ora legale. Ad esempio, il fuso orario Pacifico standard è di otto ore dietro GMT, quindi la distorsione è uguale a-420 (-8 \* 60 + 60) quando l'ora legale è in uso e-480 (-8 \* 60) quando l'ora legale non è in uso. È anche possibile determinare il valore della distorsione eseguendo una query sulla proprietà bias della classe [**del \_ fuso orario Win32**](win32-timezone.md) .

</dd> <dt>

*RunRepeatedly* \[ in, facoltativo\]
</dt> <dd>

Se **true**, un processo pianificato viene eseguito ripetutamente in giorni specifici. Il valore predefinito è **False**.

</dd> <dt>

*DaysOfWeek* \[ in, facoltativo\]
</dt> <dd>

Giorni della settimana in cui è pianificata l'esecuzione di un processo; utilizzato solo quando il parametro *RunRepeatedly* è **true**. Per pianificare un processo per più di un giorno della settimana, unire i valori appropriati in un operatore OR logico. Per pianificare un processo per martedì e venerdì, ad esempio, il valore di *DaysOfWeek* è 2 o 16.

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

**Giovedi** (8)


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

Giorni del mese in cui è pianificata l'esecuzione di un processo; utilizzato solo quando il parametro *RunRepeatedly* è **true**.

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1)


</dt> <dd>

Primo giorno del mese

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

Giorno 11 del mese

</dd> <dt>

<span id="12"></span>

<span id="12"></span>**12** (2048)


</dt> <dd>

Giorno 12 di un mese

</dd> <dt>

<span id="13"></span>

<span id="13"></span>**13** (4096)


</dt> <dd>

Giorno 13 del mese

</dd> <dt>

<span id="14"></span>

<span id="14"></span>**14** (8192)


</dt> <dd>

Giorno 14 di un mese

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384)


</dt> <dd>

Giorno 15 del mese

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768)


</dt> <dd>

Giorno 16 di un mese

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536)


</dt> <dd>

Giorno 17 del mese

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

Giorno 25 del mese

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432)


</dt> <dd>

Giorno 26 di un mese

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864)


</dt> <dd>

Giorno 27 del mese

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728)


</dt> <dd>

Giorno 28 del mese

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456)


</dt> <dd>

29 giorni di un mese

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

Se **true**, il processo specificato deve essere interattivo, il che significa che un utente può fornire l'input a un processo pianificato mentre il processo è in esecuzione. Il valore predefinito è **False**.

</dd> <dt>

*JobID* \[ out\]
</dt> <dd>

Identificatore del numero di un processo. Questo parametro è un handle per un processo pianificato in un computer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) quando ha esito positivo e un numero diverso per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

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

## <a name="remarks"></a>Commenti

Se il processo pianificato avvia un programma interattivo, ad esempio Blocco note, la proprietà **InteractWithDeskto** deve essere impostata su **true** o la schermata del programma non è visibile. Il processo viene comunque visualizzato in **Gestione attività** anche se non viene visualizzato sullo schermo.

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

 

