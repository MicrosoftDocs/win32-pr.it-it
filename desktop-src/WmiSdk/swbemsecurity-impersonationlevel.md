---
description: La proprietà ImpersonationLevel è un numero intero che definisce il livello di rappresentazione COM assegnato a questo oggetto.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: Proprietà SWbemSecurity. ImpersonationLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.ImpersonationLevel
- ISWbemSecurity.ImpersonationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3b996d5920aba91fddf880ee9ddf6bf8081fb39f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885386"
---
# <a name="swbemsecurityimpersonationlevel-property"></a>Proprietà SWbemSecurity. ImpersonationLevel

La proprietà **ImpersonationLevel** è un numero intero che definisce il livello di rappresentazione com assegnato a questo oggetto. Questa impostazione determina se i processi di proprietà di Strumentazione gestione Windows (WMI) possono rilevare o utilizzare le credenziali di sicurezza quando si effettuano chiamate ad altri processi. Per ulteriori informazioni sui livelli di rappresentazione, vedere [impostazione della \_ sicurezza del \_ processo dell'applicazione client](setting-client-application-process-security.md).

Se non si imposta il livello di rappresentazione in modo specifico in un moniker o se si imposta la proprietà **SWBemSecurity. ImpersonationLevel** su un oggetto a protezione diretta, WMI imposta il livello di rappresentazione predefinito sul valore specificato nella [chiave del registro di sistema del livello di rappresentazione predefinito](setting-the-default-process-security-level-using-vbscript.md). Se questa impostazione non è sufficiente, il provider non esegue la manutenzione della richiesta e la chiamata all'API WMI può avere esito negativo con codice di errore **wbemErrAccessDenied** (2147749891/0x80041003).

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Come livello di rappresentazione DCOM, questa proprietà può essere impostata su uno dei valori seguenti:



| Valore           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Anonimo**   | Nasconde le credenziali del chiamante. WMI non supporta effettivamente questo livello di rappresentazione; Se uno script specifica impersonationLevel = Anonymous, WMI aggiornerà automaticamente il livello di rappresentazione per identificare. In alcuni casi, tuttavia, un esercizio non significativo, perché gli script che usano il livello di identificazione avranno probabilmente esito negativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Identificare**    | Consente agli oggetti di eseguire query sulle credenziali del chiamante. Gli script che usano questo livello di rappresentazione avranno probabilmente esito negativo; il livello di identificazione generalmente non consente di controllare gli elenchi di controllo di accesso. Non sarà possibile eseguire script su computer remoti tramite l'operazione di identificazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Impersonate** | Consente agli oggetti di usare le credenziali del chiamante. Si consiglia di utilizzare questo livello di rappresentazione con script WMI. Quando si esegue questa operazione, lo script WMI utilizzerà le credenziali dell'utente. di conseguenza, sarà in grado di eseguire tutte le attività che è possibile eseguire.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Delegato**    | Consente agli oggetti di permettere ad altri oggetti di usare le credenziali del chiamante. La delega consente a uno script di usare le credenziali in un computer remoto e quindi consente a tale computer remoto di usare le credenziali in un altro computer remoto. Sebbene sia possibile utilizzare questo livello di rappresentazione all'interno di script WMI, è consigliabile eseguire questa operazione solo se necessario, perché potrebbe causare un rischio per la sicurezza.<br/> Non è possibile utilizzare il livello di rappresentazione del delegato a meno che tutti gli account utente e gli account computer utilizzati nella transazione non siano stati contrassegnati come trusted per la delega in Active Directory. Questo consente di ridurre al minimo i rischi per la sicurezza. Sebbene un computer remoto possa utilizzare le proprie credenziali, questa operazione può essere eseguita solo se entrambi i computer interessati dalla transazione sono attendibili per la delega.<br/> |



 

Come indicato, la rappresentazione anonima nasconde le credenziali e l'identificazione consente a un oggetto remoto di eseguire query sulle credenziali, ma l'oggetto remoto non può rappresentare il contesto di sicurezza. In altre parole, anche se l'oggetto remoto sa chi è, non può essere "finta". Gli script WMI che accedono a computer remoti utilizzando una di queste due impostazioni in genere avranno esito negativo. In realtà, la maggior parte degli script eseguiti nel computer locale utilizzando una di queste due impostazioni avrà esito negativo.

La rappresentazione consente al servizio WMI remoto di utilizzare il contesto di sicurezza per eseguire l'operazione richiesta. Una richiesta WMI remota che utilizza l'impostazione rappresenta in genere ha esito positivo, purché le credenziali dispongano di privilegi sufficienti per eseguire l'operazione desiderata. In altre parole, non è possibile utilizzare WMI per eseguire un'azione (in remoto o in altro modo) che non si dispone delle autorizzazioni necessarie per eseguire all'esterno di WMI.

L'impostazione di impersonationLevel su Delegate consente al servizio WMI remoto di passare le credenziali ad altri oggetti ed è in genere considerato un rischio per la sicurezza.

È possibile impostare il livello di rappresentazione di un oggetto [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) impostando la proprietà **ImpersonationLevel** sul valore desiderato. Nell'esempio seguente viene illustrato come impostare il livello di rappresentazione per un oggetto **SWbemObject** :


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



È inoltre possibile specificare livelli di rappresentazione come parte di un moniker. Nell'esempio seguente viene impostato il livello di autenticazione e il livello di rappresentazione e viene recuperata un'istanza del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,"& _
                         "authenticationLevel=pktPrivacy}"& _
                         "!root/cimv2:Win32_service='ALERTER'")
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSECURITY CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMSECURITY IID<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Impostazione della \_ sicurezza del processo dell'applicazione client \_](setting-client-application-process-security.md)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

