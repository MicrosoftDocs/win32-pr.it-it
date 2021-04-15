---
title: Metodo StartService della classe Win32_Service (Servizi Desktop remoto)
description: Tenta di collocare il servizio a cui si fa riferimento nello stato di avvio.
ms.assetid: 4DA05C48-03A0-4D4B-9E69-0404393C219C
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo StartService
- Metodo StartService Servizi Desktop remoto, classe Win32_Service
- Classe Win32_Service Servizi Desktop remoto, metodo StartService
topic_type:
- apiref
api_name:
- Win32_Service.StartService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e37a17922fe0f4f3f5a3e4f1cd4d8eb67dc2858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400569"
---
# <a name="startservice-method-of-the-win32_service-class-remote-desktop-services"></a>Metodo StartService della classe Win32_Service (Servizi Desktop remoto)

Il metodo **StartService** tenta di collocare il servizio a cui si fa riferimento nello stato di avvio.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 StartService();
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

Sebbene sia possibile che non esistano differenze pratiche tra un servizio interrotto e un servizio sospeso, i due stati vengono visualizzati in modo diverso rispetto a SCM. Un servizio interrotto è un servizio che non è in esecuzione e che deve seguire l'intera procedura di avvio del servizio. Un servizio sospeso, tuttavia, è ancora in esecuzione, ma il suo funzionamento è stato sospeso. Per questo motivo, non è necessario che un servizio sospeso attraversi l'intera procedura di avvio del servizio, ma è necessaria una procedura diversa per riprendere il funzionamento.

È necessario utilizzare il metodo appropriato per avviare un servizio che è stato interrotto o per riprendere un servizio che è stato sospeso. I metodi del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) **StartService** e [**ResumeService**](win32-terminalservice-resumeservice.md) devono essere utilizzati nelle situazioni seguenti:

-   Se un servizio è attualmente arrestato, è necessario usare il metodo **StartService** per riavviarlo; [**ResumeService**](win32-terminalservice-resumeservice.md) non è in grado di avviare un servizio attualmente arrestato.
-   Se un servizio viene sospeso, è necessario utilizzare [**ResumeService**](win32-terminalservice-resumeservice.md). Se si usa il metodo **StartService** in un servizio in pausa, viene visualizzato il messaggio "il servizio è già in esecuzione". Tuttavia, il servizio rimane sospeso fino a quando non viene inviato il codice di controllo del servizio di ripresa.

Se si avvia un servizio interrotto che dipende da un altro servizio, vengono avviati entrambi i servizi. Quando un servizio viene avviato con questo metodo, tutti i servizi dipendenti non vengono avviati automaticamente. Per individuare i dipendenti e avviarli separatamente, è necessario utilizzare la classe di associazione [**Win32 \_ DependentService**](/windows/desktop/CIMWin32Prov/win32-dependentservice) e gli [associatori di](/windows/desktop/WmiSdk/associators-of-statement) query.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
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
</dt> </dl>

 

