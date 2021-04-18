---
title: Metodo StopService della classe Win32_Service (Sdoias. h) (servizio Terminal)
description: Inserisce il servizio, rappresentato dall' \_ oggetto TerminalService Win32, nello stato interrotto.
ms.assetid: 228711DC-369B-48B6-96EE-DF4026904E26
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo StopService
- Metodo StopService Servizi Desktop remoto, classe Win32_Service
- Classe Win32_Service Servizi Desktop remoto, metodo StopService
topic_type:
- apiref
api_name:
- Win32_Service.StopService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1b21db330bb9111b96fb244200845cb83b3153
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334052"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash-for-the-terminal-service"></a>Metodo StopService della classe Win32_Service (Sdoias. h) per il servizio Terminal

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** posiziona il servizio, rappresentato dall' [**oggetto \_ TerminalService Win32**](win32-terminalservice.md) , nello stato interrotto.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

La richiesta è stata accettata.

</dd> <dt>

**1**
</dt> <dd>

La richiesta non è supportata.

</dd> <dt>

**2**
</dt> <dd>

L'utente non dispone dell'accesso necessario.

</dd> <dt>

**3**
</dt> <dd>

Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.

</dd> <dt>

**4**
</dt> <dd>

Il codice di controllo richiesto non è valido o non è accettabile per il servizio.

</dd> <dt>

**5**
</dt> <dd>

Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Proprietà state** ) è uguale a 0, 1 o 2.

</dd> <dt>

**6**
</dt> <dd>

Il servizio non è stato avviato.

</dd> <dt>

**7**
</dt> <dd>

Il servizio non ha risposto in tempo utile alla richiesta di avvio.

</dd> <dt>

**8**
</dt> <dd>

Errore sconosciuto durante l'avvio del servizio.

</dd> <dt>

**9**
</dt> <dd>

Impossibile trovare il percorso di directory del file eseguibile del servizio.

</dd> <dt>

**10**
</dt> <dd>

Il servizio è già in esecuzione.

</dd> <dt>

**11**
</dt> <dd>

Il database a cui aggiungere il nuovo servizio è bloccato.

</dd> <dt>

**12**
</dt> <dd>

Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.

</dd> <dt>

**13**
</dt> <dd>

Impossibile trovare un servizio dipendente necessario.

</dd> <dt>

**14**
</dt> <dd>

Il servizio è stato disabilitato dal sistema.

</dd> <dt>

**15**
</dt> <dd>

Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.

</dd> <dt>

**16**
</dt> <dd>

Questo servizio verrà rimosso dal sistema.

</dd> <dt>

**17**
</dt> <dd>

Il servizio non dispone di un thread di esecuzione.

</dd> <dt>

**18**
</dt> <dd>

Il servizio ha dipendenze circolari all'avvio.

</dd> <dt>

**19**
</dt> <dd>

Un servizio è in esecuzione con lo stesso nome.

</dd> <dt>

**20**
</dt> <dd>

Il nome del servizio contiene caratteri non validi.

</dd> <dt>

**21**
</dt> <dd>

Sono stati passati parametri non validi al servizio.

</dd> <dt>

**22**
</dt> <dd>

L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.

</dd> <dt>

**23**
</dt> <dd>

Il servizio esiste già nel database dei servizi disponibili dal sistema.

</dd> <dt>

**24**
</dt> <dd>

Il servizio è attualmente sospeso nel sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

Dopo aver determinato i servizi che possono essere arrestati o sospesi, è possibile usare i metodi **StopService** e [**PauseService**](win32-terminalservice-pauseservice.md) per arrestare e sospendere i servizi. La decisione di arrestare un servizio anziché sospenderla, o viceversa, dipende da diversi fattori, inclusi i seguenti:

-   Il servizio è in grado di essere sospeso? In caso contrario, l'unica opzione è arresta il servizio.
-   È necessario continuare a gestire le richieste client per chiunque si sia già connessi al servizio? In tal caso, sospendere un servizio in genere consente di gestire i client esistenti negando l'accesso ai nuovi client. Al contrario, quando si arresta un servizio, tutti i client vengono immediatamente disconnessi.
-   È necessario riconfigurare un servizio e fare in modo che le modifiche abbiano effetto immediato? Sebbene sia possibile modificare le proprietà del servizio mentre un servizio viene sospeso, la maggior parte di esse non diventano effettive fino a quando il servizio non viene effettivamente arrestato e riavviato.

Il codice di scripting necessario per arrestare un servizio è quasi identico al codice necessario per sospendere il servizio.

Se si tenta di arrestare un servizio che dispone di servizi dipendenti in esecuzione, il metodo **StopService** ha esito negativo con un valore restituito pari a 3. I servizi dipendenti devono essere arrestati per primi.

Se si arresta un servizio, controllare immediatamente il [**\_ TerminalService Win32**](win32-terminalservice.md).**Proprietà state** , perché il valore può comunque visualizzare il servizio come in esecuzione.

## <a name="examples"></a>Esempio

[Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell Sample imposta lo stato del servizio per i computer remoti.

L'esempio di [arresto di un servizio e del relativo VBScript dipendente](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) interrompe un servizio e tutti i servizi dipendenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Sdoias. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Classi del sistema operativo](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**\_TerminalService Win32**](win32-terminalservice.md)
</dt> <dt>

[Attività WMI: Servizi](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[**PauseService**](/windows/desktop/CIMWin32Prov/pauseservice-method-in-class-win32-systemdriver)
</dt> </dl>

 

