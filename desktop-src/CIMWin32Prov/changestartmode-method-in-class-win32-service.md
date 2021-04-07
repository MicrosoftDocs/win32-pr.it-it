---
description: Modifica la modalità di avvio di un \_ servizio Win32.
ms.assetid: 4fd6a1eb-d2e0-4172-843d-24ae89c5bfcf
ms.tgt_platform: multiple
title: Metodo ChangeStartMode della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06a4692996354614a685471f98b0243fc1091433
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049173"
---
# <a name="changestartmode-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Metodo ChangeStartMode della classe Win32_Service (provider WMI CIMWin32)

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica la modalità di avvio di un [**\_ servizio Win32**](win32-service.md).

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartMode* \[ in\]
</dt> <dd>

Modalità di avvio del servizio di base di Windows.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>Avvio **avvio** ("avvio")


</dt> <dd>

Driver di dispositivo avviato dal caricatore del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")


</dt> <dd>

Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Avvio automatico** ("automatico")


</dt> <dd>

Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Avvio della richiesta** ("manuale")


</dt> <dd>

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-service.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("disabilitato")


</dt> <dd>

Servizio che non può più essere avviato.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Success**
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

**Servizi dipendenti in esecuzione**
</dt> <dd>

3

Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.

</dd> <dt>

**Controllo del servizio non valido**
</dt> <dd>

4

Il codice di controllo richiesto non è valido o non è accettabile per il servizio.

</dd> <dt>

**Il servizio non può accettare il controllo**
</dt> <dd>

5

Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.

</dd> <dt>

**Servizio non attivo**
</dt> <dd>

6

Il servizio non è stato avviato.

</dd> <dt>

**Timeout richiesta servizio**
</dt> <dd>

7

Il servizio non ha risposto in tempo utile alla richiesta di avvio.

</dd> <dt>

**Errore sconosciuto**
</dt> <dd>

8

Errore sconosciuto durante l'avvio del servizio.

</dd> <dt>

**Percorso non trovato**
</dt> <dd>

9

Impossibile trovare il percorso di directory del file eseguibile del servizio.

</dd> <dt>

**Servizio già in esecuzione**
</dt> <dd>

10

Il servizio è già in esecuzione.

</dd> <dt>

**Database del servizio bloccato**
</dt> <dd>

11

Il database a cui aggiungere il nuovo servizio è bloccato.

</dd> <dt>

**Dipendenza servizio eliminata**
</dt> <dd>

12

Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.

</dd> <dt>

**Errore di dipendenza del servizio**
</dt> <dd>

13

Impossibile trovare un servizio dipendente necessario.

</dd> <dt>

**Servizio disabilitato**
</dt> <dd>

14

Il servizio è stato disabilitato dal sistema.

</dd> <dt>

**Accesso al servizio non riuscito**
</dt> <dd>

15

Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.

</dd> <dt>

**Servizio contrassegnato per l'eliminazione**
</dt> <dd>

16

Questo servizio verrà rimosso dal sistema.

</dd> <dt>

**Servizio senza thread**
</dt> <dd>

17

Il servizio non dispone di un thread di esecuzione.

</dd> <dt>

**Stato dipendenza circolare**
</dt> <dd>

18

Il servizio ha dipendenze circolari all'avvio.

</dd> <dt>

**Stato nome duplicato**
</dt> <dd>

19

Un servizio è in esecuzione con lo stesso nome.

</dd> <dt>

**Stato nome non valido**
</dt> <dd>

20

Il nome del servizio contiene caratteri non validi.

</dd> <dt>

**Stato parametro non valido**
</dt> <dd>

21

Sono stati passati parametri non validi al servizio.

</dd> <dt>

**Stato account del servizio non valido**
</dt> <dd>

22

L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.

</dd> <dt>

**Il servizio stato esiste**
</dt> <dd>

23

Il servizio esiste già nel database dei servizi disponibili dal sistema.

</dd> <dt>

**Servizio già sospeso**
</dt> <dd>

24

Il servizio è attualmente sospeso nel sistema.

</dd> <dt>

**Altri**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="examples"></a>Esempio

La seguente [modifica StartMode di un esempio di servizio](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell, Estratto dalla raccolta TechNet, modifica la modalità di avvio di un servizio.


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



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

[**\_Servizio Win32**](win32-service.md)
</dt> <dt>

[Attività WMI: Servizi](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

